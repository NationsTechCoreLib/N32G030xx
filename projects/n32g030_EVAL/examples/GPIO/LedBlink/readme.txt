1������˵��

	1��������չʾ IO ���� LED ��˸


2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
        IDE���ߣ�KEIL MDK-ARM 5.21.1.0

        /* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
        �����壺N32G030CL-STB V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
        1��SystemClock��48MHz
        2��GPIO��PB1��PB6��PB7 ���� LED(D1��D2��D3) ��˸

	/* ����Demo�Ĳ��Բ�������� */
        1.��������س���λ���У�
        2. LED(D1��D2��D3) ��˸��

4��ע������
    ��


1. Function description
    1. This routine shows the IO control LED blinking
2. Use environment
    /* Software development environment: the name and version number of the software tool used in the current project */
    Software development environment: 
    	KEIL MDK-ARM 5.21.1.0
    /* Hardware environment: the development hardware platform corresponding to the project */
    Hardware Environment: 
    	Developed based on N32G030CL-STB V1.0
3. Instructions for use
    System Configuration;
        1. SystemClock��48MHz
        2. GPIO: PB1, PB6, PB7 control LED (D1, D2, D3) to blink
    Instructions:
        1. After compiling, download the program to reset and run
        2. LED (D1, D2, D3) to blinking
4. Matters needing attention
    No