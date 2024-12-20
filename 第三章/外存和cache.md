# 外存
我们一般说的外存有两种：
- 磁盘
- 固态硬盘（SSD）

![](/image/3/wc.png)
物理原理只需要理解就好了，他本身的优点主要就在于**便宜**，**存储量大**，**不易丢失（或者说可以脱机存储）**
## 磁盘存储器
### 磁盘存储器的构成
![](/image/3/外存/cp.png)
我们可以梳理一下磁盘存储器的构成，磁盘存储器由多个**记录面**重叠组成，之间有磁头来进行读写。
![](/image/3/外存/cp1.png)
单个**记录面**有多个圆形的凹槽，称为**磁道**，数据就存储在磁道中，我们可以通过切割磁道将其分为一个个扇形的区域，称为**扇区**，即图中蓝色部分。

硬盘存储器之间的接口有多个标准：**IDE,SCSI,SATA等**
![](/image/3/外存/cp2.png)
可以看到具体实现中最上和最下的面没有磁头，说明这部分没有数据，显然又是成本之类的问题。
![](/image/3/外存/cp3.png)
![](/image/3/外存/cp4.png)
### 磁盘的性能指标
我们不深究磁盘的物理层面的原理，关键在于**磁盘的性能指标**，
![](/image/3/外存/cp5.png)
我们通过考题来联系一下：

**例71** 磁盘组有 6 片磁盘，每片有两个记录面，最上最下两个面不用。存储区域内径 22cm，外径 33cm，道密度为40 道/cm，内层位密度 400位/cm，转速6000转/分。问：
1. 共有多少柱面？
2. 盘组总存储容量是多少？
3. 内部数据传输率是多少？

我们来解析这道题：
#### 1. 有效存储区域和柱面数

有效存储区域为：
\[
16.5 \text{ cm} - 11 \text{ cm} = 5.5 \text{ cm}
\]

根据道密度（40道/cm）：
\[
\text{道数} = 40 \text{ 道/cm} \times 5.5 \text{ cm} = 220 \text{ 道}
\]
因此，柱面数为220。

#### 2. 每个面信息量和总容量

内层磁道周长：
\[
2\pi R = 2 \times 3.14 \times 11 \approx 69.08 \text{ cm}
\]

每道信息量：
\[
\text{信息量} = 400 \text{ 位/cm} \times 69.08 \text{ cm} \approx 27632 \text{ 位} \approx 3454 \text{ B}
\]

每面信息量：
\[
\text{每面信息量} = 3454 \text{ B} \times 220 = 759880 \text{ B}
\]

盘组总容量：
\[
\text{总容量} = 759880 \text{ B} \times 10 = 7598800 \text{ B}
\]

#### 3. 数据传输率

磁盘转速：
\[
r = \frac{6000 \text{ 转}}{60 \text{ 秒}} = 100 \text{ 转/秒}
\]

数据传输率：
\[
D_r = r \times N = 100 \text{ 转/秒} \times 3454 \text{ B} = 345400 \text{ B/s}
\]

#### 最终结果

1. **柱面数**：220
2. **总存储容量**：7598800 B
3. **内部数据传输率**：345400 B/s
### 磁盘的工作过程
![](/image/3/外存/cp6.png)
![](/image/3/外存/cp7.png)
![](/image/3/外存/cp8.png)
![](/image/3/外存/cp9.png)

## 固态硬盘（SSD）
固态硬盘是近些年的新考点，内容不多
![](/image/3/外存/SSD1.png)
![](/image/3/外存/SSD2.png)
![](/image/3/外存/SSD3.png)