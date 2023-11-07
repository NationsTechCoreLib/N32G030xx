1������˵��

    �ò�����ʾ��USARTy��ͬ��ģʽ����SPIy��ͨ����ѯ����ʶʵ�ֵĻ���ͨ�š�
USARTy��SPIy������USART1��SPI1��USART3��SPI1��USART2��SPI2��
    ���ȣ�ͨ��TXC����־��USARTy����TxBuffer1������SPIy����SPIy�������ݣ�
���ѯRNE����־�����յ����ݴ���RxBuffer1��
    ���SPIyͨ����ѯTE����־������TxBuffer2������USARTy��USARTy������
RXDNE����־�������ݣ��������RxBuffer2��
    ��󣬷ֱ�Ƚ������ա������ݣ��ȽϽ������TransferStatus1����
��TransferStatus2������


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
    - ʱ��ʹ��
    - ʱ�Ӽ��ԣ������ⷢ��ʱ���ָߵ�ƽ
    - ʱ����λ���ڵڶ���ʱ�ӱ��ز�����һ������
    - ���һλʱ�����壺���һλ���ݵ�ʱ�������CK���
    
    SPI�������£�
    - ���� = ��˫��˫��ģʽ
    - ģʽ = ��ģʽ
    - ���ݴ�С = 8λ����֡
    - CPOL = ����״̬ʱ��ʱ�ӱ��ָߵ�ƽ
    - CPHA = ���ݲ����ӵڶ���ʱ�ӱ��ؿ�ʼ
    - NSS = ����������豸����
    - ��1λ = ��1λΪLSB
    
    
    USART�����������£�    
    - USART1_Tx.PA9    <------->   SPI1_MOSI.PA7
    - USART1_Rx.PA10   <------->   SPI1_MISO.PA6
    - USART1_Clk.PA8   <------->   SPI1_SCK.PA5  
    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У����β鿴����TransferStatus1��TransferStatus2�����У�
      PASSEDΪ����ͨ����FAILEDΪ�����쳣


4��ע������

    ���Ƚ�������NS-LINK��MCU_TX��MCU_RX����ñ�Ͽ�


1. Function description

    This test example demonstrates the basic communication between USARTy (synchronous mode) and SPIy by querying the detection identifier.
USARTy and SPIy can be USART1 and SPI1, USART3 and SPI1 or USART2 and SPI2.
    First, through the TXC detection flag, USARTy sends TxBuffer1 data to SPIy, while SPIy receives data, it queries the RNE detection flag, and the 
received data is stored in RxBuffer1.
    Subsequently, SPIy sends TxBuffer2 data to USARTy by querying the TE detection flag. USARTy uses the RXDNE detection flag to receive data 
and stores it in RxBuffer2.
    Finally, compare the two groups of receiving and sending data respectively, and store the comparison results in the TransferStatus1 variable 
and the TransferStatus2 variable.


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
    -Clock enable
    -Clock polarity: keep high when not sending out
    -Clock phase: sample the first data on the second clock edge
    -The last clock pulse: the clock pulse of the last data is output from CK
    
    The SPI configuration is as follows:
    -Direction = "Two-wire two-way" mode
    -Mode = slave mode
    -Data size = 8-bit data frame
    -CPOL = In idle state, the clock stays high
    -CPHA = data sampling starts from the second clock edge
    -NSS = Enable software management from the device
    -1st bit = 1st bit is LSB
    
    
    The USART pin connections are as follows:
    -USART1_Tx.PA9 <-------> SPI1_MOSI.PA7
    -USART1_Rx.PA10 <-------> SPI1_MISO.PA6
    -USART1_Clk.PA8 <-------> SPI1_SCK.PA5
    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the variables TransferStatus1 and TransferStatus2 in turn, among them,
      PASSED means the test passed, FAILED means the test is abnormal


4. Matters needing attention

    the MCU_TX and MCU_RX jumper cap of the development board NS-LINK needs to be disconnected first