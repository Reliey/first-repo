# 分割线

---

# 加粗，斜体和删除线
**重点加粗**

*斜体*

~~删除线~~

# 快捷键

选中文本之后, 按下 Ctrl + B 可以给选中文本加粗.

同理 Ctrl + I 可以让选中文本变为斜体.

Ctrl + M 进入数学模式

Ctrl + Alt + V 粘贴图片

Ctrl + Shift + Alt + E 计算当前选中表达式, 用等号连接并输出
# markdown preview enhanced 扩展功能

==高亮==

任务列表:

- [x] 已经完成的事 1
- [x] 已经完成的事 2
- [x] 已经完成的事 3
- [ ] 仍未完成的事 4
- [ ] 仍未完成的事 5

# 快捷键

要进行缩进 (书写嵌套列表), 你可以使用 VS Code 的快捷键 Ctrl + [ 和 Ctrl + ].

这个快捷键可以将代码向左或向右进行缩进!

# 引用和代码
引用文本:

> 引用别人说的话
> 就这样写

代码块：使用反引号 `（~ 键）

``` python {.line-numbers}
print("Hello, World!")
```

# 注释
快捷键 Ctrl + \ 将当前行注释

# 数学公式支持
行内公式: 

单位圆 $x^2+y^2=1$

公式块:

$$
\begin{cases}
x=\rho\cos\theta \\
y=\rho\sin\theta \\
\end{cases}
$$

1. 上标和下标  
上标 $x^2 + y^{12} = 1$
下标 $x_1 + y_{12} = 1$
HyperSnips 自动扩展：

         xsr  =>  x^{2}
         xtp  =>  x^{...}
         x1  =>  x_1
         xii  =>  x_i
         xsb  =>  x_{...}

2. 分式
较小的行内行分数 $\frac{1}{2}$
展示型的分式 $\displaystyle\frac{x+1}{x-1}$
其中 \displaystyle 用于将行内展示转为块状展示
HyperSnips 自动扩展：

         1/  =>  \frac{1}{...}
         (1 + 2)/  =>  \frac{(1+2)}{...}
         //  =>  \frac{...}{...}

3. 根式
开平方 $\sqrt{2}$
开 $n$ 次方 $\sqrt[n]{2}$
HyperSnips 自动扩展：

       hsq  =>  \sqrt{...}

4. 空格
数学公式中的 空格和换行 都会在编译时 被忽略，想要实现「空格」的效果，需要用特别的命令
         紧贴 $a\!b$

         没有空格 $ab$

         小空格 $a\,b$

         中等空格 $a\;b$

         大空格 $a\ b$

         quad 空格 $a\quad b$

         两个 quad 空格 $a\qquad b$

5. 累加，累乘和积分
   
累加 $\sum_{k=1}^n\frac{1}{k}  \quad  \displaystyle\sum_{k=1}^n\frac{1}{k}$

累乘 $\prod_{k=1}^n\frac{1}{k}  \quad  \displaystyle\prod_{k=1}^n\frac{1}{k}$

积分 $\displaystyle \int_0^1x{\rm d}x  \quad  \iint_{D_{xy}}  \quad  \iiint_{\Omega_{xyz}}$
    HyperSnips 自动扩展：
         sum  =>  \sum_{...}

         prod  =>  \prod_{<n=1>}^{<\infty>} ...

         int  =>  \int

         dint  =>  \int_{<-\infty>}^{<\infty>} ... \mathrm{d}x

6. 括号
   
圆括号 $\displaystyle \left(\sum_{k=1}^{n}\frac{1}{k} \right)^2$

方括号 $\displaystyle \left[\sum_{k=1}^{n}\frac{1}{k} \right]^2$

花括号 $\displaystyle \left\{\sum_{k=1}^{n}\frac{1}{k} \right\}^2$

尖括号 $\displaystyle \left\langle\sum_{k=1}^{n}\frac{1}{k} \right\rangle^2$
HyperSnips 自动扩展：
         @(  =>  \left( ... \right)

         @[  =>  \left[ ... \right]

         @{  =>  \left\{ ... \right\}

         @<  =>  \left< ... \right>

         set  =>  \{ ... \}

7. 多行算式对齐
居中:

   $$
   \begin{aligned}
   y &=(x+5)^2-(x+1)^2 \\
   &=(x^2+10x+25)-(x^2+2x+1) \\
   &=8x+24 \\
   \end{aligned}
   $$

   左对齐:

   $
   \begin{aligned}
   y &=(x+5)^2-(x+1)^2 \\
   &=(x^2+10x+25)-(x^2+2x+1) \\
   &=8x+24 \\
   \end{aligned}
   $

   HyperSnips 自动扩展：

        ali  =>
         \begin{aligned}
         ... \\
         \end{aligned}

8. 方程组
$$
\begin{cases}
k_{11}x_1+k_{12}x_2+\cdots+k_{1n}x_n=b_1 \\
k_{21}x_1+k_{22}x_2+\cdots+k_{2n}x_n=b_2 \\
\cdots \\
k_{n1}x_1+k_{n2}x_2+\cdots+k_{nn}x_n=b_n \\
\end{cases}
$$

     HyperSnips 自动扩展：

          case  =>
         \begin{cases}
         ... \\
         \end{cases}

9.矩阵
$$
\begin{pmatrix}
1 & 1 & \cdots & 1 \\
1 & 1 & \cdots & 1 \\
\vdots & \vdots & \ddots & \vdots \\
1 & 1 & \cdots & 1 \\
\end{pmatrix}
$$

$$
\begin{bmatrix}
1 & 1 & \cdots & 1 \\
1 & 1 & \cdots & 1 \\
\vdots & \vdots & \ddots & \vdots \\
1 & 1 & \cdots & 1 \\
\end{bmatrix}
$$ 

行列式: 

$$
\begin{vmatrix}
1 & 1 & \cdots & 1 \\
1 & 1 & \cdots & 1 \\
\vdots & \vdots & \ddots & \vdots \\
1 & 1 & \cdots & 1 \\
\end{vmatrix}
$$

HyperSnips 自动扩展：

      bmat2  =>  \begin{bmatrix} ... & ... \\ ... & ... \\\end{bmatrix}

      vec2  =>  \begin{pmatrix} ... \\ ... \\\end{pmatrix}

10.特殊字符

      alpha  =>  \alpha

      Sigma  =>  \Sigma

11.公式编号与引用

$$
x+2 \tag{1.2}
$$

$$
\begin{equation}
x^n+y^n=z^n
\end{equation}
$$

由公式 $(1.2)$ 可得到结论
