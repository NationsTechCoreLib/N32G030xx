1������˵��
    1��SQRTִ��һ�ο�����������ж�����ͨ�����ڷ����̺�����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.26.2.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,SQRT CLK=48M
        2���˿����ã�
                            PA9ѡ��Ϊ�������
                    PA10ѡ��Ϊ��������
        3��HDIV��
                    SQRT�жϴ����ȼ�0������ 123456�����Ľ��
    ʹ�÷�����
        1�������򿪵���ģʽ��������SQRT�ļĴ�����
        2������ִ�к󣬿��Կ��������Ľ��Ϊ351��ͬʱ����Ҳ���ӡ�����Ϣ
4��ע������
    ��


1. Function description
     1. SQRT executes a square root, and sends the quotient and remainder through the serial port in the completion interrupt
2. Use environment
     Software development environment: KEIL KEIL MDK-ARM V5.26.2.0
     Hardware Environment: Developed based on N32G030C8L7-STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,SQRT CLK=48M
         2. Port configuration:
                     PA9 is selected as serial output
                     PA10 is selected as serial input
         3. HDIV:
                     SQRT interrupt open priority 0, calculate the result of 123456 square root
     Instructions:
         1. Open the debug mode after compiling, and open the register of the variable SQRT
         2. After the program is executed, you can see that the result of the square is 351, and the serial port will also print relevant information
4. Matters needing attention
     none