
2018/6/8 星期五

### 如何理解扩展欧几里得算法中解系的最小间距.

今天跟乐乐讲解扩展欧几里得算法的时候,突然明白了解系的最小间距是怎么得来的, 下面写一下推导过程.

```C++
//求出ax+by=gcd(a,b)的一组解
int ext_gcd(int a,int b, int &x ,int &y)
{
    if(b == 0)
    {
        x=1; y=0;
        return a;
    }
    int c = ext_gcd(a, b, x, y);
    int xt = x;
    x = y;
    y = xt - a / b * y;
    return c;
}
```

通常要求的是 $ax+by=n$的一组解,设c=gcd(a,b), 我们一般会先通过ext_gcd()函数求出
$ax+by=c$的一组解$(x_0,y_0)$使得$ax_0+by_0=c$, 然后判断n是否能被c整除, 如果不可以
整除,则原方程无解. 否则, 令$k=n/c$,则$a\cdot kx_0 + b\cdot ky_0=kc=n$,此时$(kx_0,ky_0)$
即为原方程的解, 实际上, 从$(x_0,y_0)$我们扩展出了解系:
$X = x_0 + T_1 \cdot t = x_0 + b/gcd(a,b) \cdot t$
$Y = y_0 - T_2 \cdot t = y_0 - a/gcd(a,b) \cdot t$

$t$取任意整数,都可以得到一组解$(X_i,Y_i)$满足$aX_i+bY_i=n$成立. 下面证明为什么
$T_1 = b/gcd(a,b)$
$T_2 = a/gcd(a,b)$
(因为a,b,gcd(a,b)都是正整数, 所以$T_1,T_2$也都是正整数)

将$(X,Y)$代入原方程得: $aX+bY=n$
$\Rightarrow a(x_0+T_1\cdot t) + b(y_0-T_2\cdot t)=n$
$\Rightarrow ax_0 + by_0 + (aT_1-bT_2)\cdot t = n$
$\because ax_0+by_0=n, \therefore (aT_1-bT_2)\cdot t = 0$
当$t\not=0$时, 有$aT_1-bT_2=0$,即$aT_1=bT_2$, 我们要求最小的$T_1,T_2$
令$T=aT_1=bT_2$, 显然当$T$最小的时候, $T_1,T_2$也最小, 那么$T$最小为多少呢,
因为$T$既是a的倍数, 也是b的倍数, 所以$T$是a和b的公倍数, 所以当$T$为a和b的最小
公倍数时,即$T=ab/gcd(a,b)$时,$T_1,T_2$最小,此时有:
$aT_1=ab/gcd(a,b) \Rightarrow T_1=b/gcd(a,b)$
$bT_2=ab/gcd(a,b) \Rightarrow T_2=a/gcd(a,b)$
证毕.

下面用一个实例演示一下: $3x + 4y=1$
显然$(x_0,y_0)=(-1,1)$是原方程的一组解($3\cdot-1 + 4\cdot 1 = 1$),
$T_1 = b/gcd(a,b)=4/1 = 4$
$T_2 = a/gcd(a,b)=3/1 = 3$
取$t=1$,得:
$x_1 = x_0 + T_1\cdot1 = -1 + 4 = 3$
$y_1 = y_0 - T_2\cdot1 = 1 - 3 = -2$
$\Rightarrow x_1 + 4y_1 = 3\cdot3 + 4\cdot(-2) = 1$

取$t=2$,得:
$x_2 = x_0 + T_1*2=-1+4*2= 7$
$y_2 = y_0 - T_2*2=1-3*2=-5$
$\Rightarrow 3x_2+4y_2=3*7-4*5=1;$