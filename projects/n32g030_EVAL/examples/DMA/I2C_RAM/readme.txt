1������˵��

    �������ṩ��һ��DMA�÷���������I2C������RAM֮�䴫�����ݡ�  

2��ʹ�û���

    �������������
        IDE���ߣ�KEIL MDK-ARM 5.26
    
    Ӳ��������
        ������ N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    1��ʱ��Դ��HSE+PLL
    2����ʱ�ӣ�48MHz
    3��DMAͨ����DMA_CH5��DMA_CH6
    4��I2C1 ���ã�
            SCL   -->  PB6
            SDA   -->  PB7
            ADDR��0x30(7bit)
            CLOCK��100K
    
    5��I2C2 ���ã�
            SCL   -->  PA6
            SDA   -->  PA7
            ADDR��0x30(7bit)
            CLOCK��100K
    
    6��USART1���ã�
            TX  -->  PA9
            �����ʣ�115200
            ����λ��8bit
            ֹͣλ��1bit
            ��У��

    7�����Բ���������
        a���������ش��븴λ����
        b���Ӵ��ڿ���ӡ��Ϣ����֤���

4��ע������
    ��


1. Function description
    This routine provides a DMA usage for transferring data between I2C peripheral and RAM.

2. Use environment
    Software Development environment:
	IDE tool: KEIL MDK-ARM 5.26
    
    Hardware environment:
	N32G030C8L7-STB V1.0

3. Instructions for use
    1.Clock source: HSE+PLL
    2.Master clock: 48MHz
    3.DMA channels: DMA_CH5, DMA_CH6
    4.I2C1 configuration:
		SCL   -->  PB6
            	SDA   -->  PB7
           	ADDR��0x30(7bit)
            	CLOCK��100K
    5.I2C2 configuration:
            	SCL   -->  PA6
            	SDA   -->  PA7
            	ADDR��0x30(7bit)
            	CLOCK��100K    
    6.USART1 configuration:
            	TX  -->  PA9
		Baud rate: 115200
		Data bit: 8 bits
		Stop bit: 1bit
		No check
            
    7.Test steps and phenomena
	A. Compile download code reset run
	B. View the printed information from the serial port and verify the result

4. Matters needing attention
    None
