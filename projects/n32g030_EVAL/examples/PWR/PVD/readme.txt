1������˵��
    1��PVD���õ�ѹ������Ӧ���жϡ�


2��ʹ�û���

    �������������KEIL MDK-ARM V5.25

    Ӳ��������
        1������������N32G030C8L7-STB V1.0����
        2��MCU��N32G030C8L7


3��ʹ��˵��

    ϵͳ���ã�
        1��ʱ��Դ��HSE+PLL

    ʹ�÷�����
        ��KEIL�±������¼�������壬ͨ���������������ģʽ����PVD_IRQHandler()�����öϵ㡣
                ȫ�����С�Ȼ���ٰѵ�ѹ����PVD���õ�ѹ��������ʱ�����ͣ�ڶϵ㴦��


4��ע������
    ��


1. Function description
    1. The PVD configuration voltage generates a corresponding interrupt.


2. Use environment

    Software development environment:
        IDE tool: KEIL MDK-ARM V5.25
      
    Hardware environment:
        Development board: N32G030C8L7-STB V1.0
	MCU��N32G030C8L7


3. Instructions for use

    System Configuration;
        1. Clock source: HSE+PLL

    Instructions:
        After compiling under KEIL, burn it to the evaluation board, enter the debug mode through the emulator, and set a breakpoint in PVD_IRQHandler().
        Running at full speed. Then adjust the voltage to the vicinity of the PVD setting voltage, and the program will stop at the breakpoint at this time.


4. Matters needing attention
    none

