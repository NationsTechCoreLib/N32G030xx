1������˵��
    TIM6 ���ø����жϣ�������ʱ��תIO
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM6 CLK=48M
        2���жϣ�
                    TIM6 �����жϴ򿪣����ȼ�1
        3���˿����ã�
                    PA6ѡ��ΪIO���
                    PA7ѡ��ΪIO���
                    PA8ѡ��ΪIO���
                    PA9ѡ��ΪIO���
        4��TIM��
                    TIM6ʹ�������ж�
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�PA6�Ĳ���
        2���������к�TIM6�������ж����ٷ�תPA6��ƽ
4��ע������
    ��

1. Function description
     1. TIM6 uses the update interrupt to generate timing rollover IO
2. Use environment
     Software development environment: KEIL MDK-ARM V5.34.0.0
     Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM6 CLK=48M
         2. Interruption:
                     TIM6 update interrupt is turned on, priority level 1
         3. Port configuration:
                     PA6 is selected as IO output
                     PA7 is selected as IO output
                     PA8 is selected as IO output
                     PA9 is selected as IO output
         4. TIM:
                     TIM6 enables periodic interrupts
     Instructions:
         1. After compiling, turn on the debug mode, and use an oscilloscope or logic analyzer to observe the PA6 waveform
         2. After the program is running, the periodic interrupt of TIM6 comes to reverse the level of PA6
4. Matters needing attention
     None