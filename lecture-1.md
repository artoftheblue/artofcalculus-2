# Лекция 1, 10.09.2024

## Кратные интегралы

```{prf:definition}
Замкнутым брусом (промежутком, координатным промежутком) в $\mathbb{R^n}$ будем называть множество $I=\{x\in \mathbb{R}^n|a_i\leq x\leq a_i,i=1,\dots, n\}=[a_1, b_1]\times\dots\times[a_n,b_n]$

```

```{note} Замечание
$$I=\{a_1, b_1\}\times\dots\times\{a_n,b_n\}$$

* $\{\dots\}$ — отрезок, интервал, полуинтервал
```

```{prf:definition}
**Мерой бруса** будем называть его объём: $\mu(I)=|I|=\prod^n_{i=1}(b_i-a_i)$
```

### Свойства меры бруса в $\mathbb{R}^n$

1. **Однородность** 

$$\mu(I_{\lambda a,\lambda b})=\lambda^n\mu(I_{a,b}),\lambda\geq0$$

$$a=\{a_1,\dots,a_n\}, b=\{b_1,\dots,b_n\}$$

2. **Аддитивность**

Пусть $I, I_1,\dots,I_k\colon I=\bigcup^k_{i=1}I_i$. $I_1,\dots,I_k$ не имеют общих точек $\implies |I|=\sum^k_{i=1}|I_i|$

3. **Монотонность**

### Разбиения

$I\subset\bigcup^k_{i=1}I_i$ — покрыт конечной системой брусов $\implies |I|<\sum^k_{i=1}|I_i|$

```{prf:definition}
$I$ — замкнутый невырожденный брус и $I=\bigcup_{i=1}^kI_i$, где $I_i$ попарно не имеет общих внутренних точек, тогда набор $\mathbb{T}=\{I_i\}^k_{i=1}$ будем называть **разбиением бруса** $I$.
```

```{prf:definition}
Диаметром произвольного ограниченного множества $M\subset \mathbb{R}^n$ будем называть 

$$d(M)=\sup_{x,y\in M}\|x-y\|$$

где

$$\|x-y\|=\sqrt{\sum^n_{i=1}(x_i-y_i)^2}$$
```

```{prf:definition}
**Масштабом** разбиения $\mathbb{T}=\{I_i\}^k_{i=1}$ будем называть число $\lambda(\mathbb{T})=\triangle_{\mathbb{T}}=\max_{i\leq i\leq k}d(I_i)$.
```

$\forall I_i$ выбраны точки $\xi_i\in I_i$

```{prf:definition}
Набор $\boldsymbol{\xi}=\{\xi_i\}^k_{i=1}$ будем называть **отмеченными точками**.
```

```{prf:definition}
$(\mathbb{T},\boldsymbol{\xi})$ будем называть **размеченным разбиением**.
```

### Интегральные суммы

$I$ — невырожденный замкнутый брус

$f\colon I\mapsto\mathbb{R}$ определена на $I$.

```{prf:definition}
**Интегральной суммой Римана** функции $f$ на $(\mathbb{T},\boldsymbol{\xi})$ будем называть величину $\sigma(f,\mathbb{T},\boldsymbol{\xi}):=\sum^{k}_{i=1}f(\xi_i)|I_i|$.
```

```{prf:definition}
Будем говорить, что функция $f$ **интегрируема (по Риману)** на замкнутом брусе $I\ (f\colon I\mapsto\mathbb{R})$, если $\exists A\in\mathbb{R},\forall\varepsilon>0,\exists\delta>0,\forall(\mathbb{T},\boldsymbol{xi})\colon \triangle_{\mathbb{T}}<\delta$ верно, что $|\sigma(f,\mathbb{T},\xi)-A|<\varepsilon$. Тогда

$$A=\int\limits_I f(x)dx=\int\underset{I}\ldots\int f(x_1,\ldots,x_n)dx_1\dots dx_n$$

Обозначение: $f\in R(I)$
```

### Примеры

```{prf:example} $f=\text{const}$
$\forall(\mathbb{T},\boldsymbol{\xi}),\sigma(f,\mathbb{T},\boldsymbol{\xi})=\sum^k_{i=1}\text{const}|I_i|=\text{const}|I|$

$$\int\limits_I f(x)dx=\text{const}|I|$$
```

```{prf:example} Неинтегрируемая функция
$I=[0,1]^n$

$$f=\begin{cases}
1, & \forall i=\overline{1,\dots,n}, & x_i\in\mathbb{Q}\\
0, & \text{иначе}
\end{cases}$$

$\forall\mathbb{T}$ можно выбрать $\xi_i\in\mathbb{Q}$, тогда для такого размеченного разбиения $(\mathbb{T},\boldsymbol{\xi})$

$$\sigma(f,\mathbb{T},\boldsymbol{\xi})=\sum^k_{i=1}|I_i|=|I|=1$$

---

$\forall\mathbb{T}$ можно выбрать $\hat\xi_i\not\in\mathbb{Q}$, тогда 

$$\sigma(f,\mathbb{T},\hat{\boldsymbol{\xi}})=\sum^k_{i=1}0\cdot|I_i|=0\implies f\not\in R(I)$$
```

```{prf:example}
$$\iint\limits_{\overset{\scriptstyle 0\leq x\leq 1}{0\leq y\leq 1}}xydxdy$$

$f=xy, |I_i|=\frac{1}{n^2}$

$$\sigma(f,\mathbb{T},\boldsymbol{\xi})=\sum_{i=1}^n=\sum_{i=1}^n\sum_{j=1}^n\frac{i}{n}\frac{j}{n}\frac{1}{n^2}=\frac{1}{n^4}\sum_{i=1}^n i\sum_{j=1}^n j\\=\frac{(n+1)n}{2n^4}\sum^n_{i=1}i=\frac{(n+1)^2n^2}{4n^4}\xrightarrow{n\to\infty}\frac{1}{4}$$

```