---
layout:     post
title:      散热设计5-海拔对风道系统影响分析
category:   the-little-heat-design
---

这一节的内容是参考EBM的文档《Impact of air density on air performance of fan》，对其中的信息进行自己的解读。海拔所有的影响都最终体现在空气密度的影响上。

### 1.温度湿度对空气密度影响

对于理想空气的密度计算(这个公式后面会用到)

![](/images/the-little-heat-design/Formula_S5_F1.jpg)公式1

其中p为压强\[Pa\]，1Pa=1N/m^2，T为开尔文温度\[K\]， T=摄氏温度+273.15，,Ri为气体常数\[J/kgK\]，其中干燥的空气系数Ri=287.05J/kgK 。

假定环境气压为p=101325Pa\(标准大气压\)，绝对湿度为6g水/1kg空气，那么干燥空气密度与湿空气密度如图1所示，从中可以得出，干燥空气与潮湿空气的密度相差很小。

[![](/images/the-little-heat-design/Cover_Heat_S5_E1.png)](散热设计5_海拔对风路系统影响分析-EIT Lab博客_files/Cover_Heat_S5_E1.png)

##### **图1.空气密度随温度变化**

（绿色为潮湿空气，红色为干燥空气）（引自EBM资料）

**结论1：标准大气压不变的情况下，温度每升高10K，空气密度降低2.7%。**

### 2.海拔对空气密度影响

现做如下标准环境设定：在0m海拔高度，大气压强 =101325Pa\(标准大气压\)，当环境温度为 =15℃，此时空气密度为1.225kg/m³ 。

经过长期的测试数据拟合得到图2结果（具体公式可以参看前面提到的EBM文档），海拔对空气密度，压强和温度影响。

![](/images/the-little-heat-design/Cover_Heat_S5_E2.png)

##### **图2.海拔高度对空气密度，压强和温度影响**

**结论2：与0m海拔，15度环境温度，1个大气压，标准环境条件相比**

* **海拔每升高1000m，环境温度降低6.5℃。**
* **海拔每升高1000m，大气压强降低10kPa，约为10%。**
* **海拔每升高1000m，空气密度降低0.1kg/m^3，约为10%。**

### **3.空气密度最终变化结构**

设定标准环境条件为：在0m海拔下大气压强 P=101325Pa\(标准大气压\)，当环境温度为 15℃，此时空气密度为1.225kg/m^3。

根据上一节公式推导，同一地理坐标下，当海拔升高到5000m，温度降低为-17.5℃，压强降低为54025.6，此条件下的空气密度为0.736 ，得到表1。

##### 表1.海拔对空气密度影响\(同一地理位置\)

| 海拔高度\(m\) | 环境温度\(℃\) | 大气压强\(Pa\) | 空气密度\(kg/m^3 \) |
| :--- | :--- | :--- | :--- |
| 0 | 15 | 101325.0 | 1.225 |
| 1000 | 8.5 | 89876.4 | 1.112 |
| 2000 | 2 | 79498.4 | 1.007 |
| 2500 | -1.25 | 75047.9 | 0.961 |
| 3000 | -4.5 | 70112.8 | 0.909 |
| 4000 | -11 | 61645.3 | 0.819 |
| 5000 | -17.5 | 54025.6 | 0.736 |

因为空气密度与大气压强和环境温度同时相关，而同一海拔下大气压强随温度变化只有1%左右（经验数据），因此可以假设同一地理位置在同一海拔下，其大气压强不变，此时按照公式1就可以推导出同一海拔下，50℃环境温度下的空气密度。

##### 表2.不同海拔下同一环境温度下的空气密度

| 海拔高度\(m\) | 环境温度\(℃\) | 大气压强\(Pa\) | 空气密度\(kg/m^3 \) |
| :--- | :--- | :--- | :--- |
| 0 | 15 | 101325.0 | 1.225 |
|  | 25（测试） | 101325.0 | 1.184 |
|  | 40 | 101325.0 | 1.127 |
|  | 45 | 101325.0 | 1.109 |
|  | 50 | 101325.0 | 1.092 |
| 1000 | 40 | 89876.4 | 0.969 |
| 2000 | 40 | 79498.4 | 0.884 |
|  | 45 | 79498.4 | 0.871 |
|  | 50 | 79498.4 | 0.857 |
| 2500 | 40 | 75047.9 | 0.835 |
|  | 45 | 75047.9 | 0.822 |
|  | 50 | 75047.9 | 0.809 |
| 3000 | 40 | 70112.8 | 0.780 |
|  | 45 | 70112.8 | 0.768 |
|  | 50 | 70112.8 | 0.756 |
| 4000 | 50 | 61645.3 | 0.665 |
| 5000 | 50 | 54025.6 | 0.582 |

