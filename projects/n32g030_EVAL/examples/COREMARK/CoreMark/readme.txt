1������˵��

	/* ���������̹��� */
        ����������ò���ʾMCU�ֲܷ���


2��ʹ�û���

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
        �����壺N32G030C8L7-STB V1.0
        

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	SystemClock��48MHz
    USART��TX - PA9��RX - PA10��������115200
	SysTick��ʱ�ӵδ�����Ϊ1MS

	/* ����Demo�Ĳ��Բ�������� */
        1.��������س���λ���У�
        2.ͨ�����ڴ�ӡ���ֽܷ����


4��ע������
	�����̵�IAR����Ϊ�˳�ֲ���оƬ������Ҫ�޸Ķ�ջ��Ϊ������������̳�ͻ��������Ҫѡ�񹤳��ڲ���icf�ļ�������·����icf�ļ����Ҳ������±��������Ҫ�򿪹��̺�ѡ��Options->linker->config->Override default������ѡ�񹤳��ڲ���N32G030x6.icf�ļ����ɣ����±����Ͳ��ᱨ��



1. Function description

	/* Briefly describe the project function */
         This example configures and demonstrates the MCU benchmark


2. Use environment

	/* Hardware environment: the development hardware platform corresponding to the project */
         Development board: N32G030C8L7-STB V1.0
        

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
     	USART: TX - PA9, RX - PA10, baud rate 115200
	SysTick: Clock ticks configured as 1MS

	/* Describe the test steps and phenomena of the Demo */
         	1. After compiling, download the program to reset and run;
         	2. Print out the running score results through the serial port;


4. Matters needing attention
	The IAR project of this routine needs to modify the stack in order to fully test the chip performance. In order to avoid conflicts with other routines, it is necessary to select the icf file inside the project. After changing the path, the icf file will not be found, resulting in a compilation error. You need to open the project and select Under Options->linker->config->Override default, re-select the N32G030x6.icf file inside the project, and no error will be reported after recompiling.