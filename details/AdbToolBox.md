# adb工具箱
adb工具箱用于功能调试, 方便检错过程

### 命令行工具
!> 该功能可能会导致程序无法正常运行, 请不要滥用

该工具可以在不关闭bas的情况下测试各种adb命令, 而不用额外的adb程序跑
- 出现`ADB CMD>`时可进行命令输入
- `ADB OUTPUT>`为输出内容的前缀
- 输入`exit`退出该工具
- 所有命令都以`adb`作为前缀(方便复制粘贴)

!> 请不要使用此工具运行需要持续监听的adb命令, 比如`getevent`等, 否则无法退出程序

### 坐标测试与换算工具
该工具用于测试相对坐标位置, 本程序为适配各分辨率将绝对坐标数据转化为了相对坐标数据, 在运行时再根据分辨率转为绝对坐标以此进行适配
> 绝对坐标: 固定数值, 如960 540 | 相对坐标: 比例数值, 如0.5 0.5(本程序当中为50 50)

在输入坐标并回车后即可输出转化的绝对坐标结果同时对该位置进行一次`click(点击)`