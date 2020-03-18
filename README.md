# uart_hub_sonar

本工程使用stm32cubemx 创建

DYP-A02-V2.0 超声波雷达hub



把4个模组的数据整合通过串口1 发送出来，频率50hz



### **串口1 数据格式:**

| 帧头      | data1         | data2         | data3         | data4         | 帧尾      |
| --------- | ------------- | ------------- | ------------- | ------------- | --------- |
| 0xfe 0xef | data_h data_l | data_h data_l | data_h data_l | data_h data_l | 0xee 0xff |

比如超声波1的距离：data_h * 0xff + data_l  
 比如返回 0xfe 0xef 0x07 0xA1 0x00 0x00 0x00 0x00 0x00 0x00 0xee 0xff
 超声波1 的距离 = data_h * data_l =0x07A1  = 0d1935 结果是1953mm
 其他返回00 证明没有超声波或者通讯异常

### **使用开发板 ：**

stm32f103zet6

### **原理图：**

![1584437786661](https://github.com/jinmenglei/uart_hub_sonar/blob/master/res/1584437786661.png)

### **超声波用的这个：**

![1584437593984](https://github.com/jinmenglei/uart_hub_sonar/blob/master/res/1584437593984.png)

### **协议是这个：**

![1584437650467](https://github.com/jinmenglei/uart_hub_sonar/blob/master/res/1584437650467.png)

### **MCU试用的引脚：**

![1584437923255](https://github.com/jinmenglei/uart_hub_sonar/blob/master/res/1584437923255.png)

以上资料均在根目录下
