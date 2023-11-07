1������˵��
    1��TIM3 ����CH1 CH2 CH3 CH4 CCֵ������ʱ�жϣ���תIO��ƽ
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.34.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
            HSE=8M,PLL=48M,AHB=48M,APB1=12M,APB2=48M,TIM3 CLK=24M
        2���жϣ�
            TIM3 �Ƚ��жϴ򿪣����ȼ�1
        3���˿����ã�
                    PA6ѡ��ΪIO���
                    PA7ѡ��ΪIO���
                    PA8ѡ��ΪIO���
                    PA9ѡ��ΪIO���
        4��TIM��
                    TIM3�������ģʽ��CH1 CH2 CH3 CH4�Ƚ�ֵ�����ж�
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�PA6��PA7��PA8��PA9�Ĳ���
        2���������к󣬶�Ӧͨ���ﵽ�Ƚ�ֵ�󣬱Ƚ�ֵ�ۼӲ���ת��ӦIO�ڵ�ƽ
4��ע������
   ������Ĭ��PA9,PA10��ñ�ӵ�NSLINK�����⴮�ڣ���������PA9��PA10�������ڣ�����������;����ε�������ñ��

1. Function description
     1. TIM3 uses the CH1 CH2 CH3 CH4 CC value to generate a timing interrupt and flip the IO level
2. Use environment
     Software development environment: KEIL MDK-ARM V5.34.0.0
     Hardware Environment: Developed based on N32G031C8L7-STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
             HSE=8M, PLL=48M, AHB=48M, APB1=12M, APB2=48M, TIM3 CLK=24M
         2. Interruption:
             TIM3 compare interrupt is turned on, priority level 1
         3. Port configuration:
                     PA6 is selected as IO output
                     PA7 is selected as IO output
                     PA8 is selected as IO output
                     PA9 is selected as IO output
         4. TIM:
                     TIM3 output freeze mode, CH1 CH2 CH3 CH4 compare value interrupt
     Instructions:
         1. Open the debug mode after compiling, and observe the waveform of PA6,PA7,PA8,PA9 with an oscilloscope or logic analyzer
         2. After the program runs, after the corresponding channel reaches the comparison value, the comparison value accumulates and flips the corresponding IO port level
Matters needing attention
     None