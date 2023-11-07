1������˵��

	1��I2S ��ģʽͨ�� DMA �շ�����

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
        3��DMA��I2S1 ���Ͳ��� DMA_CH3 ͨ����I2S1 ���ղ��� DMA_CH2 ͨ����
        4����־��ӡ����ģʽ DEMO �� PA9(TX)�������ʣ�115200
	
         /* ����Demo�Ĳ��Բ�������� */
        1����������س���λ���У�
        2����ģʽ DEMO ��ʹ�ģʽ DEMO ��PA4,PA5,PA7���Ӻú󣬴�ģʽ DEMO �����Ӵ��ڴ�ӡ���ߣ��ϵ磬
           �Ȱ�ס��ģʽ DEMO �帴λ�����ɣ��ٰ��´�ģʽ DEMO ��ĸ�λ������ģʽ DEMO �������������ɿ���ģʽ DEMO ��ĸ�λ�����鿴��ӡ���Գɹ���

4��ע������
	��Ҫ���� demo ����ϣ�һ�������¼��ģʽ����һ�������¼��ģʽ�������������һ���ϵ磬����������ӵ� VCC �� GND



1. Function description

	1. I2S slave mode sends and receives data through DMA

2. Use environment

        /* Software development environment: the name and version number of the software tool used in the current project */
        IDE tool: KEIL MDK-ARM 5.30.0.0
        SDK version: Nationstech.N32G030_Library.1.1.1

        /* Hardware environment: the development hardware platform corresponding to the project */
        Development board: N32G030CL-STB V1.0 V1.1

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 48MHz
	2. GPIO: (main mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7
	(Slave mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7
	3. DMA: I2S1 transmission adopts DMA_CH3 channel, I2S1 reception adopts DMA_CH2 channel;
	4. Log printing: slave mode DEMO board PA9(TX), baud rate: 115200

	 /* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. After the master mode DEMO board and the slave mode DEMO board PA4, PA5, PA7 are connected, 
	   the slave mode DEMO board is connected to the serial port printing tool, power on,
       First press and hold the reset button of the master mode DEMO board, then press the reset button of the slave mode DEMO board, 
       and then release the reset button of the master mode DEMO board after the slave mode DEMO board runs to check that the print test is successful;

4. Matters needing attention
	Two demo boards are required, one board to program the master mode program, one board to program the slave mode program,
	the two boards need to be powered on together, and connect the VCC and GND of the two boards.