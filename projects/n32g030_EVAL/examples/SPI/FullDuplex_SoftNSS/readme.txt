1������˵��

	1��SPI ȫ˫����� NSS ģʽ���ͽ�������

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��NNationstech.N32G030_Library.0.1.0

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	SystemClock��48MHz
	GPIO��SPI1: SCK--PA5�� MISO--PA6�� MOSI--PA7,
	           SPI2: SCK--PB13��MISO--PB14��MOSI--PB15��

	/* ����Demo�Ĳ��Բ�������� */
	1.��������س���λ���У�
	2.SPI1 ��ʼ��λ�������������ݣ�SPI2 ��ʼ��λ�Ի����������� ��������ɺ󣬼�����ݣ��鿴 TransferStatus1 �� TransferStatus2 ״̬Ϊ PASSED��
	  SPI2 ��ʼ��λ�������������ݣ�SPI1 ��ʼ��λ�Ի����������� ��������ɺ󣬼�����ݣ��鿴 TransferStatus3 �� TransferStatus4 ״̬Ϊ PASSED��

4��ע������
	��




1. Function description

	1. SPI full-duplex software NSS mode to send and receive data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: NNationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
	GPIO: SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	          SPI2: SCK--PB13, MISO--PB14, MOSI--PB15,

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. SPI1 initializes the bit host, sends data, SPI2 initializes the bit cluster machine, receives data, after the transmission is completed, 
	    check the data, check that the status of TransferStatus1 and TransferStatus2 is PASSED,
	    SPI2 initializes the bit host, sends data, SPI1 initializes the bit cluster machine, receives data, and after the transmission is completed,
	    check the data, and check that the status of TransferStatus3 and TransferStatus4 is PASSED;

4. Matters needing attention
	none