1������˵��
    1��ADC������ת��PA1���ŵ�ģ���ѹ
    2������ADCת�����ͨ��DMA_CH1ͨ����ȡ������ADCConvertedValue
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8,DMA CLK=48M
        2���˿����ã�
                    PA1ѡ��Ϊģ�⹦��ADCת��ͨ��1
        3��DMA��
                    DMA_CH1ͨ��ѭ��ģʽ����һ�����ֵ�ADCת�������ADCConvertedValue����
        4��ADC��
                    ADC����ת����ɨ��ģʽ�����������12λ�����Ҷ��룬ת��ͨ��1��PA1��ģ���ѹ����
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADCConvertedValue��ӵ�watch���ڹ۲�
        2��ͨ���ı�PA1���ŵĵ�ѹ�����Կ���ת���������ͬ���ı�
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI



1. Function description
    1. ADC samples and converts the analog voltage of the PA1 pin
    2. The ADC conversion result is read to the variable ADCConvertedValue through the DMA_CH1 channel

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the development board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8, DMA CLK=48M
        2. Port configuration:
                    PA1 is selected as analog function, ADC conversion channel 1
        3. DMA:
                    DMA1_CH1 channel is configuered as circular mode, carries a half-word ADC conversion result to ADCConvertedValue variable
        4. ADC:
                    ADC configuration: continuous conversion, scan mode, software trigger, 12-bit data right-aligned, conversion channel 1 is the analog voltage data of PA1
    Instructions:
        1. Open the debug mode after compiling and add the variable ADCConvertedValue to the watch window for observation
        2. By changing the voltage of the PA1 pin, you can see that the conversion result variable changes synchronously

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI