1������˵��
    1��ADC1����ת��PA0 PA1���ŵ�ģ���ѹ
    2�������������һ�Σ��ɼ�һ�εķ�ʽ
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8
        2���˿����ã�
                    PA0ѡ��Ϊģ�⹦��ADCת��ͨ��0
                    PA1ѡ��Ϊģ�⹦��ADCת��ͨ��1
        3��ADC��
                    ADC�������ת����12λ�����Ҷ��룬ת��PA0 PA1��ģ���ѹ����
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADCConvertedValue��ӵ�watch���ڹ۲�
        2��ͨ���ı�PA0 PA1���ŵĵ�ѹ�����Կ���ת���������ͬ���ı�
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI


1. Function description
    1. ADC1 samples and converts the analog voltage of PA0 PA1 pin
    2. Use software to trigger once and collect once

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the development board N32G030C8L7-STB V1.0 

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8
        2. Port configuration:
                    PA0 is selected as analog function, ADC conversion channel 0
                    PA1 is selected as analog function, ADC conversion channel 1
        3. ADC:
                    ADC configuration: software trigger, 12-bit data is right-aligned, and converts the analog voltage data of PA0 PA1
    Instructions:
        1. Open the debug mode after compiling and add the variable ADCConvertedValue to the watch window for observation
        2. By changing the voltage of the PA0 PA1 pin, you can see that the conversion result variable changes synchronously

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI