[TOC]

# 上下标，正负无穷
|     数学表达式    |   LaTex代码   |
|:---------------:|:-------------:|
|      $x^2$      |      x^2      |
|      $y_1$      |      y_1      |
|$\overline{x+y}$ | \overline{x+y}|
|$\underline{a+b}$|\underline{a+b}|
|     $\infty$    |     \infty    |
|    $-\infty$    |    -\infty    |

# 加减乘除
|   数学表达式   |  LaTex代码 |
|:------------:|:----------:|
|  $a+b-c*d$   |   a+b-c*d  |
|  $a\div(b)$  |  a\div(b)  |
|  $a\pm(b)$   |   a\pm(b)  |

# 根号，分式
|   数学表达式   |  LaTex代码 |
|:------------:|:----------:|
|$\frac{a}{b}$ | \frac{a}{b}|
|  $\sqrt{b}$  |  \sqrt{b}  |
|$\sqrt[n]{b}$ |\sqrt[n]{b} |

# 向量
|      数学表达式      |     LaTex代码    |
|:------------------:|:----------------:|
|      $\vec{a}$     |      \vec{a}     |
|$\overrightarrow{A}$|\overrightarrow{A}|
| $\overleftarrow{A}$|\overleftarrow{A} |

# 三角函数
|     数学表达式    |   LaTex代码   |
|:---------------:|:-------------:|
|  $\sin(\theta)$ |  \sin(\theta) |
|$\arcsin(\theta)$|\arcsin(\theta)|
|  $\cos(\theta)$ |  \cos(\theta) |
|$\arccos(\theta)$|\arccos(\theta)|
|  $\tan(\theta)$ |  \tan(\theta) |
|  $\cot(\theta)$ |  \cot(\theta) |

# 积分,极限,求和,乘积
|             数学表达式            |           LaTex代码           |
|:-------------------------------:|:-----------------------------:|
|    $\int_{1}^{5}x\mathrm{d}x$   |    \int_{1}^{5}x\mathrm{d}x   |
|$\lim_{a\rightarrow+\infty}{a+b}$|\lim_{a\rightarrow+\infty}{a+b}|
|      $\sum_{i=1}^{n}{a_i}$      |      \sum_{i=1}^{n}{a_i}      |
|      $\prod_{i=1}^{n}{a_i}$     |      \prod_{i=1}^{n}{a_i}     |

# 点，省略号
| 数学表达式 | LaTex代码 |
|:--------:|:---------:|
|  $\cdot$ |   \cdot   |
| $\cdots$ |   \cdots  |
| $\ldots$ |   \ldots  |
| $\vdots$ |   \vdots  |
| $\ddots$ |   \ddots  |

# 希腊字母
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

# 关系运算符
|数学表达式|LaTex代码|
|:------:|:------:|
| $\leq$ |  \leq  |
| $\geq$ |  \geq  |

# 公式
```
使用\begin{cases}…\end{cases}生成，每一行以\\结尾表示换行，元素间以&间隔
```
```
D(x) = \begin{cases}
\lim\limits_{x \to 0} \frac{a^x}{b+c}, & x<3 \\
\pi, & x=3 \\
\int_a^{3b}x_{ij}+e^2 \mathrm{d}x,& x>3 \\
\end{cases}
```
$$
D(x) = \begin{cases}
\lim\limits_{x \to 0} \frac{a^x}{b+c}, & x<3 \\
\pi, & x=3 \\
\int_a^{3b}x_{ij}+e^2 \mathrm{d}x,& x>3 \\
\end{cases}
$$

# 矩阵
## <h4>简单矩阵</h4>
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
## <h4>带括号的矩阵</h4>
```
在\begin{}之前和\end{}之后添加左右括号的代码或改变\begin{matrix}和\end{matrix}中{matrix}
```
1. 大括号
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
2. 中括号
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
3. 小括号
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
## <h4>包含希腊字母与省略号的矩阵</h4>
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

# 行列式
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

# 表格
## <h4>表格</h4>
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
## <h4>真值表</h4>
$$
\begin{array} {c c | c}
    A & B & F \\
    \hline 0 & 0 & 0 \\
	0 & 1 & 1 \\
	1 & 0 & 1 \\
	1 & 1 & 1 \\
\end{array}
$$