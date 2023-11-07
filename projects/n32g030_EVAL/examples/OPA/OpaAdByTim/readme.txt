1������˵��
    1��TIM1 CH4����ADCע�����OPA�ĵ�ѹ���ݣ�����TIM1�����COMP1ɲ������
2��ʹ�û���
     �������������KEIL MDK-ARM V5.30.0.0
     Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSE/8,OPA CLK=48M,COMP CLK=48M,TIM1 CLK=48M,TIM8 CLK=48M
        2���жϣ�
                    ADCע���жϴ򿪣����ȼ�0
                    ��ȡת�����
        3���˿����ã�
                    PA0ѡ��Ϊģ�⹦��OPA VP
                    PA6ѡ��Ϊģ�⹦��OPA OUT
                    PA1ѡ��Ϊģ�⹦��COMP1 INP
                    PA4ѡ��Ϊģ�⹦��COMP1 INM
                    PA12ѡ��Ϊģ�⹦��COMP1 OUT    
                    PA8ѡ��ΪTIM1 CH1���
                    PA9ѡ��ΪTIM1 CH2���
                    PA10ѡ��ΪTIM1 CH3���
                    PB13ѡ��ΪTIM1 CH1N���
                    PB14ѡ��ΪTIM1 CH2N���
                    PB15ѡ��ΪTIM1 CH3N���
                    PA6ѡ��ΪADC_CH6ͨ������
        4��OPA��
                    OPA��ѹ���������ܣ�VM������
        5��ADC��
                    ADCע��ģʽ��ɨ��ת����TIM1 CC4������12λ�����Ҷ��룬ע��ת��OPA���ģ���ѹ����
        6��COMP��
                    COMP1 INPѡ��PA1��INMѡ��PA4���������TIM1��TIM8ɲ��
        7��TIM��
                    TIM1 6·�����򿪣�ɲ��ʹ���Ҵ��жϣ�CH4�������
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1��������κ�ADC��ȡ�Ĳɼ�����
        2���ı�COMP1 �����״̬����ɲ��TIM1���ı�OPA�������ѹ���Ըı�ADC��ȡ������
4��ע������
    ��


1. Function description
    1. TIM1 CH4 triggers ADC to inject the voltage data of sampled OPA, and TIM1 output is controlled by COMP1 brake
2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware Environment: Developed based on the development board N32G030C8L7-STB V1.0
3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSE/8,
                    OPA CLK=48M, COMP CLK=48M, TIM1 CLK=48M, TIM8 CLK=48M
        2. Interrupt:
                     Enable the ADC injection interrupt, priority 0
                     Read conversion result
        3. Port configuration:
                    PA0 is selected as analog function, OPA VP
                    PA6 is selected as analog function, OPA OUT
                    PA1 is selected as analog function, COMP1 INP
                    PA4 is selected as analog function, COMP1 INM
                    PA12 is selected as analog function, COMP1 OUT
                    PA8 is selected as TIM1 CH1 output
                    PA9 is selected as TIM1 CH2 output
                    PA10 is selected as TIM1 CH3 output
                    PB13 is selected as TIM1 CH1 output
                    PB14 is selected as TIM1 CH2 output
                    PB15 is selected as TIM1 CH3 output
                    PA6 is selected as ADC_CH6 channel input
        4. OPA:
                    OPA voltage follower function, VM no pins
        5. ADC:
                    ADC injection mode, scan conversion, TIM1 CC4 trigger, 12-bit data right-justified, injection conversion OPA output analog voltage data
        6. TIM:
                    TIM1 6-channel complementary open, brake enable and open interrupt, CH4 trigger output
    Instructions:
        1. After compiling, open the debug mode, and use an oscilloscope or logic analyzer to observe the output waveform of TIM1 and the acquired data read by the ADC
        2. Changing the output state of COMP1 can brake TIM1, and changing the input voltage of OPA can change the data read by ADC
4. Matters needing attention
   None