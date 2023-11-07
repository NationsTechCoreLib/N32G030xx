1������˵��
    1��ADC�����ڲ�ͨ��Vrefint
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8,DMA CLK=48M
        2��DMA��
                    DMA_CH1ͨ��ѭ��ģʽ����һ�����ֵ�ADCת�������ADCConvertedValue����
        3��ADC��
                    ADC����ת�������������12λ�����Ҷ��룬ת��ͨ��16���ڲ��¶ȴ�������ģ���ѹ����
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADCConvertedValue,��ӵ�watch���ڹ۲죬���ֵ����Vrefint�Ĳ���ֵ
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI



1. Function description
    1. ADC samples the internal channel Vrefint

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the evaluation board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8, DMA CLK=48M
        2. DMA:
                    DMA1_CH1 channel is configuered as circular mode, carries a half-word ADC conversion result to ADCConvertedValue variable
        3. ADC:
                    ADC configuration: continuous conversion, software trigger, 12-bit data right-aligned, conversion channel 16 is the analog voltage data of the internal temperature sensor
    Instructions:
        1. Open the debug mode after compiling, add the variables ADCConvertedValue to the watch window for observation��This value is the Vrefint sample value
4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI