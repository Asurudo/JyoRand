# JyoRand

## JyoRand是什么
JyoRand是基于C++的随机数引擎类和随机数分布类封装的随机数生成库，旨在提供方便快捷，且形式多样的随机数生成功能。

## JyoRand的优点
JyoRand尝试在三个不同的随机数引擎之间切换，增加了随机性。这可以使生成的随机数序列更难以预测，同时还引入了一些随机性的因素来选择随机数引擎。

本库提供了均匀分布、实数均匀分布、二项分布以及正态分布等多种随机数分布的支持，因此可以满足不同应用的随机数生成需求。

## JyoRand的用法

使用时先在全局声明并定义一个对象：`Rand jyorandengine;`

接着进行方法的调用，目前支持以下方法：

```C++
// 返回一个0到100闭区间的int类型随机整数
int rd = jyorandengine.jyoRandGetInteger<int>(0, 100);

// 返回一个0到100闭区间的double类型随机数
double rd = jyorandengine.jyoRandGetReal<double>(0, 100);

// 返回一个bool值，39%的可能为true（默认为0.5）
bool value = jyorandengine.jyoRandGetBool(0.39);

// 返回一个double类型的，且均值m标准差s的正态分布的结果（默认m为0，s为1）
// 多次调用可得到一个正态分布
double value = jyorandengine.jyoRandGetNormal<double>(m, s);
```


