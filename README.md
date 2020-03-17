# uart_hub_sonar

DYP-A02-V2.0 超声波雷达hub



把4个模组的数据整合通过串口1 发送出来



### **串口1 数据格式:**

| 帧头      | data1         | data2         | data3         | data4         | 帧尾      |
| --------- | ------------- | ------------- | ------------- | ------------- | --------- |
| 0xfe 0xef | data_h data_l | data_h data_l | data_h data_l | data_h data_l | 0xee 0xff |

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
