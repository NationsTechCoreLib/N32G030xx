1������˵��

	/* ���������̹��� */
        ����������ò���ʾʹ��EXIT�ⲿ�жϼ�TIM��ʱ���ж�


2��ʹ�û���

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
        �����壺N32G030C8L7-STB V1.0
        

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
        SystemClock��48MHz
        USART��TX - PA9��������115200
	    EXIT��PA0Ϊ��������ģʽ���ⲿ�ж��� - EXIT_LINE0�������ⲿ�ж�
	    TIM��Ԥ��Ƶϵ�� - ��SystemClock/1200-1�������� - ��1200-1����������ʱ���ж�

	/* ����Demo�Ĳ��Բ�������� */
        1.��������س���λ���У�
        2.�鿴���ڴ�ӡ��Ϣ����ʱ���ж���Ϣÿ1S��ӡһ�Σ����°�����ӡֹͣ���ٴΰ����������ӡ��������������������


4��ע������


1. Function description

	/* Briefly describe the project function */
         This routine configures and demonstrates the use of EXIT external interrupt and TIM timer interrupt


2. Use environment

	/* Hardware environment: the development hardware platform corresponding to the project */
         Development board: N32G030C8L7-STB V1.0
        

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
         	SystemClock: 48MHz
         	USART: TX - PA9, baud rate 115200
	EXIT: PA0 is floating input mode, external interrupt line - EXIT_LINE0, open external interrupt
	TIM: prescale factor - (SystemClock/1200-1), period - (1200-1), enable timer interrupt

	/* Describe the test steps and phenomena of the Demo */
         1. After compiling, download the program to reset and run;
         2. Check the serial port printing information, the timer interrupt information is printed every 1S, press the button to stop printing, press it again to continue printing, indicating that the program is running normally;


4. Matters needing attention

