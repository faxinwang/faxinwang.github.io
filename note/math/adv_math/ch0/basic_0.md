# 高中数学基础知识

## 一元二次方程

$ax^2+bx+c=0(a\not=0)$
根: $x_1,x_2=\frac{-b\pm\sqrt{\Delta}}{2a}, \Delta=b^2-4ac$
根与系数的关系:$x_1+x_2=-\frac{b}{a}, x_1\cdot x_2=\frac{c}{a}$
抛物线$y=ax^2+bx+c$的顶点:$(-\frac{b}{2a},c-\frac{b^2}{4a})$

## 因式分解

$(a\pm b)^2=a^2 \pm 2ab+b^2$
$(a+b)^3=a^3+3a^2b+3ab^2+b^3$
$(a-b)^3=a^3+3a^2(-b)+3a(-b)^2+(-b)^3=a^3-3a^2b+3ab^2-b^3$
$(a+b)(a-b)=a^2-b^2$
$a^3-b^3=(a-b)(a^2+ab+b^2)$
$a^3+b^3=(a+b)(a^2-ab+b^2)$

## 不等式

1. 有限个数相加的和小于等于这些数绝对值的和.
    例如:
    $a + b \le |a|+|b|$
    $f(x) = f(x)-A+A \le |f(x)-A| + |A|$

2. 设$a,b$为实数,则
    1. $2|ab|\le a^2+b^2$
    2. $a\pm b\le |a|+|b|$
    3. $||a|-|b||\le|a-b|$
    4. 推广:
        1. 离散情况:$|a_1\pm a_2\pm \cdots \pm a_n|\le |a_1|+|a_2|+\cdots+|a_n|$
        2. 连续情况,设$f(x)$在$[a,b]$上可积,则:$|\lmoustache_a^b f(x)dx| \le \lmoustache_a^b|f(x)|dx (a<b)$
3. 设$a_1,a_2,a_3,\cdots,a_n>0,$则,
    1. $\sqrt[n]{a_1a_2a_3\cdots a_n} \le \frac{a_1+a_2+\cdots+a_n}{n}$ (当且仅当$a_1=a_2=\cdots=a_n$时等号成立)
    2. $\frac{a_1+a_2+\cdots+a_n}{n} \le \sqrt[n]{\frac{a_1^2+a_2^2+\cdots+a_n^2}{n}}$ (当且仅当$a_1=a_2=\cdots=a_n$时等号成立)
    3. 常用以下两种特殊形式:
        1. $\sqrt{ab}\le\frac{a+b}{2}\le\sqrt{\frac{a^2+b^2}{2}}, (a,b>0)$
        2. $\sqrt[3]{abc}\le\frac{a+b+c}{3}\le\sqrt{\frac{a^2+b^2+c^2}{3}}, (a,b,c>0)$
4. 若$f(x),g(x)$在$[a,b]$上可积分且平方可积,则:
    $[\lmoustache_b^af(x)g(x)dx]^2 \le \lmoustache_b^af^2(x)dx\cdot\lmoustache_b^ag^2(x)dx$
    <br>
5. 其他重要不等式
    1. $\arctan x < x < \arcsin x(0\le x\le1)$
    2. $x+1\le e^x(\forall x),\ln x \le x-1(x>0)$
    3. $\frac{1}{1+x}<\ln(1+\frac1x)<\frac{1}{x}(x>0)$
        >证明: 令$f(x)=\ln(x),$在区间$[x,x+1]$上对其用拉格朗日中值定理,有
        >$\ln(1+\frac{1}{x})=\ln(1+x)-\ln(x)=\frac{1}{\xi},(x<\xi<x+1)$
        >因此,当x>0时, 有$\frac{1}{1+x}<\ln(1+\frac1x)=\frac{1}{\xi}<\frac{1}{x}$

## 数列

等差数列(公差): $a_1, a_1+d, a_1+2d, \cdots, a_1+(n-1)d, \cdots,(d\not=0)$
通项公式: $a_n = a_1+(n-1)d$
前n项和: $S_n=\frac{n}{2}(a_1+a_n)$

等比数列: $a, aq, aq^2,\cdots, aq^{n-1},\cdots$,($q\not=1$)
通项公式:$a_n=aq^{n-1}$
前n项和:$S_n=\frac{a(1-q^n)}{1-q}$

一些数列的前n项和:
$\sum\limits_{k=1}^nk=1+2+3+\cdots+n=\frac{n(n+1)}{2}$

$\sum\limits_{k=1}^n(2k-1)=1+3+5+\cdots+(2n-1)=\frac{(1+2n-1)n}{2}=n^2$

$\sum\limits_{k=1}^nk^2=1^2+2^2+3^2+\cdots+n^2=\frac{n(n+1)(2n+1)}{6}$

$\sum\limits_{k=1}^nk^3=1^3+2^3+3^3+\cdots+n^3=[\frac{n(n+1)}{2}]^2=(\sum\limits_{k=1}^nk)^2$

## 三角函数

诱导公式:奇变偶不变, 符号看象限

平方关系:
$\sin^2a+\cos^2=1$

$1+\tan^2 a = \sec^2a$

$1+\cot^2 a = \csc^2a$

倍角公式:
$\cos2a=\cos^2a-\sin^2a=2\cos^2a-1=1-2\sin^2a$

$\sin2a=2\sin a\cos a$

$\cos3a = 4\cos^3a-3\cos a$

$\sin3a = -4\sin^3a+3\sin a$

$\tan2a = \frac{2a}{1-\tan^2a}$

万能公式:
$\sin a = \frac{2\tan \frac{a}{2}}{1+\tan^2 \frac{a}{2}}$

$\cos a = \frac{1-\tan^2 \frac{a}{2}}{1+\tan^2\frac{a}{2}}$

$\tan a = \frac{2\tan\frac{a}{2}}{1-\tan^2 \frac{a}{2}}$

## 阶乘和双阶乘

$n!=1\times2\times3\times\cdots\times n,(0!=1)$
$(2n)!!=2\times4\times6\times\cdots\times(2n)=2^n\cdot n!$
<!-- $(2n-1)!!=1\times3\times5\times\cdots\times(2n-1)$ --> 