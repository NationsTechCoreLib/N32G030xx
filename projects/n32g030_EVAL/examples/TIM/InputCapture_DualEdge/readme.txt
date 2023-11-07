1������˵��
    1��TIM3 CH2���� CH2������,CH1�½��ؼ���Ƶ��
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
        2���жϣ�
                    TIM3 CH2������ CH1�½����жϴ򿪣����ȼ�1
        3���˿����ã�
                    PA7ѡ��ΪTIM3 CH2����
                    PA3ѡ��ΪIO ���
        4��TIM��
                    TIM3 CH2�����أ�CH1�½��ز����жϴ�
    ʹ�÷�����
        1�������򿪵���ģʽ������PA3��PA7��������TIM3Freq��gOnePulsEn��ӵ�watch����
        2��Ĭ��gOnePulsEn=0��ÿ���ֶ���gOnePulsEn=1����ʱ���Կ���TIM3Freq���������Ƶ��ֵ
4��ע������
    ��

1. Function description
    1. TIM3 CH2 pin, CH2 rising edge, CH1 falling edge to calculate the frequency
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for Use
    System configuration��
        1. Clock source:
            HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM3 CLK=48M
        2. Interruption:
            TIM3 CH2 rising edge CH1 falling edge interrupt on, priority 1
        3. Port configuration:
            PA7 is selected TIM3 CH2 Input
            PA3 is selected IO Output
        4. TIM:
            TIM3 CH2 rising edge, CH1 falling edge capture interrupt is turned on
Usage method:
    1. Open debugging mode after compilation, connect PA3 to PA7, add variables TIM3Freq, gOnePulsEn to the watch window
    2. Default gOnePulsEn=0, each time you manually give gOnePulsEn=1, you can see the frequency value calculated by TIM3Freq
4. Matters needing attention
    None