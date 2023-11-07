1������˵��

	1��SPI ���ͽ������ݽ��� CRC У��

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��Nationstech.N32G030_Library.0.1.0

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	SystemClock��48MHz
	GPIO��SPI1: SCK--PA5�� MISO--PA6�� MOSI--PA7,
                           SPI2: SCK--PB13��MISO--PB14��MOSI--PB15��

	/* ����Demo�Ĳ��Բ�������� */
	1.��������س���λ���У�
	2.SPI1��SPI2 ͬʱ�շ����ݣ�������ɺ󣬷��� CRC ���ݣ�������ݺ� CRC ֵ���鿴 TransferStatus1 �� TransferStatus2 ״̬Ϊ PASSED���ٲ鿴 CRC ֵ��

4��ע������
	��




1. Function description

	1. SPI sends and receives data for CRC check

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
	GPIO: SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
                          SPI2: SCK--PB13, MISO--PB14, MOSI--PB15,

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. SPI1 and SPI2 send and receive data at the same time. After the transmission is completed, send the CRC data, 
	    check the data and CRC value, check that the status of TransferStatus1 and TransferStatus2 is PASSED, and then check the CRC value;

4. Matters needing attention
	none