1������˵��

    �ò�����ʾ��LPUART��USARTz��ͨ����ѯ����ʶʵ�ֵĻ���ͨ�š�USARTz
������USART1��
    ���ȣ�LPUART����TxBuffer1������USARTz��USARTz�������ݴ���RxBuffer2��
�ȽϽ��������뷢�����ݣ��ȽϽ������TransferStatus1������
    ���USARTz����TxBuffer2������LPUART��LPUART�������ݴ���RxBuffer1��
�ȽϽ��������뷢�����ݣ��ȽϽ������TransferStatus2������


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
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    
    USART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ
    - 1ֹͣλ
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    
    LPUART��USART�����������£�
    - LPUART_Tx.PA1   <------->   USART1_Rx.PA10
    - LPUART_Rx.PA0   <------->   USART1_Tx.PA9

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У����β鿴����TransferStatus1��TransferStatus2�����У�
      PASSEDΪ����ͨ����FAILEDΪ�����쳣


4��ע������

    ���Ƚ�������NS-LINK��MCU_TX��MCU_RX����ñ�Ͽ�

1. Function description

    This test case demonstrates the basic communication between LPUART and USARTz by querying the detection mark. USARTz
can be USART1.
    First, LPUART sends TxBuffer1 data to USARTz, and USARTz receives data and stores it in RxBuffer2.
Compare the received data with the sent data, and the comparison result is stored in the TransferStatus1 variable.
    Subsequently, USARTz sends TxBuffer2 data to LPUART, and LPUART receives data to RxBuffer1.
Compare the received data with the sent data, and the result of the comparison is stored in the TransferStatus2 variable.


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
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    
    The USART configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits
    -1 stop bit
    -Verification control disabled
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    
    The LPUART and USART pin connections are as follows:
    -LPUART_Tx.PA1 <-------> USART1_Rx.PA10
    -LPUART_Rx.PA0 <-------> USART1_Tx.PA9

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn, among them,
      PASSED means the test passed, FAILED means the test is abnormal


4. Matters needing attention

    the MCU_TX and MCU_RX jumper cap of the development board NS-LINK needs to be disconnected first