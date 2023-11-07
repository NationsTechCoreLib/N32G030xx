1������˵��
    1��ADC����ͨ������PA4��PA5���ŵ�ģ���ѹ��ע��ͨ������PA0��PA1���ŵ�ģ���ѹ
    2�����й���ת�����ͨ��DMA_CH1ͨ����ȡ������ADC_RegularConvertedValueTab[64]����
           ע��ת�����ͨ��ת�������ж϶�ȡ������ADC_InjectedConvertedValueTab[32]����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ������N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8,DMA CLK=48M
        2���жϣ�
                    ADCע��ת���������жϴ򿪣����ȼ�0
                    �жϴ������ע��ת�������ADC_InjectedConvertedValueTab[32]����
        3���˿����ã�
                    PA4ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA5ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA0ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA1ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA9ѡ��Ϊ�ⲿEXTI�¼������ش���
                    PA10ѡ��Ϊ�ⲿEXTI�¼������ش���
        4��DMA��
                    DMA_CH1ͨ��ѭ��ģʽ����64�����ֵ�ADC����ͨ��ת�������ADC_RegularConvertedValueTab[64]����
        5��ADC��
                    ADC����ͨ��ɨ����ģʽ��EXTI9������12λ�����Ҷ��룬ת��ͨ��PA4��PA5��ģ���ѹ����
                    ADCע��ͨ��ɨ��ģʽ��EXTI10������12λ�����Ҷ��룬ת��ͨ��PA0��PA1��ģ���ѹ����
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADC_RegularConvertedValueTab[64],ADC_InjectedConvertedValueTab[32]��ӵ�watch���ڹ۲�
        2��ͨ��PA9�������ؿ��Դ�������ͨ�����ݲ�����PA10�������ؿ��Դ���ע��ͨ�����ݲ���
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI


1. Function description
    1. The ADC regular channel samples the analog voltage of the PA4 and PA5 pins, and the injection channel samples the analog voltage of the PA0 and PA1 pins.
    2. The regular conversion result is read into the variable ADC_RegularConvertedValueTab[64] array through the DMA_CH1 channel
           The result of the injection conversion is read into the variable ADC_InjectedConvertedValueTab[32] array through the conversion end interrupt

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the development board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8, DMA CLK=48M
        2. Interrupt:
                    ADC injection conversion result completion interrupt is turned on, priority level 0
                    Interrupt handling receives the injected conversion result into the ADC_InjectedConvertedValueTab[32] array
        3. Port configuration:
                    PA4 is selected as the analog function, ADC conversion channel
                    PA5 is selected as the analog function, ADC conversion channel
                    PA0 is selected as the analog function, ADC conversion channel
                    PA1 is selected as the analog function, ADC conversion channel
                    PA9 is selected as external EXTI event rising edge trigger
                    PA10 is selected as external EXTI event rising edge trigger
        4. DMA:
                    DMA1_CH1 channel is configured as circular mode, carries 64 half-word ADC regular channel conversion results to ADC_RegularConvertedValueTab[64] array
        5. ADC:
                    ADC regular channel scan discontinuous mode, EXTI9 trigger, 12-bit data right-aligned, conversion of analog voltage data of channels PA4 and PA5
                    ADC injection channel scan mode, EXTI10 trigger, 12-bit data right-aligned, conversion of analog voltage data of channels PA0 and PA1
    Instructions:
        1. Open the debug mode after compiling, add the variables ADC_RegularConvertedValueTab[64], ADC_InjectedConvertedValueTab[32] to the watch window for observation
        2. The regular channel data sampling can be triggered by the rising edge of PA9, and the data sampling of the injected channel can be triggered by the rising edge of PA10.

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI