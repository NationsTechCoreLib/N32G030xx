1������˵��

	/* ���������̹��� */
        ����������ò���ʾ����޸��߳�ģʽ��Ȩ���ʼ���ջ


2��ʹ�û���

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
        �����壺N32G030C8L7-STB V1.0


3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
        SystemClock��48MHz
        USART��TX - PA9��RX - PA10��������115200

	/* ����Demo�Ĳ��Բ�������� */
        1.��������س���λ���У�
        2.��ʹ�ñ������ġ�Cortex�Ĵ��������ڲ鿴�߳�ģʽ�£�ʹ�õĶ�ջ������ķ��ʼ�����Ȩ��/����Ȩ������


4��ע������



1. Function description

	/* Briefly describe the project function */
         This routine configures and demonstrates how to modify thread mode privileged access and stack


2. Use environment

	/* Hardware environment: the development hardware platform corresponding to the project */
         Development board: N32G030C8L7-STB V1.0


3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
         SystemClock: 48MHz
         USART: TX - PA9, RX - PA10, baud rate 115200

	/* Describe the test steps and phenomena of the Demo */
         1. After compiling, download the program to reset and run;
         2. You can use the "Cortex Register" window of the compiler to view the stack used in thread mode and the access level of the code (privileged level/unprivileged level);


4. Matters needing attention