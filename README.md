# Image-processing-test
研究方向：图像篡改检测。
2020-5-25
```
项目1：
压缩文件中里面有101张图片，50张原始图片，50张经过中值或均值滤波的图片， 还有一张是两者拼接出来的图片。
1）试试能不能把原始图片找出来。
2）用第一问的算法来定位拼接图片的篡改区域。
可以用任何一种语言来实现，要有算法的解释
```
paper 1:[On detection of Median Filtering in Digital Images.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/On%20detection%20of%20Median%20Filtering%20in%20Digital%20Images.pdf)

```
项目2：
1)“ucid00001.tif”、“ucid00002.tif’,……ucid00050.tif'作为原始图像，创建对比度增强的图像。(附文件式(11))

2)执行附件第3节的取证算法，区分原始图像和增强图像。祝你好运。

```
paper 2:[stamm2008_BLINDFORENSICSOFCONTRASTENHANCEMENTINDIGITALIMAGES.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/stamm2008_BLINDFORENSICSOFCONTRASTENHANCEMENTINDIGITALIMAGES.pdf)
```
项目3:
附件是重采样检测的先驱工作。尝试尽可能多地实现它，并找出在附加数据集中对哪些图像进行了重新采样(50幅原始图像和50幅重新采样)。

为了使任务更容易，您不需要估计Alpha。您可以直接使用(25)中的Alpha*。对于数据集，缩放因子在1.1和2之间，不旋转。
```
paper 3:[2008MMSEC_Fast and Reliable Resampling Detection by Spectral Analysis of Fixed Linear Predictor Residue.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2008MMSEC_Fast%20and%20Reliable%20Resampling%20Detection%20by%20Spectral%20Analysis%20of%20Fixed%20Linear%20Predictor%20Residue.pdf)
```
项目4：
随附50张.tif图像，这些图像之前已进行JPEG压缩。 将它们与ucid00001-50.tif结合。
          1.使用所附文件（公式（2））中描述的算法来区分两类：原始tif与jpeg + tif。
          2.对于JPEG压缩图像，请尝试估计Y的（1，1）分量的q值，即m = 1，n = 1。 注意，（0,0）分量是DC分量。
          3.提供一份1-2页的文档，说明您对本文的理解。
          您不需要实现（4），而是使用类似dct2（）的函数。 希望您可以在36小时内完成。 关键是要理解所编码内容的物理含义。
```
paper 4:[2003TIP_Identification of Bitmap Compression History JPEG Detection and Quantizer Estimation.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2003TIP_Identification%20of%20Bitmap%20Compression%20History%20JPEG%20Detection%20and%20Quantizer%20Estimation.pdf)
```
项目5：
这次我们回到中值滤波取证。
    1. 在此前的工作中，我们实现了‘On Detection of Median Filtering in Digital Images’ 第三章的算法，现在我们继续实现其第四章算法。先自己尝试提取SPAM特征，如果有困难可以参考‘spam686.m’
    2. 实现‘Robust Median Filtering Forensics Using An Autoregressive Model’ 里的算法，这是我们课题组代表性工作之一。同样先自己理解，有困难参考‘ar_flip_mfr.m’
    3. 对比分析 这两种算法 以及我们之前实现的 用h_0/h_1特征的方法，在取证性能上的差异。
    机器学习需要大量的图片来训练，我把完整的UCID数据库发给你，建议用00001-01000训练，剩下的做测试。争取在36小时内提交给我
    SVM工具箱下载地址：https://www.csie.ntu.edu.tw/~cjlin/libsvm/
```
paper 5:[2013TIFS_Kang_Robust Median Filtering Forensics Using An Autoregressive Model.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2013TIFS_Kang_Robust%20Median%20Filtering%20Forensics%20Using%20An%20Autoregressive%20Model.pdf)
file 1:[ar_flip_mfr](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/ar_flip_mfr.m)
     2:[spam686.m](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/spam686.m)
