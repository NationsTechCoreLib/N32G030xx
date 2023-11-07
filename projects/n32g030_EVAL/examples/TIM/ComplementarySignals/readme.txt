1������˵��
    1��TIM1���3·��������
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ����:
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M
        2���˿����ã�
                    PA8ѡ��ΪTIM1 CH1���
                    PA9ѡ��ΪTIM1 CH2���
                    PA10ѡ��ΪTIM1 CH3���
                    PB13ѡ��ΪTIM1 CH1N���
                    PB14ѡ��ΪTIM1 CH2N���
                    PB15ѡ��ΪTIM1 CH3N���
                    PB12ѡ��ΪTIM1 Breakin����
        3��TIM��
                    TIM1 6·��������������IOMɲ��
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1�Ĳ���
        2���ɹ۲쵽3·�������Σ�PB12����Ϊ�߿ɹر����
4��ע������
       ������Ĭ��PA9,PA10��ñ�ӵ�NSLINK�����⴮�ڣ���������PA9��PA10�������ڣ�����������;����ε�������ñ��

1. Function description
    1. TIM1 output 3 complementary waveforms
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for use
    System configuration:
        1. Clock source:
            HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM1 CLK=48M
        2. Port configuration:
                     PA8 is selected as TIM1 CH1 output
                     PA9 is selected as TIM1 CH2 output
                     PA10 is selected as TIM1 CH3 output
                     PB13 is selected as TIM1 CH1N output
                     PB14 is selected as TIM1 CH2N output
                     PB15 is selected as TIM1 CH3N output
                     PB12 is selected as TIM1 Breakin input
        3. TIM:
            TIM1 6 Complementary with dead-time, with IOM Brake
    Instructions:
        1. Open debugging mode after compilation and observe TIM1 waveform with oscilloscope or logic analyzer
        2. 3 complementary waveforms can be observed, and the output of PB12 pin can be turned off when the pin is high
4. Matters needing attention
    By default, the PA9 and PA10 jumper caps of the development board are connected to the virtual serial port of NSLINK. If PA9 and PA10 are not used as serial ports in the project, and are used for other purposes, the serial port jumper caps must be unplugged.
