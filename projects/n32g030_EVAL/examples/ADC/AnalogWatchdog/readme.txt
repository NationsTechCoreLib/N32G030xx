1������˵��
    1��ADC����ת��PA4���ŵ�ģ���ѹ���������ģ�⿴�Ź��������ֵ��Χ���������жϳ���
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8
        2��ADC��
                    ADC����ת�������������12λ�����Ҷ��룬ת��PA4���ŵ�ģ���ѹ����
        3���˿����ã�
                    PA4ѡ��Ϊģ�⹦��ADCת��ͨ��4
        4���жϣ�
                    ADCģ�⿴�Ź��жϴ򿪣����ȼ�0
    ʹ�÷�����
        1�������򿪵���ģʽ��������gCntAwdg��ӵ�watch���ڹ۲�
        2���ı�PA4���ŵ�ѹֵ������ѹֵ����ģ�⿴�Ź������0x300����0.6V����0xB00����2.26V����Χ�⣬�����һ���жϣ��������ۼӲ���
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI

1. Function description
    1. ADC samples and converts the analog voltage of the PA4 pin. If it exceeds the threshold range defined by the analog watchdog, then jump into the interrupt program

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: DDeveloped based on the development board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8
        2. ADC:
                    ADC configuration: continuous conversion, software trigger, 12-bit data right-aligned, conversion of analog voltage data of PA4 pin
        3. Port configuration:
                    PA4 is selected as analog function, ADC conversion channel 4
        4. Interrupt:
                    ADC analog watchdog interrupt is turned on, priority 0
    Instructions:
        1. Open the debug mode after compiling and add the variable gCntAwdg to the watch window for observation
        2. Change the voltage value of the PA4 pin. When the voltage value exceeds the range defined by the analog watchdog from 0x300 (ie 0.6V) to 0xB00 (ie 2.26V), an interrupt is entered, and the variable is accumulated

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI