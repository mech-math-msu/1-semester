---
title: Теория чисел
---

# Делимость 

## Теоремы о делении с остатком


:::: {#definition-1}

**Определение:**  Пусть $a \in \mathbb{Z}, b \in \mathbb{Z}, a \ne 0$. Если $\exists c \in \mathbb{Z}$, такое что $b = ac$, то $a\,\,|\,\,b$    ($a$ *делит* $b$)

::::

### Простейшие свойства

$\forall a, b, c \in \mathbb{Z}$


1. $1\,\,|\,\,a$
2. Если $a \ne 0$, то $a\,\,|\,\,a$
3. Если $a\,\,|\,\,b$, то $a\,\,|\,\,bc$
4. Если $a\,\,|\,\,b$ и $b\,\,|\,\,с$, то $a\,\,|\,\,c$
5. Если $a\,\,|\,\,b$ и $a\,\,|\,\,с$, то $a\,\,|\,\,(b \pm c)$
6. Если $a\,\,|\,\,b$, то $|a| \le |b|$


### Простейшие функции

:::: {#definition-2}

**Определение:** (*(нижняя) целая часть числа*) $[x] = \max \{z \in \mathbb{Z}: z \le x\} = \lceil x \rceil$

::::

> $[-4.5] = -5$<br>
> $[5.6] = [5]$


:::: {#definition-3}

**Определение:** (*дробная часть числа*) $\{x\} = x - [x]$

::::


:::: {#definition-4}

**Определение:** (*верхняя целая часть числа*) $\lfloor x \rfloor = \min \{z \in \mathbb{Z}: z \ge x\}$

> $\lfloor -4.5 \rfloor = -4$ <br>
> $\lfloor 5.5 \rfloor = [6]$

::::

:::: {#definition-5}

**Определение:** (*расстояние до ближайшего целого*) $\displaystyle ||x|| = \min_{a \in \mathbb{Z}} |x - a|$

::::


**Упражнение:**<a name="exercise-1"></a> $||x|| = \min (\{x\}, 1 - \{x\})$

**Упражнение:**<a name="exercise-2"></a> $||x + y|| \le ||x|| + ||y||$

:::: {#theorem-1}

**Теорема:**  (*обычное деление с остатком*)
$$\forall a \in \mathbb{Z},\, b \in \mathbb{N}\,\,\,\, \exists !\,\, q, r \in \mathbb{Z}: a = bq + r,\,\, 0 \le r < b$$

*Доказательство:*

*Существование*:
1. Если $a\,\,|\,\,b$, то $q = \frac{a}{b} \in \mathbb{Z},\,\,\,\,r = 0$.
2. Иначе рассмотрим множество $$M=\{z \in \mathbb{N}: z = a - bq, q \in \mathbb{Z}\}$$
Докажем, что $M \ne \varnothing$ рассмотрим $q_0 = -|a| - 1$
$$z = a - bq_0 = a + b(|a| + 1) \ge a + |a| + 1 \ge 1 \Rightarrow z \in \mathbb{N} \Rightarrow z \in M$$
Следовательно, по аксиоме Архимеда $\exists r = \min M = a - bq$.
$$r_1 = r - b = a - b(q + 1), \,\,\,\, b \in \mathbb{N} \Rightarrow r_1 < r \Rightarrow r_1 \not\in M \Rightarrow $$    $$r_1 \le 0, \,\,\,\, r \ne 0 \Rightarrow r_1 < 0 \Rightarrow 0 \le r < b \,\,\,\,\blacksquare$$

*Единственность*:

Пусть: $$ a = bq_0 + r_0$$
$$a = bq_1 + r_1 \Rightarrow$$
$$0 = b(q_1 - q_0) + (r_1 - r_0) \Rightarrow b\,\,|\,\,(r_0 - r_1) \Rightarrow b \le |r_0 - r_1|$$
$$0 \le r_0, r_1 \le b - 1 \Rightarrow |r_0 - r_1| \le b \Rightarrow r_0 = r_1, \,\,\, q_0 = q_1 \,\,\,\,\blacksquare$$ 


::::

## НОД


:::: {#definition-6}

**Определение:** (*НОД*)  Пусть $a, b \in \mathbb{Z},\,\,\,\,\mathcal{D}_{a, b}= \{z \in \mathbb{N}: z\,\,|\,\,a, z\,\,|\,\,b\}$. Тогда $$\mathbf{НОД}(a, b) = \max \mathcal{D}$$

::::

:::: {#statement-1}

**Утверждение:**  (корректность определения)
*Доказательство:* очев.

::::

:::: {#lemma-1}

**Лемма:**  $$(a, b) = (a, a \pm b)$$

*Доказательство:*
$$\begin{cases}
z\,\,|\,\,a \\ z\,\,|\,\,b
\end{cases} \Rightarrow z\,\,|\,\,b \pm a \Rightarrow \mathcal{D}_{a, b} \subset \mathcal{D}_{a, b \pm a}$$
$$\begin{cases}
z\,\,|\,\,a \\ z\,\,|\,\,b + a
\end{cases} \Rightarrow z\,\,|\,\,b \Rightarrow \mathcal{D}_{a, b+a} \subset \mathcal{D}_{a, b}\,\,\,\,\blacksquare$$

::::

## Алгоритм Евклида


$$a \in \mathbb{Z}, b \in \mathbb{N}$$
$$a = bq_0 + r_1, \,\,\,\, 0 \le r_1 < b$$
$$b = r_1q_1 + r_2, \,\,\,\, 0 \le r_2 < r_1$$
$$r_0 = r_2q_2 + r_3, \,\,\,\, 0 \le r_3 \le r_2$$
$$\vdots$$
$$r_{j - 1} = r_{j}q_{j} + r_{j + 1}, \,\,\,\, 0 \le r_{j + 1} \le r_j$$
$$\vdots$$
$$r_{n - 2} = r_{n - 1}q_{n - 1} + r_{n}, \,\,\,\, 0 \le r_{n} \le r_{n - 1}$$
$$r_{n - 1} = r_{n}q_{n} + r_{n + 1}, \,\,\,\, r_{n + 1} = 0$$
$$\exists n \in \mathbb{N}: r_{n + 1} = 0$$

:::: {#statement-2}

**Утверждение:**  $\mathbf{НОД} (a, b) = r_n$

*Доказательство:* $\forall j \le n (r_{j - 1}, r_j) = (r_j, r_{j + 1}) \,\,\,\,\blacksquare$

::::


:::: {#theorem-2}

**Теорема:**  (*о линейном представлении НОД*)
Пусть $a, b \in \mathbb{Z}, \,\,\,\,\,\, d = (a, b)$. Тогда $$\exists x, y \in \mathbb{Z}: d = ax + by$$

*Доказательство:* Обратный ход алгоритма Евклида $\,\,\,\,\blacksquare$.

::::

:::: {#lemma-2}

**Лемма:**  (*важная*)
$$\begin{cases}
a\,\,|\,\,bc \\ (a, b) = 1
\end{cases} \Rightarrow a\,\,|\,\,c$$
*Доказательство:* $$(a, b) = 1 \Rightarrow \exists x, y \in \mathbb{Z}: 1 = ax + by$$
$$acx + bcy = c$$
$$\begin{cases}
a\,\,|\,\,acx \\ a\,\,|\,\,bcy
\end{cases} \Rightarrow a\,\,|\,\,c \,\,\,\,\blacksquare$$

::::

## НОК и НОД нескольких чисел


:::: {#definition-7}

**Определение:**  $z \in \mathbb{Z}$ - общее кратное чисел $a_1, \ldots, a_n$, если $a_j \,\,|\,\,z \forall j$

::::

:::: {#definition-8}

**Определение:**  $\mathbf{НОК} (a_1, \ldots, a_n) = \min \{z \in \mathbb{N} : z$ общее кратное чисел $a_1, \ldots, a_n \}$

::::

:::: {#theorem-3}

**Теорема:**  Если $z_0 - \mathbf{НОК} (a_1, \ldots, a_n)$, то $z_0 \,\,|\,\,z$

*Доказательство:* 

::::

:::: {#definition-9}

**Определение:**  $\mathbf{НОД} (a_1, \ldots, a_n) = \max \{z \in \mathbb{N}: z \,\,|\,\,a_j \,\,\,\,\,\, \forall j = 1, \ldots, n\}$

::::

:::: {#theorem-4}

**Теорема:**  Пусть $d$ - общий делитель $a_1, \ldots, a_n$. Тогда $d \,\,|\,\,\mathbf{НОД} (a_1, \ldots, a_n)$

*Доказательство:*

::::

# Конечные цепные дроби


$$\frac{a}{b} \in \mathbb{Q}, \,\,\,\, (a, b) = 1$$
$$\frac{a}{b} = A_0 + \frac{1}{A_1 + \frac{1}{A_2 + \frac{1}{\ddots \frac{1}{A_n}}}}$$

:::: {#definition-10}

**Определение:**  $[A_0, \ldots, A_n]$ - разложение числа $\frac{a}{b}$ в конечную цепную дробь.

::::

:::: {#definition-11}

**Определение:**  $[A_0, \ldots, A_k], \,\,\,\, k \le n$ - подходящая дробь для разложения $\frac{a}{b}$ в конечную цепную дробь.

::::

:::: {#lemma-3}

**Лемма:**  (*основная лемма о подходящих дробях*)

1. $$\begin{cases}
p_{k + 1} = A_{k + 1}p_k + p_{k - 1} \\ q_{k + 1} = A_{k + 1}q_k + q_{k - 1}
\end{cases}$$
2. $$p_kq_{k-1} - q_kp_{k - 1} = (-1)^{k + 1}$$

*Доказательство:*

::::

:::: {#theorem-5}

**Теорема:**  (*Перрона*)
$$\left| \alpha - \frac{p_k}{q_k} \right| = \frac{1}{q_k^2(\alpha_{k + 1} + \alpha_{k})} \,\,\,\, \alpha_k = [A_k;A_{k - 1};\ldots ;A_1]$$

*Доказательство:*

::::

# Теория сравнений


:::: {#definition-12}

**Определение:**
$$a, b \in \mathbb{Z} \,\,\,\, m \in \mathbb{N}, \,\,\,\, m \ge 2$$
$$a \equiv b \mod m \,\,\,\, m \,\,|\,\,(a - b)$$

::::

## Простейшие свойства сравнений

1. $\,\,\,\,a \equiv a \mod m$<br>
$\,\,\,\,a \equiv b \mod m \Rightarrow b \equiv a \mod m$<br>
$\begin{cases}
a \equiv b \mod m \\ b \equiv c \mod m
\end{cases} \Rightarrow a \equiv c \mod m$<br><br>
2. $\begin{cases}
a \equiv b \mod m \\ c \equiv d \mod m
\end{cases} \Rightarrow a \pm b \equiv c \pm d \mod m$<br><br>
3. $\begin{cases}
a \equiv b \mod m \\ c \equiv d \mod m
\end{cases} \Rightarrow ac \equiv bd \mod m$<br><br>
4. $\begin{cases}
a \equiv b \mod m \\ d\,\,|\,\,a \\ d\,\,|\,\,b \\ d\,\,|\,\,m 
\end{cases} \Rightarrow \frac{a}{d} \equiv \frac{b}{d} \mod \frac{m}{d}$<br><br>
4\*. $ad \equiv bd \mod md \Rightarrow a \equiv b \mod m$<br><br>
5. $\begin{cases}
ad \equiv bd \mod m \\ (d, m) = 1
\end{cases} \Rightarrow a \equiv b \mod m$<br><br>
6. Пусть $(a, m) = 1$. Тогда $\exists x \in \mathbb{Z}:$
    a. $ax \equiv 1 \mod m$
    b. $\begin{cases}
ax_1 \equiv 1 \mod m \\ ax_2 \equiv 1 \mod m
\end{cases} \Rightarrow x_1 \equiv x_2 \mod m$<br><br>
7. Если $(a, m) = 1$, то $\forall b \,\,\,\, \exists ! \,\, x: ax \equiv b \mod m$

## Функция Эйлера


:::: {#definition-13}

**Определение:**  

$\varphi (m)=$ количество элементов в множестве $\{x \in \mathbb{N}, x \le m, (x, m) = 1\}$

::::

## Теорема Эйлера

:::: {#theorem-6}

**Теорема:**  Пусть $(a, m) = 1$. Тогда 
$$a^{\varphi(m)} \equiv 1 \mod m$$

*Доказательство:*

::::

:::: {#corollary-5}

**Следствие:**  Если $p$ - простое, то: $$a^{p - 1} \equiv 1 \mod p$$

*Доказательство:*

::::

## Классы вычетов


$m \ge 2, \,\,\,\, m \in \mathbb{N}$

:::: {#definition-15}

**Определение:**  *Класс вычетов* $a$ *по модулю* $m$<br>

$\overline{a} = \{x \in \mathbb{Z}: x \equiv a \mod m\}$<br>
$\overline{a} + \overline{b} = \overline{a_0 + b_0} \,\,\,\, a_0 \in \overline{a}, \,\, b_0 \in \overline{b}$<br>
$\overline{a} \cdot \overline{b} = \overline{a_0 \cdot b_0} \,\,\,\, a_0 \in \overline{a}, \,\, b_0 \in \overline{b}$

*Доказательство: корректности*

::::

:::: {#definition-16}

**Определение:**  класс $\overline{a}$ вычетов по модулю $m$ называется *обратимым*, если:

1. $\exists \,\, a_1 \in \overline{a}: (a_1, m) = 1$
2. $\forall \,\, a_1 \in \overline{a}: (a_1, m) = 1$
3. $\exists \,\, b \in \mathbb{Z}: \overline{a} \cdot \overline{b} = \overline{1}$

*Доказательство:* (эквивалентности 1. 2. 3.)

::::

:::: {#definition-17}

**Определение:**  $B \subset \mathbb{Z}$ - *полная* система вычетов по модулю $m$, если $B$ содержит ровно по одному числу из каждого класса вычетов по модулю $m$.

::::

:::: {#definition-18}

**Определение:**  $B^* \subset \mathbb{Z}$ - *приведенная* система вычетов по модулю $m$, если $B^*$ содержит ровно по одному числу из каждого обратимого класса вычетов по модулю $m$.

::::
 
*Замечание:* $\forall B \,\,\,\, |B| = m$<br>
$\forall B^* \,\,\,\, |B^* | = \varphi(m)$<br>

:::: {#statement-3}

**Утверждение:**  Пусть $B$ обладает свойствами:

1. Все элементы $B$ различны по модулю $m$.
2. $\forall x \in \mathbb{Z} \,\,\,\, \exists b \in B: x \equiv b \mod m$

Тогда $B$ - полная система вычетов по модулю $m$.

*Доказательство:*

::::

:::: {#statement-4}

**Утверждение:**  Пусть $B^*$ обладает свойствами:

1. Все элементы $B^*$ различны по модулю $m$.
2. $\forall b \in B^*  \,\,\,\,(b, m) = 1$
3. $\forall x \in \mathbb{Z}:(x, m) = 1 \,\,\,\, \exists b \in B^*: x \equiv b \mod m$

Тогда $B^*$ - приведенная система вычетов по модулю $m$.

*Доказательство:*

::::

:::: {#theorem-8}

**Теорема:**  Пусть $(m, n) = 1$<br>
$B_1$ - полная система вычетов по модулю $m$.<br>
$B_2$ - полная система вычетов по модулю $n$.<br>
$B = \{xn + ym, \,\,\,\, x \in B_1, \,\,\,\, y \in B_2\}$.<br> Тогда $B$ - полная система вычетов по модулю $mn$

*Доказательство:*

::::

:::: {#theorem-9}

**Теорема:**  Пусть $(m, n) = 1$<br>
$B_1^*$ - полная система вычетов по модулю $m$.<br>
$B_2^*$ - полная система вычетов по модулю $n$.<br>
$B^* = \{xn + ym, \,\,\,\, x \in B_1^*, \,\,\,\, y \in B_2^*\}$.<br> Тогда $B^*$ - полная система вычетов по модулю $mn$

*Доказательство:*

::::

:::: {#corollary-1}

**Следствие:**  (*мультипликативность функции Эйлера*)
$$\begin{cases}
|B_1^*| = \varphi(m) \\ |B_2^*| = \varphi(n)
\end{cases} \Rightarrow |B^*| = \varphi(mn)$$

*Доказательство:*

::::

:::: {#corollary-2}

**Следствие:** 
Если $m = p_1^{\alpha_1} \cdot \ldots \cdot p_t^{\alpha_t}, p_i$ - простое $\forall i$<br>
$$\varphi(m) = m(1 - \frac{1}{p_1})\cdot \ldots \cdot (1 - \frac{1}{p_t})$$

*Доказательство:* $\varphi(p) = p - 1$, если $p$ - простое.

$\varphi(p^{\alpha}) = p^{\alpha} - p^{\alpha - 1} = p^{\alpha}(1 - \frac{1}{p})$

Далее используем [следствие 1](#corollary-1).

::::

## Простые числа


:::: {#definition-19}

**Определение:**  $n \in \mathbb{N}$ - *простое*, если имеет ровно 2 делителя $1$ и $n$.

::::

:::: {#definition-20}

**Определение:**  $n \in \mathbb{N} \,\,\,\, n > 1$ - *составное*, если оно не простое.

::::

> $1$ не составное и не простое.

:::: {#theorem-9}

**Теорема:**  Пусть $a > 1 \,\,\,\,  a \in \mathbb{Z}$. Тогда наименьший делитель $c$ числа $a$ неравный $1$ - простое число.

*Доказательство:* 

::::

:::: {#theorem-10}

**Теорема:**  Множество простых чисел бесконечно.

*Доказательство:* (от противного)

::::

:::: {#theorem-11}

**Теорема:**  Пусть $a, b \in \mathbb{Z}$, $p$ - простое, $p \,\,|\,\, ab$. Тогда $p \,\,|\,\, a$ или $p \,\,|\,\, b$.

*Доказательство:*

::::

:::: {#theorem-12}

**Теорема:**  (*основная теорема арифметики*) Всякое $n \in \mathbb{N} \,\,\,\, n > 1$ раскладывается в произведение простых сомножителей единственным образом.

*Доказательство:*

::::

#### Каноническая запись разложения числа на простые сомножители

$n = p_1^{\alpha_1} \cdot \ldots \cdot p_k^{\alpha_k}$, где $\forall i \ne j \,\,\,\, 1 \le i, j \le k \,\,\,\, p_i \ne p_j \,\,\,\, \alpha_i \in \mathbb{N} \,\,\,\, \alpha_i \ge 1$.

:::: {#theorem-13}

**Теорема:** Наименьший простой делитель $p$ составного числа $n$ не больше $\sqrt{n}$.

*Доказательство:*

::::


#### Решето Эратосфена

:::: {#lemma-4}

**Лемма:** $$\ln(N + 1) \le \displaystyle \sum_{n = 1}^{N}\frac{1}{n}$$

*Доказательство:* $\ln(1 + t) \le t$ по теореме Лагранжа.<br>
Рассмотрим $t = \frac{1}{n} \Rightarrow$
$\ln(n + 1) - \ln(n) = \ln(\frac{n + 1}{n}) = \ln(1 + \frac{1}{n}) \le \frac{1}{n}$<br>
Суммируя по натуральным числам от $1$ до $n$, получаем:<br>
$$\displaystyle \sum_{n = 1}^{N}\ln(n + 1) - \ln(n) \le \displaystyle \sum_{n = 1}^{N}\frac{1}{n} \Rightarrow$$
$$\ln(N + 1) \le \displaystyle \sum_{n = 1}^{N}\frac{1}{n} \,\,\,\,\blacksquare$$

::::

:::: {#theorem-14}

**Теорема:**  При любом $x \ge 2$ справедливо неравенство:
$$\displaystyle \sum_{p \le x}^{}\frac{1}{p} \ge \ln(\ln(x)) - 1$$

*Доказательство:* Пусть $k$ удовлетворяет условию: $2^k \le x \le 2^{k + 1}$. Тогда

$\forall n \le x, \,\,\,\,\,\,\,\, n = p_1^{\alpha_1} \cdot \ldots \cdot p_r^{\alpha_r}, \,\,\,\, p_i \le x, \,\,\,\, \alpha_i \le k$.
Рассмотрим $\displaystyle \prod_{p \le x}\left(1 - \frac{1}{p}\right)^{-1} = \displaystyle \prod_{p \le x}\frac{1}{\left(1 - \frac{1}{p}\right)} = \displaystyle \prod_{p \le x}\left(1 + \frac{1}{p} + \frac{1}{p^2} + \ldots\right)=$<br> $= \displaystyle \prod_{p \le x}\left(1 + \frac{1}{p} + \frac{1}{p^2} + \ldots + \frac{1}{p^k}\right) = 1 + \displaystyle \sum_{n}’ \frac{1}{n} \ge 1 + \displaystyle \sum_{n \le x} \frac{1}{n} \ge \displaystyle \sum_{n \le x} \frac{1}{n} \ge \ln(x)$

$\ln\left(1 - \frac{1}{p}\right)^{-1} = \ln\left(1 + \frac{1}{p - 1}\right) \le \frac{1}{p - 1}$<br>
Суммируя, получаем: $\ln \displaystyle \prod_{p \le x}\left(1 - \frac{1}{p}\right)^{-1} \le \displaystyle \sum_{p \le x}\frac{1}{p - 1} = \displaystyle \sum_{p \le x}\frac{1}{p} + \sum_{p \le x}\frac{1}{p - 1} - \frac{1}{p} \le \displaystyle \sum_{p \le x}\frac{1}{p} + 1 \,\,\,\,\blacksquare$

::::


:::: {#definition-21}

**Определение:** (количество простых меньших $x$) $$\pi(x) = \displaystyle \sum_{p \le x}^{}1$$

::::

:::: {#definition-22}

**Определение:**  (*функция Мёбиуса*)

$$\mu(n) = \begin{cases} 1,\,\,\,\, n = 1 \\
 0,\,\,\,\, n = p^2m,\,\,\,\, p - простое \\ 
 (-1)^k,\,\,\,\, n = p_1 \cdot \ldots \cdot p_k \end{cases}$$

**Обозначение:** $\displaystyle \sum_{d \,\,|\,\, n}$ - сумма по всем делителям числа $n$, включая $n$ и $1$.

::::

:::: {#definition-23}

**Определение:**
$$\tau(n) = \displaystyle \sum_{d \,\,|\,\, n}1$$

::::

:::: {#definition-24}

**Определение:**
$$\sigma(n) = \displaystyle \sum_{d \,\,|\,\, n}d$$

::::

:::: {#theorem-10}

**Теорема:**  (*основное свойство функции Мёбиуса*)
$$\displaystyle \sum_{d \,\,|\,\, n}\mu(n) = \begin{cases} 1,\,\,\,\, n = 1 \\
0,\,\,\,\, n \ne 1 \end{cases}$$

*Доказательство:* 

::::

:::: {#corollary-3}

**Следствие:**  Пусть $a, b \in \mathbb{N}$
$$\displaystyle \sum_{d \,\,|\,\, (a, b)}\mu(n) = \begin{cases} 1,\,\,\,\, (a, b) = 1 \\
0,\,\,\,\, (a, b) \ne 1 \end{cases}$$

*Доказательство:*

::::

:::: {#theorem-11}

**Теорема:**  Если $x$ достаточно велико, то
$$\pi(x) \le \frac{2x}{\ln\ln(x)}$$

*Доказательство:* 

::::

## Китайская теорема об остатках


Рассмотрим сравнения:
$$\begin{cases} x \equiv a_1 \mod m_1 \\
\vdots \\
x \equiv a_k \mod m_k \end{cases}$$
$$(m_i, m_j) = 1 \,\,\,\,\,\,\,\, \forall i \ne j$$
$$m_i \in \mathbb{N} \,\,\,\,\,\,\,\, a_i \in \mathbb{Z}$$

:::: {#theorem-12}

**Теорема:**  $$x_0 = M_1x_1 + \ldots + M_kx_k$$
$M = m_1 \cdot \ldots \cdot m_k,\,\,\,\, M_i = \frac{M}{m_i},\,\,\,\,$
$x_i$ - решение сравнения $M_ix_i \equiv a_i \mod m_i$ - является решением системы сравнений, приведенной выше. 

*Доказательство:*

::::

:::: {#corollary-4}

**Следствие:**  Если $f(x) = a_nx^n + a_{n - 1}x^{n - 1} + \ldots + a_0$ - полином с целыми коэффицентами, $J(f, m)$ - число решений сравнения $f(x) \equiv 0 \mod m$, то функция $J(f, m)$ мультипликативна при фиксированном $f$.

*Доказательство:* 

::::


## Сравнения с одним неизвестным


Рассмотрим сравнение $ax \equiv b \mod m$, где $(a, m) = 1$.

:::: {#theorem-15}

**Теорема:**  $(-1)^{n}bp_{n - 1}$ - является решением сравнения, приведенного выше.

*Доказательство:* $p_nq_{n - 1} - p_{n - 1}q_n = (-1)^{n}, \,\,\,\,\,\,\,\, \frac{p_n}{q_n} = \frac{m}{a} \Rightarrow mq_{n - 1} - p_{n - 1}a = (-1)^{n} \Rightarrow$

$(-1)^{n}bmq_{n - 1} - (-1)^{n}bp_{n - 1}a = b \Rightarrow (-1)^{n - 1}bp_{n - 1}a \equiv b \mod m \,\,\,\,\blacksquare$

::::

:::: {#theorem-16}

**Теорема:**  $a^{\varphi(m) - 1}b$ - является решением сравнения, приведенного выше.

*Доказательство:* $(a, m) = 1 \Rightarrow$ по [теореме Эйлера](#theorem-6) $a^{\varphi(m)} \equiv 1 \mod m \Rightarrow$<br>

$ax \equiv a^{\varphi(m)}b \mod m \Rightarrow x \equiv a^{\varphi(m) - 1}b \mod m \,\,\,\,\blacksquare$

::::

### Случай не взаимно простых $a$ и $m$

Пусть $(a, m) = d \Rightarrow a = a_1d, \,\,\,\,\,\,\,\, m = m_1d \Rightarrow a_1dx \equiv b \mod m_1d \Rightarrow$:

1. $d \nmid b$ - нет решений.
2. $d \,\,|\,\, b \Rightarrow b = b_1d \Rightarrow a_1x \equiv b_1 \mod m_1$<br>
Пусть $x_0$ - решение этого сравнения. Тогда классы вычетов $x_0, x_0 + m_1, \ldots, x_0(d - 1)m_1$ по модулю $m$ являются решениями сравнения $ax \equiv b \mod m$. То есть сравнение $ax \equiv b \mod m$ имеет $d = (a, m)$ - решений.

## Полиномиальные сравнения


Рассмотрим полином: $$f(x) = a_nx^n + a_{n - 1}x^{n - 1} + \ldots + a_0 \,\,\,\,(17)$$ <a name="equation-17"></a>

:::: {#theorem-17}

**Теорема:**  Полиномиальное сравнение степени $n$ по простому модулю $p$ равносильно некоторому сравнению степени не выше $p - 1$.

*Доказательство:* Поделим $f(x)$ на $x^p - x$ с отстатком:

$$f(x) = (x^p - x)g(x) + r(x)$$
Степень $deg(r(x)) < p$, по [малой теореме Ферма](#corollary-5) $x^p - x \equiv 1 \mod p \,\,\,\,\blacksquare$

::::

:::: {#theorem-18}

**Теорема:**  Если $f(x) \equiv 0 \mod p$($p$ - простое) имеет более чем $n$ решений, то все коэффиценты $f(x)$ делятся на $p$.

*Доказательство:*

::::

:::: {#theorem-19}

**Теорема:**  (*Вильсона*) $p$ - простое $\Rightarrow$
$$(p - 1)! + 1 \equiv 0 \mod p$$

*Доказательство:* Рассмотрим $f(x) = (x - 1)(x - 2) \cdot \ldots \cdot (x - (p - 1)) - (x^{p - 1} - 1)$.

Его степень не выше $p - 2$, но вычеты $1, \ldots, p - 1$ являются решениями сравнения $\Rightarrow$ по [теореме](#theorem-18) все коэффиценты $f(x)$ делятся на $p$. Свободный член $(-1)^{p - 1}(p - 1)! + 1 \,\,\,\,\blacksquare$

::::

### Метод "подъёма" решения


:::: {#theorem-20}

**Теорема:**  (*Лемма Гензеля*) Пусть $p$ - простое, $f(x) \in \mathbb{Z}[x]$, $f(x_1) \equiv 0 \mod p \,\,\,\,$, $f’(x_1) \not\equiv 0 \mod p$. Тогда в полной системе вычетов по модулю $p^k, \,\,\,\, k \in \mathbb{N}$ существует только один элемент $x_k$, удовлетворяющий условиям: $x_k \equiv x_1 \mod p, \,\,\,\,\,\,\,\, f(x_k) \equiv 0 \mod p^k$.

*Доказательство:* (индукция по степени $k$) Для $k = 1$ верно по [определению полной системы вычетов](#definition-17). Докажем для $k$, пользуясь тем, что для $k - 1$ верно. $f(x_k) \equiv 0 \mod p^k \Rightarrow f(x_k) \equiv 0 \mod p^{k - 1}$. Т.к. по модулю $p^{k - 1}$ существует единственное решение, $x_k \equiv x_{k - 1} \mod p^{k - 1} \Rightarrow x_k = x_{k - 1} + t \cdot p^{k - 1}$.
$$f(x_{k - 1} + t \cdot p^{k - 1}) = f(x_{k - 1}) + f’(x_{k - 1})t \cdot p^{k - 1} + \ldots \equiv f(x_{k - 1}) + f’(x_{k - 1})t \cdot p^{k - 1} \mod p^{k} \Rightarrow$$
$$f(x_{k - 1}) + f’(x_{k - 1})t \cdot p^{k - 1} \equiv 0 \mod p^{k}$$
$f(x_{k - 1}) \equiv 0 \mod p^{k - 1}$, поэтому можем поделить на $p^{k - 1}$:
$$\frac{f(x_{k - 1})}{p^{k - 1}} + f’(x_{k - 1})t \equiv 0 \mod p$$ это сравнение имеет единственное решение, т.к. $f’(x_{k - 1}) \equiv f’(x_1) \not\equiv 0 \mod p \,\,\,\,\blacksquare$

::::

## Сравнения второй степени


Рассмотрим сравнение $x^n \equiv a \mod m, \,\,\,\, (a, m) = 1$

:::: {#definition-25}

**Определение:**  Если сравнение, написанное выше, имеет решение, то $a$ - вычет $n$-й степени.

::::

> $n = 2$ квадратичный вычет
> $n = 3$ кубический вычет

:::: {#theorem-21}

**Теорема:**  Если $a, \,\,\,\, a \ne 0$ - квадратичный вычет, то сравнение $x^2 \equiv a \mod p, \,\,\,\, p \ge 3, \,\,\,\, p$ - простое имеет ровно $2$ решения.

*Доказательство:*

::::

:::: {#theorem-22}

**Теорема:**  Пусть $p \ge 3, \,\,\,\, p$ - простое. Тогда по модулю $p$ существует ровно $\frac{p - 1}{2}$ - квадратичных вычетов и столько же квадратичных невычетов. При этом квадратичные вычеты сравнимы по модулю $p$ с числами: $1^2, 2^2, \ldots, \left(\frac{p - 1}{2}\right)$

*Доказательство:*

::::

### Символ Лежандра

:::: {#definition-26}

**Определение:**  (*Символ Лежандра*) $a \in \mathbb{Z}, \,\,\,\, p \ge 3, \,\,\,\,p$ - простое.

$$\left(\frac{a}{p}\right) = \begin{cases} -1, \,\,\,\, (a, p) = 1, \,\,\,\, a - квадратичный \,\,\,\, невычет \,\,\,\, по \,\,\,\, модулю \,\,\,\, p \\
\,\,\,\,\,0, \,\,\,\, p \,\,|\,\, a \\
\,\,\,\,\,1, \,\,\,\, (a, p) = 1, \,\,\,\, a - квадратичный \,\,\,\, вычет \,\,\,\,по \,\,\,\, модулю \,\,\,\, p \end{cases}$$

::::

:::: {#theorem-23}

**Теорема:**  (*Свойства символа Лежандра*)

1. (*Критерий Эйлера*) $a^{\frac{p - 1}{2}} \equiv \left(\frac{a}{p}\right) \mod p$
2. Если $a \equiv b \mod p$, то $\left(\frac{a}{p}\right) = \left(\frac{b}{p}\right)$
2. $\left(\frac{1}{p}\right) = 1$
3. $\left(\frac{-1}{p}\right) = (-1)^{\frac{p - 1}{2}}$
4. $\left(\frac{ab}{p}\right) = \left(\frac{a}{p}\right) \cdot \left(\frac{b}{p}\right)$
5. $\left(\frac{a^2}{p}\right) = 1$
6. $\displaystyle \sum_{a = 1}^{p}\left(\frac{a}{p}\right) = 0$

### Квадратичный закон взаимности

:::: {#lemma-5}

**Лемма:** (*Лемма Гаусса*) Пусть $p \ne 2, \,\,\,\, p$ - простое, $p \nmid a$. Тогда $$\left(\frac{a}{p}\right) = \varepsilon_1 \cdot \ldots \cdot \varepsilon_k$$
$ka \equiv \varepsilon_kr_k \mod p, \,\,\,\, 1 \le r_k \le \frac{p - 1}{2}, \,\,\,\, \varepsilon_k = \pm 1, \,\,\,\, k = 1, \ldots, \frac{p - 1}{2}$.

*Доказательство:* Пусть $r_k \equiv r_l \mod p \Rightarrow ka \equiv \varepsilon_kr_k \mod p$ и $la \equiv \varepsilon_lr_l \mod p \Rightarrow ka \equiv \pm la \mod p \Rightarrow p \,\,|\,\, \mp(k - l)$, что невозможно, т.к. $|\mp(k - l)| \le p \Rightarrow$ все $r_k$ различны. Значит $\{r_1, \ldots, r_k\} = \{1, \ldots, \frac{p - 1}{2}\}$, перемножая все $ka \equiv \varepsilon_kr_k \mod p$, получаем $a^{\frac{p - 1}{2}} \equiv \varepsilon_1 \cdot \ldots \cdot \varepsilon_k \mod p$. Т.к. модуль раности правой и левой частей сравнения $\le 2$

$$a^{\frac{p - 1}{2}} = \varepsilon_1 \cdot \ldots \cdot \varepsilon_k \mod p \,\,\,\,\blacksquare$$

::::

:::: {#corollary-6}

**Следствие:**  

1. Пусть $a$ - нечетное, $S = \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}\left[\frac{ax}{p}\right]$. Тогда $\left(\frac{a}{p}\right) = (-1)^S$
2. $$\left(\frac{2}{p}\right) = (-1)^\frac{p^2 - 1}{8}$$

*Доказательство:* $ax - p\left[\frac{ax}{p}\right] = \begin{cases} r_x, \,\,\,\, \varepsilon_x = 1 \\ p - r_x, \,\,\,\, \varepsilon_x = -1 \end{cases}$, суммируя по $1, \ldots, \frac{p - 1}{2}$, получаем: $\left(\frac{p^2 - 1}{8}\right)a - p \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}\left[\frac{ax}{p}\right] = pt + \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}\varepsilon_xr_x, \,\,\,\, t$ - количество $-1$ среди $\varepsilon_x$.

Переходя к сравнению по модулю $2$, заметив, что $p \equiv -1 \mod 2$, $\varepsilon \equiv 1 \mod 2 \Rightarrow \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}\varepsilon_xr_x \equiv \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}r_x = \left(\frac{p^2 - 1}{8}\right)$, получаем:
$$\left(\frac{p^2 - 1}{8}\right)a + \displaystyle \sum_{x = 1}^{\frac{p - 1}{2}}\left[\frac{ax}{p}\right] \equiv t + \left(\frac{p^2 - 1}{8}\right) \mod 2 \,\,\,\,\blacksquare$$

::::

:::: {#theorem-24}

**Теорема:**  (*Квадратичный закон взаимности*)

Пусть $p \ne q, \,\,\,\, q \ne 2, \,\,\,\, p \ne 2, \,\,\,\, p, q$ - простые. Тогда:
$$\left(\frac{p}{q}\right) \cdot \left(\frac{q}{p}\right) = (-1)^{\frac{p - 1}{2} \cdot \frac{q - 1}{2}}$$

*Доказательство:* 

::::

## Суммы двух и четырех квадратов


:::: {#theorem-25}

**Теорема:**  Пусть $p = 4k + 1, \,\,\,\, p$ - простое. Тогда уравнение $x^2 + y^2 = p$ разрешимо в целых числах.

*Доказательство:*

::::

:::: {#lemma-6}

**Лемма:**  Если $u, v$ представимы в виде суммы четырех квадратов, то их произведение $u\cdot v$ представимо в виде суммы четырех квадратов.

*Доказательство:* Рассмотрим числа $\alpha = x_1 + ix_2, \,\,\,\, \beta = x_3 + ix_4, \,\,\,\, \gamma = y_1 + iy_2, \,\,\,\, \delta = y_3 + iy_4$. Пусть $$\mathbf{A} = \left(\begin{array}{cc} \alpha & \beta \\ -\bar{\beta} & \bar{\alpha} \end{array}\right) \,\,\,\,\,\,\,\, \mathbf{B} = \left(\begin{array}{cc} \gamma & \delta \\ -\bar{\delta} & \bar{\gamma} \end{array}\right)$$

$$\det \mathbf{A} = x_1^2 + x_2^2 + x_3^2 + x_4^2, \,\,\,\, \det \mathbf{B} = y_1^2 + y_2^2 + y_3^2 + y_4^2$$
$$\mathbf{AB} = \left(\begin{array}{cc} \alpha \gamma - \beta \bar{\delta} & \alpha \delta + \beta \bar{\gamma} \\ - \gamma \bar{\beta} - \bar{\alpha} \bar{\delta} & - \delta \bar{\beta} + \bar{\alpha} \bar{\gamma} \end{array}\right)$$ Эта матрица имеет ту же структуру, что и матрицы выше, поэтому, в силу $\det A \cdot \det B = \det AB$, получаем: $$(x_1^2 + x_2^2 + x_3^2 + x_4^2)(y_1^2 + y_2^2 + y_3^2 + y_4^2) = z_1^2 + z_2^2 + z_3^2 + z_4^2 \,\,\,\,\blacksquare$$

::::

:::: {#lemma-7}

**Лемма:**  Для любого простого $p \,\,\,\,\,\,\,\, \exists a, b$:$$1 + a^2 + b^2 \equiv 0 \mod p$$

*Доказательство:* Рассмотрим множества $M_1 = \{k^2, \,\,\,\, k = 0, \ldots, \frac{p - 1}{2}\}$ и $M_2 = \{-1 - k^2, \,\,\,\, k = 0, \ldots, \frac{p - 1}{2}\}$. В объединении этих множеств $p + 1$ элемент, а по модулю $p$ существует $p - 1$ различный класс вычетов, значит существуют $0 \le a \le \frac{p - 1}{2}$ и $0 \le b \le \frac{p - 1}{2}$, такие что $a^2 \equiv -1 - b^2 \mod p \,\,\,\,\blacksquare$
::::

:::: {#lemma-8}

**Лемма:**  Любое простое число $p$ представимо в виде суммы четырех квадратов.

*Доказательство:* Опять рассмотрение чего-то и принцип Дирихле.

::::

:::: {#theorem-26}

**Теорема:**  Любое натуральное число $n$ представимо в виде суммы четырех квадратов.

*Доказательство:* Следует из лемм [1](#lemma-6), [2](#lemma-7), [3](#lemma-8) $\,\,\,\,\blacksquare$

::::

**Проблема Варинга**: $m \in \mathbb{Z}, \,\,\,\, k > 0, \,\,\,\, k \in \mathbb{Z}$. Верно ли что любое $n \in \mathbb{N}$ представимо в виде: $$n = x_1^m + \ldots + x_k^m, \,\,\,\,\,\,\,\, x_i \ge 0$$

## Показатель числа


:::: {#definition-14}

**Определение:**  *Показатель числа* $a$ по модулю $m$ ($ord_ma$)

Рассмотрим $M = \{x \in \mathbb{N}: a^x \equiv 1 \mod m\}$<br>
$M \ne \varnothing$ по [теореме Эйлера](#theorem-6)<br>
По аксиоме Архимеда $\exists \,\, \min M = ord_ma$ 

::::

:::: {#theorem-7}

**Теорема:**  (*о показателе*)
Пусть $(a, m) = 1, \,\,\,\, z \in \mathbb{N}, \,\,\,\, a^z \equiv 1 \mod m$. Тогда $$ord_am\,\,|\,\,z$$

*Доказательство:*

::::

:::: {#theorem-27}

**Теорема:**  Пусть $(a, m) = 1$. Тогда
$$a^k \equiv a^n \mod m \Leftrightarrow k \equiv n \mod ord_ma$$

*Доказательство:*

::::

# Первообразные корни


:::: {#definition-27}

**Определение:**  Пусть $(a, m) = 1$. Если $ord_ma = \varphi(m)$, то $a$ - первообразный корень по модулю $m$.

::::

:::: {#theorem-28}

**Теорема:**  Пусть $(a, m) = 1, \,\,\,\, a$ - первообразный корень по модулю $m$. Тогда числа $$a^0, a^1, a^2, \ldots, a^{\varphi(m)}$$ образуют приведенную систему вычетов по модулю $m$.

*Доказательство:*

::::

## Существование первообразных корней по простому модулю


:::: {#theorem-29}

**Теорема:**  По простому модулю $p$ существуют первообразные корни.

*Доказательство:* 

::::


