1������˵��
    1��LP RUNģʽ�Ľ�����˳���


2��ʹ�û���

    �������������KEIL MDK-ARM V5.25

    Ӳ��������
        1������������N32G030C8L7-STB V1.0����
	2��MCU��N32G030C8L7


3��ʹ��˵��

    ϵͳ���ã�
        1��ʱ��Դ��HSE+PLL/LSE
        2��ʱ��Ƶ�ʣ�48M/4M


    ʹ�÷�����
        ��KEIL�±������¼�������壬���ӵ������ϵ���һ�ᣬ�������Ա�С���ֹ�һ������ֱ��
        ѭ��������
            


4��ע������
    ������LP RUNģʽʱ��ϵͳʱ���л�����LSE/LSI�����˳�ʱ����Ҫ�л��û�Ĭ��ϵͳʱ��


1. Function description
    1. Entry and exit of LP RUN mode.


2. Use environment

    Software development environment:
        IDE tool: KEIL MDK-ARM V5.25
      
    Hardware environment:
        Development board: N32G030C8L7-STB V1.0
	MCU: N32G030C8L7


3. Instructions for use

    System Configuration;
        1. Clock source: HSE+PLL/LSE
        2. Clock frequency: 48M/4M

    Instructions:
        After compiling under KEIL, it is burned to the evaluation board, and the ammeter is connected in series. After a while, the current becomes significantly smaller. After a while the current increases again.
        Cycle back and forth, check the print information to see entering and exiting the LP RUN mode.
            
4. Matters needing attention
    When entering LP RUN mode, the system clock is switched to LSE/LSI, and when exiting, it needs to switch back to the user default system clock

