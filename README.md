# AHT20
Harmony OS 的 AHT20 温湿度传感器库



**功能简介**：

* 使用Harmony OS的IoT硬件接口;
* 接口简洁易于使用、易于移植;
* 内置了测试程序，可直接进行测试;



**API接口**：

```c
uint32_t AHT20_Calibrate(void); // 校准，成功返回0

uint32_t AHT20_StartMeasure(void); // 触发测量，成功返回0

uint32_t AHT20_GetMeasureResult(float* temp, float* humi); // 读取测量结果，成功返回0
```



## 如何编译

1. 在openharmony源码目录下克隆本项目：`git clone https://github.com/xusiwei/harmonyos-aht20`

2. 修改openharmony源码的`build/lite/product/wifiiot.json`文件：

   将`//applications/sample/wifi-iot/app`替换为`//harmonyos-aht20:app`保存；

3. 在openharmony源码目录下执行：`python build.py wifiiot`

