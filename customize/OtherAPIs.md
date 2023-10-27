# 接入其他ocr API
> 需要一定的`Python`基础知识

因为百度ocr有一定的每日与每月限额, 所以对于一部分人仍然不够使用, 这时候可以尝试自己重写ocr函数

### ocr执行流程
1. 截取图片并读取为`bytes`存入变量 (位置: ./utils/box_scan.py => `Scan.scan`函数)
2. 调用ocr识别图片上的文字并以`List[str]`的形式输出学生名(只有学生名, **其他干扰文字过滤已进行**) (位置: ./utils/box_scan.py => `Scan.pic2name`函数)
3. 滚轮下滑学生列表然后跳回`1` (位置: ./utils/box_scan.py => `Scan.scan`函数)
4. 返回学生清单 (位置: ./utils/box_scan.py => `Scan.scan`函数)

### 如何重写ocr?
理论上只要重写[`./utils/box_scan.py`](https://github.com/ACGN-Alliance/BlueArchive-Starter-cli/blob/main/utils/box_scan.py)当中的`Scan.pic2name`方法即可, 输入为截取的图片(`PIL.Image.Image`), 输出为学生名(`List[str]`)