```
项目6：
在Task3中，你试图回答以下问题:
图像是否已重新采样?
现在，我们想更进一步:
图像被重新采样了多少?

1)使用ucid数据库生成重采样图像，重采样率= [0.6 0.8 1.2 1.8];结果，你将有4*1338重新采样图像和1338原始图像;
2)实现附图中的算法，估计给定图像的重采样率。使用5*1000张图像进行训练，5*338张图像进行测试。
希望你们能学会如何用SVM进行多分类。(在我们的情况下，5个类)提交结果
```
paper 6:[2012TM_Normalized Energy Density-Based Forensic Detection of Resampled Images ](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2012TM_Normalized%20Energy%20Density-Based%20Forensic%20Detection%20of%20Resampled%20Images%20.pdf)
```
项目7：
 1. Detail understanding of 'Demosaicing',
 2. Distinguish PIM and CG images by implementing 'Image Authentication by Detecting Traces of Demosaicing'.
     About the database: for PIM images, you can take pics with your mobile phone or camera. For CG images, you can download images from the urls in 'Identification of natural images and computer generated graphics based on statistical and textural features'
      Please submit the results, as well as your understanding of 'Demosaicing' in 36 hours.
```
paper 7-1:[2015JFS_Pengfei_Identification of natural images and computer generated graphics based on statistical and textural features](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2015JFS_Pengfei_Identification%20of%20natural%20images%20and%20computer%20generated%20graphics%20based%20on%20statistical%20and%20textural%20features.pdf)
      7-2:[CVPRW2008_Gallagher_Image Authentication by Detecting Traces of Demosaicing](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/CVPRW2008_Gallagher_Image%20Authentication%20by%20Detecting%20Traces%20of%20Demosaicing.pdf)
```
项目8:
 这一周的任务是实现‘Synthesis of Color Filter Array Pattern in Digital Images’里的方法。目标和以往不同，我们这次不是要检测CFA的痕迹，而是要伪造CFA痕迹。
     1）用论文中的方法，对上次任务中收集的 CG 图片（没有CFA痕迹）进行CFA伪造，保存成未压缩格式(tif 或png)，使得我们上次的算法将其判断为PIM images。
     2）将自己对算法的理解和实现过程形成类似2009_SPIE_slides.pdf一样的文档。
     从这次任务开始，希望你能把大部分时间放在写作，而不是写代码上，这才是我们研究生的培养目标。
```
paper 8-1:[2009_SPIE_slides.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2009_SPIE_slides.pdf)
      8-2:[2009_SPIE_Synthesis of Color Filter Array Pattern in Digital Images.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2009_SPIE_Synthesis%20of%20Color%20Filter%20Array%20Pattern%20in%20Digital%20Images.pdf)
```
项目9：
这一次的任务是利用附件‘2006TIFS_Lukáˇs_digital camara identification from SPN’里的方法来检测相片所对应的相机。
     1）准备三部相机(或手机)的各50张照片，相信已经完成；
     2）按照论文修改我给你的代码。注意：想要运行代码，你需要学习将Filter文件夹中c++代码编译成Matlab可以调用的mex文件 （如果你电脑是windows64，则应该是mexw64文件）
     3）每部相机用20张照片生成相机指纹，30张测试。你有3部相机，应该要做3*3*30次实验。
```
paper 9:[2006TIFS_Lukáˇs_digital camara identification from SPN](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2006TIFS_Luk%C3%A1%CB%87s_digital%20camara%20identification%20from%20SPN.PDF)
```
项目10：
这一次的任务是利用附件‘2008TIFS_Chen_Determining Image Origin and Integrity UsingSensorNoise'里的方法来定位图像篡改。
     1）选定上次三部相机中的一部，再拍30张照片(Set_train)，用于训练一个correlation predictor(详见论文)；
     2）从这部相机的上次用于测试的30张图片（Set_test）中选择几张，进行论文中的篡改（建议用Photoshop），篡改完成后另存为tif 或png格式；
     3）实现论文中的算法, 对篡改区域进行定位。重点在 V. CORRELATION PREDICTOR，也就是你要从图像内容来预测相关性值，见（26）。然后用实际相关性值和预测值对比，从而确定篡改区域。(25)的matlab参考代码：
     theta = inv(features'*features)*features'*target;
     为了定位效果比较好，篡改时的原图建议选择光线较好，内容相对平坦的图片.如果提取(23)中的15维特征有困难，参考这个函数extractPatchFeatures.m
```
paper 10:[2008TIFS_Chen_Determining Image Origin and Integrity UsingSensorNoise](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2008TIFS_Chen_Determining%20Image%20Origin%20and%20Integrity%20UsingSensorNoise.pdf)
```
Task 11:
       1）实现代码中的算法，
       2）思考如何把噪声水平估计用到拼接定位中来，自己假设一个案例，并用此方法来进行定位。
```
paper 11:[2015ICCV_Chen_An_Efficient_Statistical_method_for_NLE_yang.pdf](https://github.com/standbyme-ge/Image-processing-test/blob/master/PaperList/2015ICCV_Chen_An_Efficient_Statistical_method_for_NLE_yang.pdf)
```


