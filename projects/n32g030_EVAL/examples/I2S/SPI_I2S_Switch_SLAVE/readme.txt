1������˵��

	1��I2S ��ģʽ������������Ժ��л��� SPI ��ģʽ�������ݣ����л��� I2S ��ģʽ��������

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��Nationstech.N32G030_Library.1.1.1

	 /* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.1

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	1��SystemClock��48MHz
	2��GPIO������ģʽ DEMO �壩I2S1: WS--PA4��CK--PA5��SD--PA7
	         ����ģʽ DEMO �壩I2S1: WS--PA4��CK--PA5��SD--PA7

	/* ����Demo�Ĳ��Բ�������� */
	1.��������س���λ���У�
	2.��ģʽ DEMO ��������ģʽ���Ȱ�ס��ģʽ DEMO �帴λ����Ȼ���ģʽ DEMO ��ȫ���ܣ����ɿ���ģʽ DEMO �帴λ����
	  �鿴 TransferStatus1��TransferStatus2��TransferStatus2 ״̬Ϊ PASSED

4��ע������
	��Ҫ���� demo ����ϣ�һ�������¼��ģʽ����һ�������¼��ģʽ�������������һ���ϵ磬����������ӵ� VCC �� GND




1. Function description

	1. After receiving data in I2S slave mode, switch to SPI slave mode to receive data, and then switch to I2S master mode to receive data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.1.1.1

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.1

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 48MHz
	2. GPIO: (main mode DEMO board)  I2S1: WS--PA4, CK--PA5, SD--PA7
	         (Slave mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Enter the debug mode from the mode DEMO board, first press and hold the main mode DEMO board reset button, 
	   then run the slave mode DEMO board at full speed, then release the main mode DEMO board reset button, 
	   check the status of TransferStatus1, TransferStatus2, TransferStatus2 is PASSED.

4. Matters needing attention
	Two demo boards are required, one board to program the master mode program, one board to program the slave mode program, 
	the two boards need to be powered on together, and connect the VCC and GND of the two boards