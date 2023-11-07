1������˵��
    1��OPA PGAģʽ���Ŵ������ѹ2��
2��ʹ�û���
     �������������KEIL MDK-ARM V5.30.0.0
     Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,OPA CLK=48M
        2���˿����ã�
                    PA1ѡ��Ϊģ�⹦��OPA VP
                    PA6ѡ��Ϊģ�⹦��OPA OUT
        3��OPA��
                    OPA PGA���ܣ�����2��
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ�����۲�OPA����������
        2��OPA���=2*OPA����
4��ע������
     ��


1. Function description
    1. OPA PGA mode, amplifies the input voltage by 2 times
2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware Environment: Developed based on the development board N32G030C8L7-STB V1.0
3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,OPA CLK=48M
        2. Port configuration:
                    PA1 is selected as analog function, OPA VP
                    PA6 is selected as analog function, OPA OUT
        3. OPA:
                    OPA PGA function, 2x magnification
    Instructions:
        1. Open the debug mode after compiling, and observe the input and output of the OPA with an oscilloscope
        2. OPA output = 2*OPA input
4. Matters needing attention
   None