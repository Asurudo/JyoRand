# JyoRand

## What is JyoRand
JyoRand is a random number generation library based on C++ random engine class and random distribution class, aiming to provide convenient and fast, and various forms of random number generation functions.

## Advantages of JyoRand
JyoRand tries to switch between three different random number engines to increase randomness. This can make the generated random number sequence more difficult to predict, and also introduce some random factors to select the random number engine.

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

If you find any problems, please contact asurudojyo@gmail.com
