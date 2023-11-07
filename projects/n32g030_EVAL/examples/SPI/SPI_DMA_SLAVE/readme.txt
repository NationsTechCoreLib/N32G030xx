1������˵��

	1��SPI ��ģʽȫ˫�� DMA ���ͺ͵��߽�������

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��Nationstech.N32G030_Library.0.1.0

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	SystemClock��48MHz
	GPIO������ģʽ DEMO �壩SPI1: SCK--PA5��MISO--PA6��MOSI--PA7,
	           ����ģʽ DEMO �壩SPI1: SCK--PA5��MISO--PA6��MOSI--PA7,
	��־��ӡ����ģʽ DEMO �� PA9(TX)�������ʣ�115200

	/* ����Demo�Ĳ��Բ�������� */
	1����������س���λ���У�
	2���Ӻô��ڴ�ӡ���ߣ��ϵ磬�鿴��ӡ���Գɹ�

4��ע������
	��Ҫ���� demo ����ϣ�һ�������¼��ģʽ����һ�������¼��ģʽ�������������һ���ϵ磬����������ӵ� VCC �� GND




1. Function description

	1. SPI slave mode full-duplex DMA transmit and single-wire receive data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
	GPIO: (master mode DEMO board) SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	             (Slave mode DEMO board) SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	Log print: slave mode DEMO board PA9(TX), baud rate: 115200

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Connect the serial port printing tool, power on, and check that the printing test is successful

4. Matters needing attention
	Two demo boards are required, one board to program the master mode program, one board to program the slave mode program,
	 the two boards need to be powered on together, and connect the VCC and GND of the two boards.