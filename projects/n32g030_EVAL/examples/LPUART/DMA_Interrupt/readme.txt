1������˵��

    �ò�����ʾ��LPUART��USARTz��ͨ��DMA���жϣ�ʵ�ֵĻ���ͨ�š�
USARTz������USART1��
    ���ȣ�DMA����TxBuffer1������LPUART�������ݼĴ�����������ɲ���
DMA�жϣ�������ݷ�����USARTz��USARTz�������ݣ�DMA��USARTz����
���ݼĴ�������������RxBuffer2����ɺ����DMA�жϡ�
    ͬʱ��DMA����TxBuffer2������USARTz�������ݼĴ�����������ɲ���
DMA�жϣ�������ݷ�����LPUART��LPUART�������ݣ�DMA��LPUART����
���ݼĴ�������������RxBuffer1����ɺ����DMA�жϡ�
    ��󣬷ֱ�Ƚ������ա������ݣ��ȽϽ������TransferStatus1����
��TransferStatus2������


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
    - DMA����ģʽ��DMA����ģʽʹ��
    
    LPUART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ���̶���
    - 1ֹͣλ���̶���
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    - DMA����ģʽ��DMA����ģʽʹ��
    
    USART�����������£�
    - LPUART_Tx.PA1   <------->   USART1_Rx.PA10
    - LPUART_Rx.PA0   <------->   USART1_Tx.PA9

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У����β鿴����TransferStatus1��TransferStatus2�����У�
      PASSEDΪ����ͨ����FAILEDΪ�����쳣


4��ע������

    ���Ƚ�������NS-LINK��MCU_TX��MCU_RX����ñ�Ͽ�

1. Function description

   This test example demonstrates the basic communication between LPUART and USARTz via DMA (interrupt).
USARTz can be USART1.
     First, DMA transfers the TxBuffer1 data to the LPUART send data register. After the transfer is completed, 
a DMA interrupt is generated, and then the data is sent to USARTz. USARTz receives data, DMA moves data 
from USARTz receive data register to RxBuffer2, and generates DMA interrupt after completion.
     At the same time, DMA transfers TxBuffer2 data to the USARTz send data register, the transfer is completed 
and a DMA interrupt is generated, and then the data is sent to LPUART. LPUART receives data, DMA moves data 
from LPUART receive data register to RxBuffer1, and generates DMA interrupt after completion.
     Finally, compare the two groups of receiving and sending data respectively, and store the comparison results 
in the TransferStatus1 variable and the TransferStatus2 variable.


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
    -DMA transmit mode and DMA receive mode enable
    
    The LPUART configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 8 data bits (fixed)
    -1 stop bit (fixed)
    -Verification control disabled
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    -DMA transmit mode and DMA receive mode enable
    
    The USART pin connections are as follows:
    -LPUART_Tx.PA1 <-------> USART1_Rx.PA10
    -LPUART_Rx.PA0 <-------> USART1_Tx.PA9

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn, among them,
      PASSED means the test passed, FAILED means the test is abnormal


4. Matters needing attention

    the MCU_TX and MCU_RX jumper cap of the development board NS-LINK needs to be disconnected first