# LilyGo-EPD47-HC08-PDM_MIC
这是一个关于测试 HC08-PDM_MIC 低功耗蓝牙模组的Dome.  

### 一、代码简介
将 HC08-PDM_MIC 模组安装于一块 LilyGo-EPD47 水墨屏上并将其休眠,通过另外一块 ESP32 随时唤醒正在休眠的 LilyGo-EPD47 发送需要显示的字符文本,并使其进入麦克风检测,当检测到有声音后再次进入休眠.通过定义的按钮可重复以上测试步骤.  
  
### 二、硬件准备
1、HC08-PDM_MIC 蓝牙模组
2、USB 转 TTL 串口模块
3、LilyGo-EPD47
4、ESP32 开发板
5、FPC排线 6 Pin  
  
！[Hardware display](LilyGo-EPD47/images/1.jpg)  
  
### 三、HC08 AT设置
1、HC08 连接 USB 转 TTL 串口模块  
  
+---------------------+   
|HC08-------USB_to_TTL|  
|TX-----------------RX|  
|RX-----------------TX|  
|VCC--------------3.3V|  
|GND---------------GND|  
+---------------------+  
  
2、发送AT指令设置蓝牙模组  
AT+LED=0           //关闭LED灯，设置成功收到返回字符：OK+LED=0  
AT+NAME = INK_047  //蓝牙名称，设置成功收到返回字符：OKsetNAME:INK_047  
AT+MODE = 1        //一级节能模式（必要），设置成功收到返回字符：OK  
  
！[HC08-ATset](LilyGo-EPD47/images/ATset.jpg)  
  
### 四、在 LilyGo-EPD47 上安装 HC08-PDM_MIC 模组
！[HC08install](LilyGo-EPD47/images/2.jpg)
（注意：必须断电操作，否则有可能烧坏水墨屏ESP32模组）  
  
### 五、

