### 前言
LaTeX是一套非常优秀的排版系统， 通过它排版的图书和论文会变得非常漂亮和易读。 而LaTeX在编写数学公式的易用性和通用性，使我对它产生了浓厚的兴趣。 这篇文章主要介绍了LaTeX公式编辑在MarkDown下的使用语法和方法。
以下的例子是在Sublime Text3上编写， 并测试的结果， 当然你也可以在任何引入MathJax的MarkDown编辑器上测试。
![](http://www.littlenote.cn/wp-content/uploads/2015/12/005.jpg)
### 1.显示方法
* 嵌入文字显示：`$...$`
eg: `$\sum^n_{i=1}x^i=1$` ==> $\sum^n_{i=1}x^i=1$ 
* 单行显示： `$$...$$`
eg: `$ $\sum^n_{i=1}x^i=1$ $` ==> $$\sum^n_{i=1}x^i=1$$
* 带序号显示：`\begin{equation}...\end{equation}`
eg: 
`\begin{equation}\sum^n_{i=1}x^i=1\end{equation}` ==> \begin{equation}\sum^n_{i=1}x^i=1\end{equation}
`\begin{equation}\x+y=z\end{equation}` ==> \begin{equation}x+y=z\end{equation}

### 2.通用显示规则

* `^` => 上标
* `_` => 下标
* `{}` => 包括
* `~` => 空格
* `\` => 转移符号

### 3.增强型显示规则

* \sqrt 求根
eg: `$\sqrt{x+y}$`==> $\sqrt{x+y}$
eg: `$\sqrt[3]{x+y}$`==> $\sqrt[3]{x+y}$
* \frac \over 分数形式
eg: `$\frac{a+1}{b+2}$` ==> $\frac{a+1}{b+2}$
eg: `${a+1}\over{b+2}$` ==> ${a+1}\over{b+2}$
* \sum 求和
eg: `$\sum$`==> $\sum$
* \prod 求积
eg: `$\prod^n_{i=1}i+1=1$` ==> $\prod^n_{i=1}i+1=1$
* \int 求积分
eg: `$\int x+1$` ==> $\int x+1$
* \iint 求积分
eg: `$\iint x+1$` ==> $\iint x+1$ 
* \bigcup 并集
eg: `$A\bigcup B$` ==> $A\bigcup B$
* \cup 并集
eg: `$A\cup B$` ==> $A\cup B$
* \cap 交集
eg: `$A\cap B$` ==> $A\cap B$
* \bigcap 交集
eg: `$A\bigcap B$` ==> $A\bigcap B$
* \to 箭头
eg: `$A\to B$` ==> $A\to B$
* \lim
eg: `$\lim_{0\to 100}$` ==>  $\lim_{0\to 100}$
* \ln
eg: `$\ln_{0\to 100}$` ==>  $\ln_{0\to 100}$
* \sin
eg: `$\sin x$` ==>  $\sin x$
* \cos
eg: `$\cos x$` ==>  $\cos x$
* \qquad 8m空格
* \quad 4m空格
* \times 乘号 
eg: `$a \times b$`=$a \times b$
* \div  除号	
eg: `$a\div b$`=$a\div b$
* \\{\\} 花括号显示
eg: `$\\{ hello \\}$` ==> $\\{ hello \\}$
*注意：在这里我测试的Sublime Text3编写输出的结果， 如果在其他MarkDown编辑器可能要使用单反斜杠*

* 小括号增强
eg: `$\left( hello\right)$` ==> $\left( hello\right)$
* 中括号增强
eg: ` $\left[hello\right]$` ==> $\left[hello\right]$
* 绝对值增强
eg: `$\left|hello\right|$` ==> $\left|hello\right|$
* 尖括号
eg: `$\langle hello\rangle$` ==> $\langle hello\rangle$
* 向上取整
eg: `$\lceil hello\rceil$` ==> $\lceil hello\rceil$
* 向下取整
eg: `$\lfloor hllo\rfloor$` ==> $\lfloor hllo\rfloor$

### 4.数学符号表一[^1][^2]

|符号|显示方法|符号|显示方法|符号|显示方法|
|--------|------------|------------|--------|------------|--------|
|$\pm$|`\pm`|$\mp$|`\mp`|$\times$|`\times`|
|$\div$|`\div`|$\ast$|`\ast`|$\star$|`\star`|
|$\circ$|`\circ`|$\bullet$|`\bullet`|$\cdot$|`\cdot`|
|$\oplus$|`\oplus`|$\oslash$|`\oslash`|$\dagger$|`\dagger`|
|$+$|`+`|$-$|`-`|$\cap$|`\cap`|
|$\cup$|`\cup`|$\ddagger$|`\ddagger`|$\diamond$|`\diamond`|
|$\uplus$|`\uplus`|$\sqcap$|`\sqcap`|$\sqcup$|`\sqcup`|
|$\vee$|`\vee`|$\wedge$|`\wedge`|$\setminus$|`\setminus`|
|$\wr$|`\wr`|$\ominus$|`\ominus`|$\odot$|`\odot`|
|$\bigtriangleup$|`\bigtriangleup`|$\bigtriangledown$|`\bigtriangledown`|$\triangleleft$|`\triangleleft`|
|$\triangleright$|`\triangleright`|$\lhd$|`\lhd`|$\rhd$|`\rhd`|
|$\unlhd$|`\unlhd`|$\unrhd$|`\unrhd`|$\otimes$|`\otimes`|
|$\bigcirc$|`\bigcirc`|$\amalg$|`\amalg`|$\sum$|`\sum`|
|$\prod$|`\prod`|$\coprod$|`\coprod`|$\int$|`\int`|
|$\oint$|`\oint`|$\bigcap$|`\bigcap`|$\bigcup$|`\bigcup`|
|$\bigsqcup$|`\bigsqcup`|$\bigvee$|`\bigvee`|$\bigwedge$|`\bigwedge`|
|$\bigodot$|`\bigodot`|$\bigotimes$|`\bigotimes`|$\bigoplus$|`\bigoplus`|
|$\biguplus$|`\biguplus`|$\leq$|`\leq`|$\geq$|`\geq`|
|$\equiv$|`\equiv`|$\prec$|`\prec`|$\succ$|`\cucc`|
|$\sim$|`\sim`|$\preceq$|`\preceq`|$\succeq$|`\succeq`|
|$\simeq$|`\simeq`|$\ll$|`\ll`|$\gg$|`\gg`|
|$\asymp$|`\asymp`|$\subset$|`\subset`|$\supset$|`\supset`|
|$\approx$|`\approx`|$\subseteq$|`\subseteq`|$\supseteq$|`\subseteq`|
|$\cong$|`\cong`|$\sqsubset$|`\sqsubset`|$\sqsupset$|`\sqsupset`|
|$\neq$|`\neq`|$\sqsubseteq$|`\sqsubseteq`|$\sqsupseteq$|`\sqsupseteq`|
|$\doteq$|`\doteq`|$\in$|`\in`|$\ni$|`\ni`|
|$\notin$|`\notin`|$\vdash$|`\vdash`|$\dashv$|`\dashv`|
|$:$|`:`|$\models$|`\models`|$\perp$|`\perp`|
|$\mid$|`\mid`|$\parallel$|`\parallel`|$\bowtie$|`\bowtie`|
|$\Join$|`\Join`|$\smile$|`\smile`|$\frown$|`\frown`|
|$\propto$|`\propto`|$<$|`<`|$>$|`>`|

### 5.数学符号表二

|符号|显示方法|符号|显示方法|符号|显示方法|
|--------|------------|------------|--------|------------|--------|
|$\arccos$|`\arccos`|$\arcsin$|`\arcsin`|$\arctan$|`\arctan`|
|$\arg$|`\arg`|$\cos$|`\cos`|$\cosh$|`\cosh`|
|$\cot$|`\cot`|$\coth$|`\coth`|$\csc$|`\csc`|
|$\deg$|`\deg`|$\det$|`\det`|$\dim$|`\dim`|
|$\exp$|`\exp`|$\gcd$|`\gcd`|$\hom$|`\hom`|
|$\inf$|`\inf`|$\ker$|`\ker`|$\lg$|`\lg`|
|$\lim$|`\lim`|$\liminf$|`\liminf`|$\limsup$|`\limsup`|
|$\ln$|`\ln`|$\log$|`\log`|$\max$|`\max`|
|$\min$|`\min`|$\Pr$|`\pr`|$\sec$|`\sec`|
|$\sin$|`\sin`|$\sinh$|`\sinh`|$\sup$|`\sup`|
|$\tan$|`\tan`|$\tanh$|`\tanh`|——|——|

### 5.箭头符号表

|符号|显示方法|符号|显示方法|符号|显示方法|
|--------|------------|------------|--------|------------|--------|
|$\leftarrow$|`\leftarrow`|$\longleftarrow$|`\longleftarrow`|$\Leftarrow$|`\Leftarrow`|
|$\Longleftarrow$|`\Longleftarrow`|$\rightarrow$|`\rightarrow`|$\longrightarrow$|`\longrightarrow`|
|$\Rightarrow$|`\Rightarrow`|$\Longrightarrow$|`\Longrightarrow`|$\leftrightarrow$|`\leftrightarrow`|
|$\longleftrightarrow$|`\longleftrightarrow`|$\Leftrightarrow$|`\Leftrightarrow`|$\Longleftrightarrow$|`\Longleftrightarrow`|
|$\mapsto$|`\mapsto`|$\longmapsto$|`\longmapsto`|$\hookleftarrow$|`\hookleftarrow`|
|$\hookrightarrow$|`\hookrightarrow`|$\leftharpoonup$|`\leftharpoonup`|$\rightharpoonup$|`\rightharpoonup`|
|$\leftharpoondown$|`\leftharpoondown`|$\rightharpoondown$|`\rightharpoondown`|$\rightleftharpoons$|`\rightleftharpoons`|
|$\leadsto$|`\leadsto`|$\uparrow$|`\uparrow`|$\downarrow$|`\downarrow`|
|$\Uparrow$|`\Uparrow`|$\Downarrow$|`\Downarrow`|$\updownarrow$|`\updownarrow`|
|$\Updownarrow$|`\Updownarrow`|$\nwarrow$|`\nwarrow`|$\nearrow$|`\nearrow`|
|$\swarrow$|`\swarrow`|$\searrow$|`\searrow`|——|——|

### 6.特殊符号表

|符号|显示方法|符号|显示方法|符号|显示方法|
|--------|------------|------------|--------|------------|--------|
|$\S$|`\S`|$\aleph$|`\aleph`|$\LaTeX$|`\LaTeX`|
|$\ldots$|`\ldots`|$\ddots$|`\ddots`|$\cdots$|`\cdots`|
|$\vdots$|`\vdots`|$\imath$|`\imath`|$\jmath$|`\jmath`|
|$\ell$|`\ell`|$\wp$|`\wp`|$\Re$|`\Re`|
|$\Im$|`\Im`|$\Diamond$|`\Diamond`|$\diamondsuit$|`\diamondsuit`|
|$\prime$|`\prime`|$\emptyset$|`\emptyset`|$\nabla$|`\nabla`|
|$\surd$|`\surd`|$\top$|`\top`|$\bot$|`\bot`|
|$\backslash$|`\backslash`|$\partial$|`\partial`|$\infty$|`\infty`|
|$\triangle$|`\triangle`|$\heartsuit$|`\heartsuit`|$\circledS$|`\circledS`|
|$\hbar$|`\hbar`|$\forall$|`\forall`|$\exists$|`\exists`|
|$\neg$|`\neg`|$\flat$|`\flat`|$\natural$|`\natural`|
|$\sharp$|`\sharp`|$\angle$|`\angle`|$\mho$|`\mho`|
|$\Box$|`\Box`|$\clubsuit$|`\clubsuits`|$\spadesuit$|`\spadesuit`|

### 7.希腊字母(Greek Letters)显示表

|拉丁字母|小写显示方法|大写显示方法|大写字母|
|--------|------------|------------|--------|
|$\alpha$|`\alpha`      |——     |——|
|$\beta$|`\beta`     |——     |——|
|$\gamma$|`\gamma`     |`\Gamma`     |$\Gamma$ |
|$\delta$|`\delta`      |`\Delta`      |$\Delta$|
|$\epsilon$|`\epsilon`    |——      |——|
|$\zeta$|`\zeta`     |——      |——|
|$\eta$|`\eta`     |——      |——|
|$\theta$|`\theta`      |`\Theta`      |$\Theta$|
|$\iota$|`\iota`    |——      |——|
|$\kappa$|`\kappa`    |——      |——|
|$\lambda$|`\lambda`      |`\lambda`     |$\lambda$|
|$\mu$|`\mu`     |——      |——|
|$\nu$|`\nu`     |——      |——|
|$\xi$|`\xi`    |`\Xi`    |$\Xi$|
|$\omicron$|`\omicron`    |——      |——|
|$\pi$|`\pi`   |`\Pi`    |$\Pi$|
|$\rho$|`\rho`   |——      |——|
|$\sigma$|`\sigma`    |`\Sigma`    |$\Sigma$|
|$\tau$|`\tau`     |——      |——|
|$\upsilon$|`\upsilon`   |`\Upsilon` |$\Upsilon$|
|$\phi$|`\phi`  |`\Phi` |$\Phi$|
|$\chi$|`\chi`    |——      |——|
|$\psi$|`\psi`    |`\Psi`    |$\Psi$|
|$\omega$|`\omega`    |`\Omega`     |$\Omega$|

*注意：将小写字母的首字母大写表示为大写拉丁字母*

![](http://www.littlenote.cn/wp-content/uploads/2015/12/gongshi.jpg)

### 8.常用结构例子[^3]

#### 例1
```html
\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
 \end{align}
```
\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}

#### 例2
```html
\begin{matrix}
        1 & x & x^2 \\\
        1 & y & y^2 \\\
        1 & z & z^2 \\\
\end{matrix}

\begin{pmatrix}
        1 & x & x^2 \\\
        1 & y & y^2 \\\
        1 & z & z^2 \\\
\end{pmatrix}

\begin{bmatrix}
        1 & x & x^2 \\\
        1 & y & y^2 \\\
        1 & z & z^2 \\\
\end{bmatrix}

\begin{Bmatrix}
        1 & x & x^2 \\\
        1 & y & y^2 \\\
        1 & z & z^2 \\\
\end{Bmatrix}

\begin{vmatrix}
        1 & x & x^2 \\\
        1 & y & y^2 \\\
        1 & z & z^2 \\\
\end{vmatrix}

```
<a href="http://www.littlenote.cn/wp-content/uploads/2016/01/text1.jpg" rel="attachment wp-att-106"><img src="http://www.littlenote.cn/wp-content/uploads/2016/01/text1.jpg" alt="text1" width="134" height="639" class="aligncenter size-full wp-image-106" /></a>

#### 例3
```html
\left[
    \begin{array}{cc|c}
      1&2&3\\\
      4&5&6
    \end{array}
\right]
```
<a href="http://www.littlenote.cn/wp-content/uploads/2016/01/text2.jpg" rel="attachment wp-att-107"><img src="http://www.littlenote.cn/wp-content/uploads/2016/01/text2.jpg" alt="text2" width="143" height="89" class="aligncenter size-full wp-image-107" /></a>

#### 例4
```html
f(n) =
\begin{cases}
n/2,  & \text{if $n$ is even} \\\
3n+1, & \text{if $n$ is odd}
\end{cases}

\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\\
\hline
1 & 0.24 & 1 & 125 \\\
2 & -1 & 189 & -8 \\\
3 & -20 & 2000 & 1+10i
\end{array}

```
<a href="http://www.littlenote.cn/wp-content/uploads/2016/01/text3.jpg" rel="attachment wp-att-108"><img src="http://www.littlenote.cn/wp-content/uploads/2016/01/text3.jpg" alt="text3" width="282" height="192" class="aligncenter size-full wp-image-108" /></a>

### 参考文献

[^1]:  [LaTeX符号集文档](http://www.littlenote.cn/wp-content/uploads/2016/01/LaTeX_Symbols.pdf)

[^2]:  [LaTeX符号表](http://blog.sina.com.cn/s/blog_642075770100u0np.html)

[^3]:  [MathJax基本结构](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)
