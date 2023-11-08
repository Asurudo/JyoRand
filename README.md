# JyoRand

## What is JyoRand

JyoRand is a random number generation library based on C++ random engine class and random distribution class, aiming to provide convenient and fast, and various forms of random number generation functions.

## Advantages of JyoRand

JyoRand tries to switch between three different random number engines to increase randomness. This can make the generated random number sequence more difficult to predict, and also add some random factors to select the random number engine.

This library provides support for uniform distribution, real uniform distribution, binomial distribution and normal distribution, so it can meet the random number generation needs of different applications.

## How to use JyoRand

First declare and define an object globally: `Rand jyorandengine;`

Then call the method, currently supports the following methods:

```C++
// Returns an int type random integer in the closed interval of 0 to 100
int rd = jyorandengine.jyoRandGetInteger<int>(0, 100);

// Returns a double type random number in the closed interval of 0 to 100
double rd = jyorandengine.jyoRandGetReal<double>(0, 100);

// Returns a bool value, 39% chance of true (default 0.5)
bool value = jyorandengine.jyoRandGetBool(0.39);

// Returns a double type, and the mean m standard deviation s of the normal distribution (default m is 0, s is 1)
// Multiple calls can get a normal distribution
double value = jyorandengine.jyoRandGetNormal<double>(m, s);
```

## Reference links of JyoRand

[mt19937 and random distribution template](https://demo.hedgedoc.org/s/ECOgQ9RZM)

[Random number generation](https://demo.hedgedoc.org/s/Dp8lD-IGz)

If you find any problem, please contact asurudojyo@gmail.com


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

## JyoRand的参考链接

[mt19937及随机数分布模板](https://demo.hedgedoc.org/s/ECOgQ9RZM)

[随机数生成](https://demo.hedgedoc.org/s/Dp8lD-IGz)

发现问题请联系asurudojyo@gmail.com

