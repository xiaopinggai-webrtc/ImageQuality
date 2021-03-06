# ImageQuality

图像质量评估工具，采用客观评估算法对图像质量进行评估。
可用于图像处理算法的验证。

目前支持的算法：

* 峰值信噪比 PSNR (**p**ulse **s**ignal-to-**n**oise **r**atio)
* 结构相似度 SSIM (**s**tructural **sim**ilarity)

目前采用 RGB 三通道进行图像评估，不支持透明通道的计算。

## 用法

点击“添加”按钮会弹出“添加图像对”对话框。
添加图像暂时仅支持拖放。
点击“确认”按钮则会关闭对话框，并添加文件到主窗口。

点击主窗口左侧中任一图像对，则会在右侧显示图像质量评估算法的结果，同时也会显示所选图像对的预览图。

图像质量评估结果为延迟赋值，在第一次使用时才会计算，当图像过大时会有些许延迟。

点击“复制结果”按钮会计算图像对列表中所有图像对的图像质量评估算法的结果。
由于目前暂时未作异步处理，可能会导致主窗口无响应。
计算完成后会将结果以 CSV（comma-separated values，逗号分隔符）格式保存到剪贴板。
