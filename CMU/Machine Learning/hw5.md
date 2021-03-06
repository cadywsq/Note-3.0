# HW5

## 1.1.1

+ `#pi` = 10 - 1 = 9
+ `#A` = 10 * (10-1) = 90
+ `#B` = 10 * (100-1) = 990

990 + 90 + 9 = 1089

## 1.1.2

根据题意可以列出方程

```
pi_a = pi_a*0.7 + pi_b*0.1 + pi_c*0.2
pi_b = pi_a*0.2 + pi_b*0.6 + pi_c*0.2
pi_b = pi_a*0.1 + pi_b*0.1 + pi_c*0.8
```

解得 0.3 0.5 0.2

## 1.1.3

**a.**

P(q3) = A 由四条路径组成(A_aa 表示从 A 到 A 的迁移概率)：

+ pi_a * A_aa * A_aa
+ pi_a * A_ab * A_ba
+ pi_b * A_ba * A_aa
+ pi_b * A_bb * A_ba

列成算式就是

```
0.6*0.7*0.7+0.4*0.3*0.7+0.6*0.3*0.3+0.4*0.7*0.3
```

**b.**

ABA 序列可以列出公式

```
pi_A * A_ab * A_ba 
i.e
0.6 * 0.3 * 0.3
```

**c.**

```
alpha_2(A) = (alpha_1(A)A_aa + alpha_1(B)A_ba)*B_Ao2
           = (0.12*0.7+0.36*0.3)*0.8
           = 0.1536

alpha_1(A) = pi_A * b_a1 = 0.6 * 0.2 = 0.12
alpha_1(B) = pi_B * b_b1 = 0.4 * 0.9 = 0.36

```

```
alpha_2(B) = (alpha_1(A)A_ab + alpha_1(B)A_bb)*B_Bo2
           = (0.12*0.3 + 0.36*0.7)*0.1
           = 0.0288
```

**d.**

P(o1=a, o2=0, o3=1) 是所有可能路径生成指定序列的概率

利用前向概率计算

```
alpha_3(A) 
= alpha_2(A)*A_aa*B_A1 + alpha_2(B)*A_ba*B_A1 
= 0.1536*0.7*0.2 + 0.0288*0.3*0.2
= 0.0232

alpha_3(B)
= alpha_2(A)*A_ab*B_B1 + alpha_2(B)*A_bb*B_B1
= 0.1536*0.3*0.9 + 0.0288*0.7*0.9
= 0.0596

相加 = 0.0828
```

**e.**

0.0232 / 0.0828 = 0.2802

**f.**

BA

## 1.2.1

BIC

ln L - k1 = ln L - k2 / 2 * ln N

比较 k1 和 k2 的大小，k2 会更好


