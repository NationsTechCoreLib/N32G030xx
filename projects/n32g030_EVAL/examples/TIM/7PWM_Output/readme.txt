1������˵��
    1��TIM1��TIM8���3·�������κ�һ·CH4����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ����:
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M,TIM8 CLK=48M
        2���˿����ã�
                    PA8ѡ��ΪTIM1 CH1���
                    PA9ѡ��ΪTIM1 CH2���
                    PA10ѡ��ΪTIM1 CH3���
                    PB13ѡ��ΪTIM1 CH1N���
                    PB14ѡ��ΪTIM1 CH2N���
                    PB15ѡ��ΪTIM1 CH3N���
                    PA11ѡ��ΪTIM1 CH4���
                    PA0ѡ��ΪTIM8 CH1���
                    PA1ѡ��ΪTIM8 CH2���
                    PA2ѡ��ΪTIM8 CH3���
                    PB6ѡ��ΪTIM8 CH1N���
                    PB7ѡ��ΪTIM8 CH2N���
                    PB5ѡ��ΪTIM8 CH3N���
                    PA3ѡ��ΪTIM8 CH4���
        3��TIM��
                    TIM1 6·�������,CH4���
                    TIM8 6·�������,CH4���
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1 TIM8���������
        2���������TIM1 3·������һ·CH4��TIM8 3·������һ·CH4
4��ע������
       ������Ĭ��PA9��PA10��ñ�ӵ�NSLINK�����⴮�ڣ���������PA9��PA10�������ڣ�����������;����ε�������ñ��

1. Function description
    1. TIM1 and TIM8 output 3 complementary waveforms and 1 CH4 waveform
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for Use
    System configuration;
        1. Clock source:
            HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM1 CLK=48M, TIM8 CLK=48M
        2. Port configuration:
                    PA8 is selected as TIM1 CH1 output
                    PA9 is selected as TIM1 CH2 output
                    PA10 is selected as TIM1 CH3 output
                    PB13 is selected as TIM1 CH1N output
                    PB14 is selected as TIM1 CH2N output
                    PB15 is selected as TIM1 CH3N output
                    PA11 is selected as TIM1 CH4 output
                    PA0 is selected as TIM8 CH1 output
                    PA1 is selected as TIM8 CH2 output
                    PA2 is selected as TIM8 CH3 output
                    PB6 is selected as TIM8 CH1N output
                    PB7 is selected as TIM8 CH2N output
                    PB5 is selected as TIM8 CH3N output
                    PA3 is selected as TIM8 CH4 output
        3. TIM:
            TIM1 6 complementary outputs, CH4 output
            TIM8 6 complementary outputs, CH4 output
    Instructions:
        1. Open debugging mode after compilation and use an oscilloscope or logic analyzer to observe the output waveform of TIM1 TIM8
        2. Output waveform TIM1 3-way complementary plus one CH4, TIM8 3-way complementary plus one CH4
4. Matters needing attention
       By default, the PA9 and PA10 jumper caps of the development board are connected to the virtual serial port of NSLINK. If PA9 and PA10 are not used as serial ports in the project, and are used for other purposes, the serial port jumper caps must be unplugged.
