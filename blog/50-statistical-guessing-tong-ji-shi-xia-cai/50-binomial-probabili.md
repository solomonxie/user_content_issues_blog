# Binomial Probability

[Refer to article on Khan academy: Binomial probability (basic)](https://www.khanacademy.org/math/ap-statistics/random-variables-ap/modal/a/binomial-probability-basic)
[Refer to Khan academy: Generalizing k scores in n attempts](https://www.khanacademy.org/math/ap-statistics/random-variables-ap/modal/v/generalizing-k-scores-in-n-attempts)

[`▶︎ Online Binomial Probability Calculator`](https://www.omnicalculator.com/statistics/binomial-distribution)

## Formula of 「Binomial Probability」


![image](https://user-images.githubusercontent.com/14041622/46007847-a9010a80-c0ed-11e8-91b8-25ea8d6cb7e6.png)


![image](https://user-images.githubusercontent.com/14041622/44652285-1d2c8d80-aa1e-11e8-8413-01d4d074f07b.png)


We could simplify (verbal) it as:
```
P(X=r) = Combinations × P(yes) × P(no)
```

For the **combinations**, here's the formula:
![image](https://user-images.githubusercontent.com/14041622/44515307-cb6dc580-a6f4-11e8-9b85-8c3375a297a5.png)

Or use the [`▶︎ Online Combination Calculator`](https://www.omnicalculator.com/statistics/combination).


Example:
![image](https://user-images.githubusercontent.com/14041622/44392555-1062f200-a565-11e8-854d-c331560dd408.png)

### Example
![image](https://user-images.githubusercontent.com/14041622/44515644-a75eb400-a6f5-11e8-8434-43a71c723fad.png)
Solve:
- Apply the `Binomial Probability Formula`, the answer is:
![image](https://user-images.githubusercontent.com/14041622/44515680-c9f0cd00-a6f5-11e8-8af7-0c421c8009bf.png)


## 「Mean & Variance」 of Binomial R.V.

![Formula](https://user-images.githubusercontent.com/14041622/44516491-ca8a6300-a6f7-11e8-9eb6-fb01d0debb63.png)

- `Expected Value = Mean = μx`
- `Variance = Standard Deviation = σx`


### Example
![image](https://user-images.githubusercontent.com/14041622/44653853-726a9e00-aa22-11e8-9ad7-780f391ab486.png)
Solve:
![image](https://user-images.githubusercontent.com/14041622/44653960-c1183800-aa22-11e8-8aed-e21b0e50f02e.png)


### Example
![image](https://user-images.githubusercontent.com/14041622/44516338-67003580-a6f7-11e8-9ffa-84469c1977d5.png)
Solve:
- `Mean = μx = np = 100 * 0.25 = 25`
- `SD = σx = √(np(1-p)) = √(25*0.75) = 4.33`


## 「Cumulative Binomial Probability」


### Example
![image](https://user-images.githubusercontent.com/14041622/44652967-f2dbcf80-aa1f-11e8-97b9-a02a859f911f.png)
Solve:
- One way:
![image](https://user-images.githubusercontent.com/14041622/44653099-5ebe3800-aa20-11e8-9de9-f5a610c4b542.png)
- Another way:
![image](https://user-images.githubusercontent.com/14041622/44653197-a5139700-aa20-11e8-8d9e-4fa0c828538c.png)


### Example
![image](https://user-images.githubusercontent.com/14041622/46006743-ce404980-c0ea-11e8-8d8c-7723df83e41f.png)
Solve:
- We can see it as `P(X > 3) = P(4) + P(5)`, or `P(X>3) = 1 - (P(1) + P(2) + P(3))`, we're gonna use first one in this case.
![image](https://user-images.githubusercontent.com/14041622/46006976-663e3300-c0eb-11e8-8f9a-40bbeabe3409.png)

