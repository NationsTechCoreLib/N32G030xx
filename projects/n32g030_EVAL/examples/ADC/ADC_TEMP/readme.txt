1������˵��
    1��ADC����ת���ڲ��¶ȴ�������ģ���ѹ����ת��Ϊ�¶�ֵ
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
        4���˿����ã�
                    PA9ѡ��ΪUSART1��TX����
                    PA10ѡ��ΪUSART1��RX����
        5��USART��
                    USART1 115200�����ʡ�8λ����λ��1λֹͣλ������żУ��λ����Ӳ�����ء����ͺͽ���ʹ��
        6�����ܺ�����
                    TempValue = TempCal(ADCConvertedValue)�������¶�ADCԭʼ��ʽ����תΪ�ȵĵ�λ�ĸ�ʽ
    ʹ�÷�����
        1�������򿪵���ģʽ��������ADCConvertedValue,TempValue��ӵ�watch���ڹ۲�
        2�������ڹ������ӵ�PA9���ţ����򿪴��ڽ��չ���
        3��ȫ�����У����Կ����¶ȱ�������ֵ�ڳ����½ӽ�25�����ң�ͬʱ���ڹ�����ʾʵʱоƬ�ڵ��¶�ֵ
4��ע������
    ��ϵͳ����HSEʱ��ʱ��һ��HSIҲ�Ǵ򿪵ģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8)��������ΪHSE����HSI
    ��ϵͳ����HSIʱ��ʱ��һ��HSE�ǹرյģ���RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8)ֻ������ΪHSI



1. Function description
    1. ADC samples and converts the analog voltage of the internal temperature sensor and converts it to a temperature value

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
        4. Port configuration:
                    PA9 is selected as the TX pin of USART1
                    PA10 is selected as the RX pin of USART1
        5. USART:
                    USART1 configuration: 115200 baud rate, 8 data bits, 1 stop bit, no parity bit, no hardware flow control, send and receive enable
        6. Function function:
                    The TempValue = TempCal(ADCConvertedValue) function converts the temperature ADC raw format data into the format of the unit of degree
    Instructions:
        1. Open the debug mode after compiling, add the variables ADCConvertedValue, TempValue to the watch window for observation
        2. Connect the serial port tool to the PA9 pin and open the serial port receiving tool
        3. Running at full speed, you can see that the value of the temperature variable is close to about 25 degrees at room temperature, and the serial port tool displays the temperature value in the real-time chip

4. Matters needing attention
    When the system uses the HSE clock (HSI is generally enabled), ), RCC_ConfigAdc1mClk (RCC_ADC1MCLK_SRC_HSE, RCC_ADC1MCLK_DIV8) can be configured as HSE or HSI
    When the system uses the HSI clock(HSE is generally disabled), RCC_ConfigAdc1mClk(RCC_ADC1MCLK_SRC_HSI, RCC_ADC1MCLK_DIV8) can only be configured as HSI