**结论3：**

* **同一地理位置，同一海拔下，大气压强变化小于1%**
  **。**
* **同样环境温度下，不同海拔高度下，空气密度变化与压强成正比。**
* **环境温度每升高10K**
  **，空气密度下降7%**
  **，在工程上已经不能忽略，因为环境温度升高35**
  **度就会产生空气密度10%**
  **的降低。**

### **4.海拔对风道影响**

有关海拔与空气密度对风道风阻和风扇特性的影响，目前查阅的文献没有得到有效的计算公式，多数分析结果是基于经验估计和实际测试结果。

基于经验估计的话，**假设风扇转速不随空气密度变化而变化，**也就意味着在不同空气密度下，风扇的体积流量不变，风扇的静压和质量流量均与密度成正比，而风道特性随着空气密度增加，风阻也会增加，于是得到如图3所示。由此可以得到，**当空气密度发生变化时，风道工作点对应的体积流量不变。**

![](/images/the-little-heat-design/Cover_Heat_S5_E3.png)

##### **图3.空气密度对风道工作点的影响**

基于试验测试的话，则是对整个风道在不同海拔和环境温度下，进行测试，AVC资料中提供的测试结果如图4所示。

[![](/images/the-little-heat-design/Cover_Heat_S5_E4.png)](散热设计5_海拔对风路系统影响分析-EIT Lab博客_files/Cover_Heat_S5_E4.png)

##### **图4.实验测试海拔对风道特性影响**

实际测试中，空气密度变化，风扇的转速不是恒定值，当密度降低时，转速升高，风道风阻降低，同时风扇风压降低，具体的工作点变化多少完全取决于风扇电机的工作特性，以及风道的结构。 根据图4测试结果得出的结论是，高度升高到4000m后，空气密度降低26.74%，体积流量增高4.7%，这意味着海拔升高过程中，占主要部分的是空气密度变化，超过体积流量变化一个数量级。

**结论4：**

* **无论是经验估计，还是实际测试，都表明海拔升高后（空气密度变小），体积流量基本不变，主要受影响是空气密度本身的变化。**

### **5.综合结论**

风扇的散热效果与风扇的质量流量相关，而4小节中的结论得到的信息是，当空气密度变化，风扇体积流量基本不变，所以风扇质量流量变化更大程度上取决于空气密度。

为了方便计算，现在将所有空气密度下的体积流量，折算为风扇温升测试环境条件下（0海拔下25度环境温度）的等效体积流量，为方便表达这里转化为体积比例因数，因为体积流量不变，所以等效体积流量比转化为空气密度比值，由此得到表3。

##### 表3.不同海拔下，等效体积流量表

| 海拔高度\(m\) | 环境温度\(℃\) | 大气压强\(Pa\) | 空气密度\( kg/m^3\) | 流量等效比例因数 |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 15 | 101325.0 | 1.225 | 1.035 |
|  | 25（测试） | 101325.0 | 1.184 | 1.000 |
|  | 40 | 101325.0 | 1.127 | 0.952 |
|  | 45 | 101325.0 | 1.109 | 0.937 |
|  | 50 | 101325.0 | 1.092 | 0.922 |
| 1000 | 40 | 89876.4 | 0.969 | 0.818 |
| 2000 | 40 | 79498.4 | 0.884 | 0.747 |
|  | 45 | 79498.4 | 0.871 | 0.736 |
|  | 50 | 79498.4 | 0.857 | 0.724 |
| 2500 | 40 | 75047.9 | 0.835 | 0.705 |
|  | 45 | 75047.9 | 0.822 | 0.694 |
|  | 50 | 75047.9 | 0.809 | 0.683 |
| 3000 | 40 | 70112.8 | 0.780 | 0.659 |
|  | 45 | 70112.8 | 0.768 | 0.649 |
|  | 50 | 70112.8 | 0.756 | 0.639 |
| 4000 | 40 | 61645.3 | 0.686 | 0.579 |
| 5000 | 40 | 54025.6 | 0.601 | 0.508 |

如果分析海拔和温度对散热的影响，只要将参考点的流量乘以对应的比例因数即可。比如一风道的参考点是0m海拔，25环境温度下的流量为1000\(m^3/h\),想知道在3000m高度环境温度为50度下的等效流量，只要查表3得到比例因子为0.639，那么其等效流量为1000\*0.639=639m^3/h.

散热设计系列结束了，但是希望能够多多交流。

