1������˵��
    1��COMP1�����ɲ��TIM1 �Ļ����źţ�COMP OUT��ͺ�ָ�TIM1 ����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,COMP CLK=48M,TIM1 CLK=48M
        2���˿����ã�
                    PA1ѡ��Ϊģ�⹦��COMP INP
                    PA0ѡ��Ϊģ�⹦��COMP INM
                    PA6ѡ��Ϊģ�⹦��COMP OUT
                    PA2ѡ��ΪIO���
                    PA3ѡ��ΪIO���
                    PA8ѡ��ΪTIM1 CH1���
                    PA9ѡ��ΪTIM1 CH2���
                    PA10ѡ��ΪTIM1 CH3���
                    PB13ѡ��ΪTIM1 CH1N���
                    PB14ѡ��ΪTIM1 CH2N���
                    PB15ѡ��ΪTIM1 CH3N���
        3��TIM��
                    TIM1����CH1 CH2 CH3 CH1N CH2N CH3N���,COMP��Ϊɲ������
        4��COMP��
                    COMP1�������TIM1 ɲ���������ʱ�ָ�TIM1 ���
    ʹ�÷�����
        1�������򿪵���ģʽ����PA2���ӵ�PA1��PA3���ӵ�PA0������ʾ���������߼������ǹ۲�TIM1�������
        2����������PA2��ƽ����PA3ʱ��TIM������ʧ���෴ʱ�������������
4��ע������
    ��



1. Function description
    1. The output of COMP1 brakes the complementary signal of TIM1, and the waveform of TIM1 is restored after COMP OUT goes low.

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the evaluation board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, COMP CLK=48M, TIM1 CLK=48M
        2. Port configuration:
                    PA1 is selected as the analog function, COMP INP
                    PA0 is selected as the analog function, COMP INM
                    PA6 is selected as the analog function, COMP OUT
                    PA2 is selected as IO output
                    PA3 is selected as IO output
                    PA8 is selected as TIM1 CH1 output
                    PA9 is selected as TIM1 CH2 output
                    PA10 is selected as TIM1 CH3 output
                    PB13 is selected as TIM1 CH1N output
                    PB14 is selected as TIM1 CH2N output
                    PB15 is selected as TIM1 CH3N output
        3. TIM:
                    TIM1 turns on CH1 CH2 CH3 CH1N CH2N CH3N output, COMP is used as brake input
        4. COMP:
                    COMP1 output triggers TIM1 brake, and resumes TIM1 output when there is no output
    Instructions:
        1. Open the debug mode after compiling, connect PA2 to PA1 and PA3 to PA0, use an oscilloscope or logic analyzer to observe the output waveform of TIM1
        2. When the software output PA2 level is greater than PA3, the TIM waveform disappears, on the contrary, the waveform is output normally

4. Matters needing attention
   None