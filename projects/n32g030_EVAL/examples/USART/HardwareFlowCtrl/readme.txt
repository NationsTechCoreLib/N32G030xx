1������˵��

    �ò�����ʾ��USARTy��USARTz��ʹ��Ӳ�������ƵĻ���ͨ�š�USARTy��
USARTz������USART1��USART2��
    ���ȣ�USARTy����CTS����TxBuffer1���ݣ�USARTz����RTS����
���ݣ�����RxBuffer2�����USARTz����CTS����TxBuffer2���ݣ�USARTy
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
    
    USARTy�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ
    - 1ֹͣλ
    - У����ƽ���
    - CTSӲ��������ʹ��
    - ������ʹ��   
    
    USARTz�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ
    - 1ֹͣλ
    - У����ƽ���
    - RTSӲ��������ʹ��
    - ������ʹ��   
    
    
    USART�����������£�    
    - USART1_Tx.PA9      <------->   USART2_Rx.PA3
    - USART1_Rx.PA10     <------->   USART2_Tx.PA2
    - USART1_CTS.PA11   <------->   USART2_RTS.PA1 
    - USART1_RTS.PA12   <------->   USART2_CTS.PA0 

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У����β鿴����TransferStatus1��TransferStatus2�����У�
      PASSEDΪ����ͨ����FAILEDΪ�����쳣


4��ע������

    ���Ƚ�������NS-LINK��MCU_TX��MCU_RX����ñ�Ͽ�

1. Function description

    This test example demonstrates the basic communication between USARTy and USARTz using hardware flow control. USARTy and USARTz can be USART1 
and USART2.
    First, USARTy uses CTS to send TxBuffer1 data, USARTz uses RTS to receive data and stores it in RxBuffer2; then, USARTz uses CTS to send TxBuffer2 data, 
and USARTy uses RTS to receive data and stores it in RxBuffer1.
    Then, compare the received data with the sent data, and the comparison results are stored in the variables TransferStatus1 and TransferStatus2 respectively.

2. Use environment

    Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

    Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

    The system clock configuration is as follows:
    -Clock source = HSI + PLL
    -System clock = 48MHz
    
    The USARTy configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits
    -1 stop bit
    -Verification control disabled
    -CTS hardware flow control enable
    -Transmitter enable
    
    The USARTz configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits
    -1 stop bit
    -Verification control disabled
    -RTS hardware flow control enable
    -Receiver enable
    
    
    The USART pin connections are as follows:
    -USART1_Tx.PA9 <-------> USART2_Rx.PA3
    -USART1_Rx.PA10 <-------> USART2_Tx.PA2
    -USART1_CTS.PA11 <-------> USART2_RTS.PA1
    -USART1_RTS.PA12 <-------> USART2_CTS.PA0

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn,
Among them, PASSED means the test passed and FAILED means the test is abnormal


4. Matters needing attention

    the MCU_TX and MCU_RX jumper cap of the development board NS-LINK needs to be disconnected first