# 下载
本项目提供三种下载渠道, 分别是蓝奏云, GitHub Release与群文件

## 下载渠道
#### 蓝奏云
不开魔法也能下载, 速度很快, 但版本不全

#### GitHub Release(推荐)
需要魔法, 不然下载极慢甚至无法访问, 有重大更新的版本基本都会发布并且有完整的更新日志
[链接](https://github.com/ACGN-Alliance/BlueArchive-Starter-cli/releases/tag/v1.0.6.3)

#### 群文件
致力于实时解决群友反馈的bug以及发布新功能测试, 理论上是最新最全的版本, 欢迎加群下载~

## 内容
下载的文件是`7z`或者`zip`格式的压缩包, Linux版本解压后为`.bin`文件, windows则为`.exe`与很多`dll`与`pyd`文件

> 为什么不用nuitka的`onefile`打包, 这样就没有这么多dll与pyd了? 因为经测试发现在Windows上运行onefile版本会被ESET认定为病毒程序, 为了防止被误会所以没有使用onefile进行打包
