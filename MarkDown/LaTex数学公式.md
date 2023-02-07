# # 上下标，正负无穷
|数学表达式 |LaTex代码|
|:-------:|:-------:|
|  $x^2$  |   x^2   |
|  $y_1$  |   y_1   |
|$\infty$ |  \infty |
|$-\infty$| -\infty |

# # 加减乘除，分号，根号，省略号
|   数学表达式   |  LaTex代码 |
|:------------:|:----------:|
|  $a+b-c*d$   |   a+b-c*d  |
|  $a\div(b)$  |  a\div(b)  |
|  $a\pm(b)$   |   a\pm(b)  |
|$\frac{a}{b}$ | \frac{a}{b}|
|  $\sqrt{b}$  |  \sqrt{b}  |
|    $\cdot$   |    \cdot   |
|   $\cdots$   |   \cdots   |

# # 三角函数
|     数学表达式    |   LaTex代码   |
|:---------------:|:-------------:|
|  $\sin(\theta)$ |  \sin(\theta) |
|$\arcsin(\theta)$|\arcsin(\theta)|
|  $\cos(\theta)$ |  \cos(\theta) |
|$\arccos(\theta)$|\arccos(\theta)|
|  $\tan(\theta)$ |  \tan(\theta) |
|  $\cot(\theta)$ |  \cot(\theta) |

# # 矢量，累加累乘，极限
|             数学表达式            |           LaTex代码           |
|:-------------------------------:|:-----------------------------:|
|            $\vec{F}$            |            \vec{F}            |
|      $\sum_{i=1}^{n}{a_i}$      |      \sum_{i=1}^{n}{a_i}      |
|      $\prod_{i=1}^{n}{a_i}$     |      \prod_{i=1}^{n}{a_i}     |
|$\lim_{a\rightarrow+\infty}{a+b}$|\lim_{a\rightarrow+\infty}{a+b}|

# # 希腊字母
|   数学表达式  | LaTex代码 |
|:-----------:|:--------:|
|   $\alpha$  |  \alpha  |
|   $\beta$   |   \beta  |
|   $\gamma$  |  \gamma  |
|   $\delta$  |  \delta  |
|  $\epsilon$ | \epsilon |
|$\varepsilon$|varepsilon|
|    $\eta$   |   \eta   |
|   $\theta$  |  \theta  |
|   $\kappa$  |  \kappa  |
|   $\iota$   |   \iota  |
|   $\zeta$   |   \zeta  |
|  $\lambda$  |  \lambda |
|    $\mu$    |    \mu   |
|    $\phi$   |   \phi   |
|    $\pi$    |    \pi   |
|    $\rho$   |   \rho   |
|    $\xi$    |    \xi   |
|    $\nu$    |    \nu   |
|  $\upsilon$ | \upsilon |
|  $\varphi$  |  \varphi |
|   $\chi$    |   \chi   |
|   $\psi$    |   \psi   |
|   $\omega$  |  \omega  |

# # 关系运算符
|数学表达式|LaTex代码|
|:------:|:------:|
| $\leq$ |  \leq  |
| $\geq$ |  \geq  |

# # 矩阵
1.简单矩阵
```
使用\begin{matrix}…\end{matrix}生成，每一行以\\结尾表示换行，元素间以&间隔，表示序号\tag{1}（右边的序号）
```
```
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9 
\end{matrix} \tag{1}
```
$$
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9 
\end{matrix} \tag{1}
$$

2.带左右括号的矩阵(大中小括号)
```
在\begin{}之前和\end{}之后添加左右括号的代码或改变\begin{matrix}和\end{matrix}中{matrix}
```
大括号：
```
\left\{
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right\}
```
$$
\left\{
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right\}
$$
```
\begin{Bmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{Bmatrix}
```
$$
\begin{Bmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{Bmatrix}
$$
中括号：
```
\left[
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right]
```
$$
\left[
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right]
$$
```
\begin{bmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{bmatrix}
```
$$
\begin{bmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{bmatrix}
$$
小括号：
```
\left(
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right)
```
$$
\left(
\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{matrix}
\right)
$$

3.包含希腊字母与省略号的矩阵
```
行省略号\cdots，列省略号\vdots，斜向省略号（左上至右下）\ddots
```
```
\left\{
\begin{matrix}
    1 & 2 & \cdots & 5 \\
    6 & 7 & \cdots & 10 \\
    \vdots & \vdots & \ddots & \vdots \\
    \alpha & \alpha+1 & \cdots & \alpha+4 
\end{matrix}
\right\}
```
$$
\left\{
\begin{matrix}
    1 & 2 & \cdots & 5 \\
    6 & 7 & \cdots & 10 \\
    \vdots & \vdots & \ddots & \vdots \\
    \alpha & \alpha+1 & \cdots & \alpha+4 
\end{matrix}
\right\}
$$

# # 行列式
```
与矩阵类似
```
```
\begin{vmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{vmatrix}
```
$$
\begin{vmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
\end{vmatrix}
$$

# # 表格
1.简易表格
```
使用\begin{array}…\end{array}生成，每一行以\\结尾表示换行，元素间以&间隔
定义式：例：{|c|c|c|}，其中c l r 分别代表居中、左对齐及右对齐
分割线：
①竖直分割线：在定义式中插入 |，||表示两条竖直分割线
②水平分割线：在下一行输入前插入\hline
```
```
\begin{array} {|c|c|c|}
    \hline 2 & 9 & 4 \\
    \hline 7 & 5 & 3 \\
    \hline 6 & 1 & 8 \\
    \hline
\end{array}
```
$$
\begin{array} {| c | c | c |}
    \hline 2 & 9 & 4 \\
    \hline 7 & 5 & 3 \\
    \hline 6 & 1 & 8 \\
    \hline
\end{array}
$$
2.真值表
$$
\begin{array} {c c | c}
    A & B & F \\
    \hline 0 & 0 & 0 \\
	0 & 1 & 1 \\
	1 & 0 & 1 \\
	1 & 1 & 1 \\
\end{array}
$$