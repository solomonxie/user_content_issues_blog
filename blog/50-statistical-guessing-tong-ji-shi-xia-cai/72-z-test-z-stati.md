#  ❖ Z Test (z statistics)

> _Z Test_ is a test constructed using the `Z-score`

[`▶︎ Jump back to previous note on: Z-score`](https://github.com/solomonxie/solomonxie.github.io/issues/50#issuecomment-410644808)
[`▶︎ Jump back to previous note on: Z-interval`](https://github.com/solomonxie/solomonxie.github.io/issues/50#issuecomment-418641425)

## Formula of 「Z Test Statistic for proportion」

[`▶︎ Jump back to previous note on: Sample Proportion`](https://github.com/solomonxie/solomonxie.github.io/issues/50#issuecomment-416493188)


The test statistic gives us an idea of how far away our sample result is from our null hypothesis. For a one-sample z-test for a proportion, our test statistic is:

![image](https://user-images.githubusercontent.com/14041622/45348047-2736ba80-b5e0-11e8-9199-610a5e0e9b9d.png)
(which p^ is the `Sample proportion`, p₀ is the proportion from _null hypothesis_, n is sample size)

> Understanding the formula:
The `statistic - parameter` results the DISTANCE from _Sample proportion_ to _Population proportion_.
The `Standard Deviation of statistic` represents the ~DISTANCE from _Sample SD_ to population SD.~
Therefore, dividing the **Distance of proportion** by **Distance of SD** will results in a `Normalized Distance for proportion`.


## Calculating 「Z Test」 about a proportion

[Refer to Khan academy: Calculating a z statistic in a test about a proportion](https://www.khanacademy.org/math/statistics-probability/significance-tests-one-sample/modal/v/calculating-a-z-statistic-in-a-significance-test)

### Example
![image](https://user-images.githubusercontent.com/14041622/45347965-ef2f7780-b5df-11e8-951d-cd459d192097.png)
Solve:
![image](https://user-images.githubusercontent.com/14041622/45348229-aa581080-b5e0-11e8-9ebf-b130cca01930.png)



## Calculating a 「P-value」 given a z statistic

[Refer to Khan academy: Calculating a P-value given a z statistic](https://www.khanacademy.org/math/statistics-probability/significance-tests-one-sample/modal/v/calculating-p-value-from-z-table)


### Example
![image](https://user-images.githubusercontent.com/14041622/45360436-30d11a00-b602-11e8-84e0-168e55fd5e09.png)
Solve:
![image](https://user-images.githubusercontent.com/14041622/45360444-34fd3780-b602-11e8-91fd-23b8640c6ba3.png)


### Example
![image](https://user-images.githubusercontent.com/14041622/45358366-ca48fd80-b5fb-11e8-9a6d-3a9cdc23713d.png)
Solve:
- To get the probability in a Z-score normal distribution, we need:
    - Mean
    - Standard deviation
    - Z-score
- For convenience, we can set the _mean_ as `0` at the centre, and _SD_ as `1`
![image](https://user-images.githubusercontent.com/14041622/45358598-77bc1100-b5fc-11e8-9ab3-3dd1a95a0bd9.png)
- Since it's asking for proportion at left tail, so we can directly input those values in a calculator:
![image](https://user-images.githubusercontent.com/14041622/45358643-a803af80-b5fc-11e8-8e76-c8c135c4a3e3.png)
- The answer is 0.106


### Example
![image](https://user-images.githubusercontent.com/14041622/45359676-cf0fb080-b5ff-11e8-9b7e-cbd77134995c.png)
Solve:
- Get a calculator, and input these values:
    - Mean (default): 0
    - SD (default): 1
    - Z-score: -1.5
- We get that the `left-tail` proportion is `0.0668072`
- Since the alternative hypothesis is `ha ≠ ...`, so we're to calculate BOTH tails proportion.
- Z-score as `-1.5` means the point is at left tail, so we just need to multiply the proportion by `2`
- The `p-value` then is `0.0668072*2 = 0. 134`
![image](https://user-images.githubusercontent.com/14041622/45360073-0cc10900-b601-11e8-958e-64e2bbedcffc.png)



## Making conclusions in a 「z test」 for a proportion

Calculate Z-value -> Convert to P-value -> Compare with ⍺ level -> Make decision.

### Example
![image](https://user-images.githubusercontent.com/14041622/45362348-29603f80-b607-11e8-800b-4abd4d5c3f7b.png)
Solve:
![image](https://user-images.githubusercontent.com/14041622/45362386-45fc7780-b607-11e8-8f05-d1eb4a3f2124.png)

