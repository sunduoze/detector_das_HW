# detector_das_HW
detector_das 硬件设计
![main](https://github.com/sunduoze/detector_das_HW/assets/10105111/8184c166-6098-4a4d-a5ee-98370dadf463)

### 硬件架构
![image](https://github.com/sunduoze/detector_das_HW/assets/10105111/28328ea6-011d-45d7-a304-4205b7205af9)


整个系统在ADI的EVAL-AD7606CFMCZ 评估套件 | 亚德诺半导体 (analog.com)评估板的基础上开发控制、交互、物联以及检测器接口部分来实现整个系统的硬件部分。
整个系统使用ESP32作为控制核心，采用TYPE-C接口供电和烧录（及串口通讯），使用Type-C控制器与适配器进行cc通讯实现PD充电，切换为20V电压输入，通过使用螺旋编码按键、OLED、蜂鸣器进行简单的硬件端UI交互。使用数字电位器控制可调输出的高性能电压源Vs1为TCD供电，通过DC/DC降压到5.6V的Vs2为EVAL-AD7606C、PID及DID供电，AD7606C的6个通道分别采集TCD、PID、DID、Vs1、Vs2、VBUS（20V）信号或电压，剩余的2个通道预留为辅助电压测量（可配置最大为±20V的差分输入范围）和电流测量（0.1-9.8A）功能。
