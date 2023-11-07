1������˵��
    1��ADC�������PA5���Զ�ע�����PA4���ŵ�ģ���ѹ����TIM1 CC2�¼��´�������
    2�����й���ת�����ͨ��DMA_CH1ͨ����ȡ������ADC_RegularConvertedValueTab[32]����
           ע��ת�����ͨ��ת�������ж϶�ȡ������ADC_InjectedConvertedValueTab[32]����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,ADC CLK=48M/16,ADC 1M CLK=HSI/8,DMA CLK=48M
        2���жϣ�
                    ADCע��ת���������жϴ�, �����ȼ�0
                    �жϺ����н�ע������ȡ��ADC_InjectedConvertedValueTab[32]���飬����תPA6��ƽ
        3���˿����ã�
                    PA4ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA5ѡ��Ϊģ�⹦��ADCת��ͨ��
                    PA6ѡ��Ϊͨ��IO���
                    PA9ѡ��ΪTIM1 CH2 PWM���
        4��DMA��
                    DMA_CH1ͨ��ѭ��ģʽ����32�����ֵ�ADC1ת�������ADC_RegularConvertedValueTab[32]����
        5��ADC��
                    ADC TIM1 CC2������12λ�����Ҷ��룬����ת��ͨ��PA5���Զ�ע��ת��ͨ��PA4��ģ���ѹ����
        6��TIM��
                    TIM1����CH2�����CH2��������ADCת��        
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADC_RegularConvertedValueTab[32],ADC_InjectedConvertedValueTab[32]��ӵ�watch���ڹ۲�
        2��ͨ���ı�PA4 PA5���ŵĵ�ѹ����ÿ��CC2�¼�����ʱת��һ�ι����ע��ͨ�������������ڶ�Ӧ�����С�ͬʱ��PA9 ���Կ���TIM1 CH2�� PWM ����
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI


1. Function description
    1. The ADC regularly samples PA5, automatically injects and samples the analog voltage of the PA4 pin, and triggers sampling under the TIM1 CC2 event
    2. The regular conversion result is read into the variable ADC_RegularConvertedValueTab[32] array through the DMA_CH1 channel
           The result of the injection conversion is read into the variable ADC_InjectedConvertedValueTab[32] array through the conversion end interrupt

2. Use environment
    Software development environment: KEIL MDK-ARM V5.30.0.0
    Hardware environment: Developed based on the development board N32G030C8L7-STB V1.0

3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, ADC CLK=48M/16, ADC 1M CLK=HSI/8, DMA CLK=48M
        2. Interrupt:
                    ADC injection conversion result complete interrupt is turned on, interrupt priority is 0
                    In the interrupt function, the injection result is read into the ADC_InjectedConvertedValueTab[32] array, and the PA6 level is flipped
        3. Port configuration:
                    PA4 is selected as the analog function, ADC conversion channel
                    PA5 is selected as the analog function, ADC conversion channel
                    PA6 is selected as general IO output
                    PA9 is selected as TIM1 CH2 PWM output
        4. DMA:
                    DMA1_CH1 channel is configuered as circular mode,carries 32 half-word ADC1 conversion results to ADC_RegularConvertedValueTab[32] array
        5. ADC:
                    ADC configuration: TIM1 CC2 trigger, 12-bit data right-aligned, regular conversion channel PA5, automatic injection of analog voltage data of conversion channel PA4
        6. TIM:
                    TIM1 turns on CH2 output, and CH2 is used to trigger ADC conversion
    Instructions:
        1. Open the debug mode after compiling and add the variables ADC_RegularConvertedValueTab[32], ADC_InjectedConvertedValueTab[32] to the watch window for observation
        2. By changing the voltage of the PA4 PA5 pin, the rule and injection channel are converted once every CC2 event occurs, and the variables are stored in the corresponding array. At the same time, you can see the PWM waveform of TIM1 CH2 on PA9

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI