1������˵��
    1��TIM3 CH1 CH2 CH3 CH4 �ﵽCCֵ�����ACTIVE��ƽ
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
        2���˿����ã�
                    PA4ѡ��ΪTIM3 CH1���
                    PA7ѡ��ΪTIM3 CH2���
                    PB0ѡ��ΪTIM3 CH3���
                    PB1ѡ��ΪTIM3 CH4���
                    PB7ѡ��ΪIO ���
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM3 CH1 CH2 CH3 CH4�Ĳ���
        2����ʱ�����е�CC1 CC2 CC3 CC4֮�󣬶�Ӧͨ���������ΪActive
4��ע������
    ��

1. Function description
     1. After TIM3 CH1 CH2 CH3 CH4 reaches the CC value, it outputs ACTIVE level
2. Use environment
     Software development environment: KEIL MDK-ARM V5.34.0.0
     Hardware Environment: Developed based on N32G031C8L7_STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM3 CLK=48M
         2. Port configuration:
                     PA4 is selected as TIM3 CH1 output
                     PA7 is selected as TIM3 CH2 output
                     PB0 is selected as TIM3 CH3 output
                     PB1 is selected as TIM3 CH4 output
                     PB7 is selected as IO output
     Instructions:
        1. Open the debug mode after compiling, and observe the waveforms of TIM2 CH1 CH2 CH3 CH4 with an oscilloscope or logic analyzer
        2. After the timer runs to CC1 CC2 CC3 CC4, the output of the corresponding channel becomes Active
4. Matters needing attention
     None