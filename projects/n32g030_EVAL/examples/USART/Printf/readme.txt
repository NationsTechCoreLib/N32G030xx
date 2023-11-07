1������˵��

    �ò�����ʾ��USARTx��PC��ͨ����ѯ����ʶʵ�ֵĻ���ͨ�š�
    �ض���printf������USARTx����ʹ��printf���������Ϣ���նˡ�
    USARTx������USART1��USART2��


2��ʹ�û���

    �������������KEIL MDK-ARM Professional Version 5.26.2.0

        Ӳ����������Сϵͳ��N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    ϵͳʱ���������£�
    - ʱ��Դ = HSI + PLL
    - ϵͳʱ�� = 48MHz
    
    USART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ
    - 1ֹͣλ
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    
    USART�����������£�
    - USART1_Tx.PA9 
    ��
    - USART2_Tx.PA2
    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У��鿴���ڴ�ӡ��Ϣ


4��ע������



1. Function description

    This test case demonstrates the basic communication between USARTy and USARTz by querying the detection identification.
    First, USARTy sends TxBuffer1 data to USARTz, and USARTz receives data and stores it in RxBuffer1.
Compare the received data with the sent data, and the comparison result is stored in the TransferStatus1 variable.
    Subsequently, USARTz sends TxBuffer2 data to USARTy, and USARTy receives data to RxBuffer2.
Compare the received data with the sent data, and the result of the comparison is stored in the TransferStatus2 variable.
    USARTy and USARTz can be USART1 and USART2.


2. Use environment

    Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

    Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

    The system clock configuration is as follows:
    -Clock source = HSI + PLL
    -System clock = 48MHz
    
    The USART configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits
    -1 stop bit
    -Verification control disabled
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    
    The USART pin connections are as follows:
    -USART1_Tx.PA9 <-------> USART2_Rx.PA3
    -USART1_Rx.PA10 <-------> USART2_Tx.PA2

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn, among them,
      PASSED means the test passed, FAILED means the test is abnormal


4. Matters needing attention