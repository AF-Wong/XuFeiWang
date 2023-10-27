CNN

基于CNN的稠密连接网络的单图超分是以CNN的网络为基础，使用稠密连接构建网络并进行超分。
其中的CNN是指经典的如SRCNN等CNN超分算法，使用双三次插值将低分辨率图像放大到目标尺寸。
然后通过卷积网络提取目标特征和非线性映射最后完成重建。
稠密连接简单地说就是所有的层互相进行连接，每个层都会接受前面所有层作为额外的输入。
从而形成了一个密集的连接结构。

SwinTransformer

传统Transformer主要应用于自然语言处理领域，与图像任务相比，单词作为token的大小比较固定，
但是图片的像素取值范围非常大，并且图片的像素解析度也远大于单词。所以，使用SwinTransformer
比传统Transformer更适合图像领域。SwinTransformer的主要贡献是“移位窗”结构，这种结构会使窗
向不同的方向移动从而进行新的模块划分。能够将上一次的传统窗结构的不同窗之间进行联系，增强不同
区域信息交互能力，提高任务效率。另一个贡献是提出了“本地计算注意力”机制，将图片划分为一个个
小块进行本块的注意力计算，使得注意力对图片尺寸具有线性复杂度而非传统的二次复杂度，并进行
层级式特征提取。最后，SwinTransformer的文章提出了循环掩码结构解决“移位窗”后分块数变多并且
分块大小不一致问题。