1������˵��

    �ò�����ʾ��LPUART��USARTz��ʹ��Ӳ�������ƵĻ���ͨ�š�USARTz
������USART1��
    ���ȣ�LPUART����CTS����TxBuffer1���ݣ�USARTz����RTS����
���ݣ�����RxBuffer2�����USARTz����CTS����TxBuffer2���ݣ�LPUART
����RTS�������ݣ�����RxBuffer1��
    ��󣬱ȽϽ��������뷢�����ݣ��ȽϽ���ֱ�������TransferStatus1
��TransferStatus2��


2��ʹ�û���

    �������������KEIL MDK-ARM Professional Version 5.26.2.0

    Ӳ����������Сϵͳ��N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    ϵͳʱ���������£�
    - ʱ��Դ = HSI + PLL
    - ϵͳʱ�� = 48MHz
    
    LPUART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ���̶���
    - 1ֹͣλ���̶���
    - У����ƽ���
    - CTS��RTSӲ��������ʹ��
    - �������ͷ�����ʹ��
   
    USART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ
    - 1ֹͣλ
    - У����ƽ���
    - CTS��RTSӲ��������ʹ�ܣ�
    - �������ͷ�����ʹ��
    
    
    LPUART��USART�����������£�    
    - LPUART_Tx.PA1      <------->   USART1_Rx.PA10
    - LPUART_Rx.PA0      <------->   USART1_Tx.PA9
    - LPUART_CTS.PA6    <------->   USART1_RTS.PA12
    - LPUART_RTS.PA15   <------->   USART1_CTS.PA8  

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У����β鿴����TransferStatus1��TransferStatus2�����У�
      PASSEDΪ����ͨ����FAILEDΪ�����쳣


4��ע������

    ���Ƚ�������NS-LINK��MCU_TX��MCU_RX����ñ�Ͽ�

1. Function description

    This test example demonstrates the basic communication between LPUART and USARTz using hardware flow control. USARTz can be USART1.
     First, LPUART uses CTS to send TxBuffer1 data, USARTz uses RTS to receive data and stores it in RxBuffer2; then, USARTz uses CTS to send 
TxBuffer2 data, and LPUART uses RTS to receive data and stores it in RxBuffer1.
     Then, compare the received data with the sent data, and the comparison results are stored in the variables TransferStatus1 and TransferStatus2 respectively.


2. Use environment

    Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

    Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

    The system clock configuration is as follows:
    -Clock source = HSI + PLL
    -System clock = 48MHz
    
    The LPUART configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits (fixed)
    -1 stop bit (fixed)
    -Verification control disabled
    -CTS and RTS hardware flow control enable
    -Receiver and transmitter enable
   
    The USART configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits
    -1 stop bit
    -Verification control disabled
    -CTS and RTS hardware flow control enable)
    -Receiver and transmitter enable
    
    
    The LPUART and USART pin connections are as follows:
    -LPUART_Tx.PA1 <-------> USART1_Rx.PA10
    -LPUART_Rx.PA0 <-------> USART1_Tx.PA9
    -LPUART_CTS.PA6 <-------> USART1_RTS.PA12
    -LPUART_RTS.PA15 <-------> USART1_CTS.PA8

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn, among them,
      PASSED means the test passed, FAILED means the test is abnormal


4. Matters needing attention

    the MCU_TX and MCU_RX jumper cap of the development board NS-LINK needs to be disconnected first