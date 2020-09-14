deme说明：

运行平台P2 SSD202

SDK使用最新release的版本即可

解压后把ffmpeg/host/dynamic目录下的lib拷到板子/customer/lib下 
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/lib:/customer/lib
运行./RotateTest hd_cus.mp4

默认是不旋转，串口输入'c'切换到旋转270度
hd_cus.mp4 是mpeg4编码，模拟软解下的翻转
demo.mp4 是H264编码不带B帧，模拟硬解下的翻转
MIss_A_Bframes.mp4 是H264编码带B帧

更换屏参需要更改platform.h文件中的屏幕宽高

