1������˵��
    1��TIM3 CH1 CH2 CH3 CH4 �ﵽCCֵ�󣬶�Ӧ����PA6 PA7 PA8 PA9��IO��ƽ
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
        2���жϣ�
                    TIM3 �Ƚ��жϴ�,���ȼ�1
        3���˿����ã�
                    PA6ѡ��ΪIO ���
                    PA7ѡ��ΪIO ���
                    PA8ѡ��ΪIO ���
                    PA9ѡ��ΪIO ���
        4��TIM��
                    TIM3 ���ú�CH1 CH2 CH3 CH4�ıȽ�ֵ�����򿪱Ƚ��ж�
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�PA6 PA7 PA8 PA9�Ĳ���
        2����ʱ���˽���CC1 CC2 CC3 CC4�жϺ�,��Ӧ����PA6 PA7 PA8 PA9��IO
4��ע������
       ������Ĭ��PA9,PA10��ñ�ӵ�NSLINK�����⴮�ڣ���������PA9��PA10�������ڣ�����������;����ε�������ñ��

Function Description
     1. After TIM3 CH1 CH2 CH3 CH4 reaches the CC value, pull down the IO level of PA6 PA7 PA8 PA9 correspondingly.
2. Use environment
     Software development environment: KEIL MDK-ARM V5.34.0.0
     Hardware Environment: Developed based on N32G031C8L7_STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
         2. Interruption:
                    TIM3 compare interrupt is turned on, subpriority 1
         3. Port configuration:
                     PA6 is selected as IO output
                     PA7 is selected as IO output
                     PA8 is selected as IO output
                     PA9 is selected as IO output
         4. TIM:
                    TIM3 configures the comparison value of CH1, CH2, CH3, CH4, and turns on the comparison interrupt
     Instructions:
         1. Open the debug mode after compiling, and observe the waveforms of PA6 PA7 PA8 PA9 with an oscilloscope or logic analyzer
         2. After the timer runs to CC1 CC2 CC3 CC4, pull down the IO level of PA6 PA7 PA8 PA9 correspondingly
4. Matters needing attention
    By default, the PA9 and PA10 jumper caps of the development board are connected to the virtual serial port of NSLINK. If PA9 and PA10 are not used as serial ports in the project, and are used for other purposes, the serial port jumper caps must be unplugged.
