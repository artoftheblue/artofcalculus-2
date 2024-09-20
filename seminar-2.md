# Семинар-2, 16.09.2024

## Задача 1

Доказать, что мера $n$-мерного промежутка

### Подзадача А 

$n$-однородна: $|I_{\lambda a,\lambda b}|=\lambda^n|I_{a,b}|$

---

$$I=[a_1, b]\times[a_i,b_2]\times\ldots\times[a_n,b_n]$$

$$\mu(I)=\sqcap^n_{k=1}(b_k-a_k)$$
$$\mu(I_{\lambda a,\lambda b})=\sqcap(\lambda b_k-\lambda a_k)=\dots=\lambda^n\sqcap(b_k-a_k)$$




### Подзадача B

аддитивна: $|\bigsqcup_{i=1}^K|=\sum^K_{i=1}|I_i|$

Если $\bigsqcup_{i=1}^k I_i$ есть брусок, то $\mu(\bigsqcup I_k)=\sum\mu(I_k)$

### Подзадача C

удовлетворяет свойству: если $I\subset\bigcup_{i=1}^K I_i$, то $|I|\leq\sum^K_{i=1}|I_i|$

Есть много брусков, которые пересекаются, некоторые из которых могут встречаться несколько раз. Если мы построим сеточное разбиение, то мы получим в левой части элементы сетки, лежащие в объединении по одному разу, а в правой части по несколько раз. Очевидно, что в таком случае LHS включается в RHS.

## Задача 2

Может ли множество лебеговой меры нуль содержать внутренние точки?

Покроем множество $A$ брусками и возьмём минимальное покрытие aka минимальную верхнюю границу — покрытие с минимальным количеством пересечений и выходов за границу множества:

$$\mu^{\text{ext}}(A)=\inf_{\text{покрытие}}\sum^n_{k=1}\mu(I_k)$$

```{prf:definition}
$x$ — внутренняя точка для $F$, если $\exists\varepsilon>0\colon[x_1-\varepsilon,x_1+\varepsilon]\times[x_2-\varepsilon,x_2+\varepsilon]\times\ldots\times[x_n-\varepsilon,x_n+\varepsilon]\subseteq A$
```

```{seealso} 3 плохих парня
1. рациональные / иррациональные числа
2. канторово множество
3. множество Витали
```

```{seealso} Множество Витали
Живём в $\mathbb{R}^1$.
$A$ — иррациональные числа на отрезке $[0, 1]$.
$B$ — рациональные числа на отрезке $[0, 1]$.

$\mu^{\text{ext}}(A)=1$

$\mu^{\text{ext}}(B)=0$
```

```{seealso} Канторово множество.
$$\begin{align*}
&A_0=[0, 1]\\
&A_1=[0,\tfrac{1}{3}] \cup [\tfrac{2}{3}, 1]\\
&A_2=[0,\tfrac{1}{9}] \cup [\tfrac{2}{9}, \tfrac{3}{9}] \cup [\tfrac{6}{9},\tfrac{7}{9}] \cup [\tfrac{8}{9}, 1]\\
&\ \vdots
\end{align*}$$

$$K=\bigcap^\infty_{i=1}A-i$$

* $\frac{1}{3}\in K$
* $\frac{2}{3}\in K$
* $\frac{1}{2}\not\in K$

В $K$ континуум точек. Можем выбирать, куда идти, вправо или влево.

$$\begin{align*}&RRRRRRR&\dots\\&RLRLRLR&\dots\end{align*}$$

```

```{seealso} Множество Витали
Точки имеют один цвет, если $|a-b|\in\mathbb{Q}$.

Тогда 

$$\frac{1}{2}\sim\frac{1}{3}\sim\frac{5}{6}\sim\frac{6}{11}\sim\dots$$
$$\frac{\pi}{6}\sim\frac{\pi}{6}+\frac{1}{4}\sim\frac{\pi}{6}-\frac{1}{100}\sim\frac{\pi}{6}+\frac{1}{50}\sim\dots$$

т. к. эти классы эквивалентности счётны, то цветов континуум.

Если мы возьмём одну точку и пробежим все её повороты по окружности, где координаты изменяются полярно от 0 до 1, тогда мы покроем все точки в классе эквивалентности.

$$\bigcup^{\infty}_{i=1}U_i=\text{Окр}$$

$$\mu(V_i)=\text{const}$$
```

## Листок 2, 3а

$$\int\limits^2_1dy\int\limits^2_ydx\int\limits^{1/(xy)}_0\frac{dz}{x(1+x^2y^2z^2)}$$

$$\int\limits^2_1 dy\int dz\int\frac{dx}{x(1+x^2y^2z^2)}$$

$$\int dz\int dx\int\frac{dy}{x(1+x^2y^2z^2)}$$

* $y\in[1,2]$
* $x\in[y,2]$
* $z\in[0,\frac{1}{xy}]$