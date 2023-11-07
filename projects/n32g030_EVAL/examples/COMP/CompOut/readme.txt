1������˵��
    1��COMP1�����PA6������INP PA1��INM PA0��Ӱ��
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,COMP CLK=48M
        2���˿����ã�
                    PA1ѡ��Ϊģ�⹦��COMP INP
                    PA0ѡ��Ϊģ�⹦��COMP INM
                    PA6ѡ��Ϊģ�⹦��COMP OUT
                    PA2ѡ��ΪIO���
                    PA3ѡ��ΪIO���
        3��COMP��
                    COMP1����PA1��PA0�����PA6
    ʹ�÷�����
        1�������򿪵���ģʽ����PA2���ӵ�PA1��PA3���ӵ�PA0������ʾ���������߼������ǹ۲�PA6�������
        2����������PA2��ƽ����PA3ʱ��PA6����ߵ�ƽ���෴ʱ������͵�ƽ
4��ע������
    ��


1. Function description
     1. The output PA6 of COMP1 is affected by the input INP PA1 and INM PA0

2. Use environment
     Software development environment: KEIL MDK-ARM V5.30.0.0
     Hardware environment: Developed based on the development board N32G030C8L7-STB V1.0

3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, COMP CLK=48M
         2. Port configuration:
                     PA1 is selected as the analog function, COMP INP
                     PA0 is selected as the analog function, COMP INM
                     PA6 is selected as the analog function, COMP OUT
                     PA2 is selected as IO output
                     PA3 is selected as IO output
         3. COMP:
                     COMP1 input PA1, PA0, output PA6
     Instructions:
         1. After compiling, turn on the debug mode, connect PA2 to PA1, and PA3 to PA0, use an oscilloscope or logic analyzer to observe the output waveform of PA6
         2. When the software output PA2 level is greater than PA3, PA6 output high level, on the contrary, output low level

4. Matters needing attention
   None