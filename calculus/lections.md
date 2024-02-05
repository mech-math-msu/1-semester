---
title: Математический анализ
---

# Пределы


## Предел функции по Коши и по Гейне, их эквивалентность. Основные свойства предела функции


:::: {#definition-0}

**Определение:**  (По Коши) Предел функции $f(x)$ при $x$ стремящемся к $x_0$ равен $a$, если: $$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, f(x) \in B_{\varepsilon}(a)$$

Обозначается: $\displaystyle \lim_{x\to x_0} f(x) = a$

::::

:::: {#definition-1}

**Определение:**  (По Гейне) Предел функции $f(x)$ при $x$ стремящемся к $x_0$ равен $a$, если:

$$\forall \displaystyle \{x_n\}_{n = 1}^{\infty}: \left( \forall n \,\,\,\, x_n \ne x_0 \,\,\,\, \exists \displaystyle \lim_{n\to \infty}x_n = x_0 \right)\,\,\,\,\,\,\,\, \exists \displaystyle \lim_{n\to \infty}f(x_n) = a$$

::::

:::: {#theorem-0}

**Теорема:**  Определение предела по Коши $\Leftrightarrow$ определнию предела по Гейне.

*Доказательство:*

::::

:::: {#theorem-7}

**Теорема:**  Если $\exists \displaystyle \lim_{x\to x_0}f(x) = a$, то он единственный.

*Доказательство:* Гейне.

::::

:::: {#theorem-8}

**Теорема:**  Если $\exists \displaystyle \lim_{x\to x_0}f(x) = a$, то $\exists c, \,\,\,\, \exists \delta > 0: \,\,\,\,\forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, |f(x)| < c$

*Доказательство:* $\exists \delta > 0: \,\,\,\, \forall x: 0 < |x - x_0| < \delta \,\,\,\, |f(x) - a| < 1 \Rightarrow a - 1 < f(x) < a + 1 \,\,\,\,\blacksquare$

::::

:::: {#theorem-9}

**Теорема:**  (Отделимость) Пусть $\exists \displaystyle \lim_{x\to x_0}f(x) = a$ и $b \ne a$. Тогда $\exists \varepsilon > 0, \,\,\,\, \exists \delta > 0: \,\,\,\, f(\mathring{B}_{\delta}(x_0)) \cap B_{\varepsilon}(b) = \varnothing$

*Доказательство:* $\exists \delta > 0: \,\,\,\, \forall x: 0 < |x - x_0| < \delta \,\,\,\, |f(x) - a| < \frac{|b - a|}{3}$. Возьмем $\varepsilon = \frac{|b - a|}{3} \,\,\,\,\blacksquare$

::::

:::: {#definition-6}

**Определение:**  Пусть $A \subset \mathbb{R}$ и $x_0 \in A’$ (множество предельных точек $A$). Если $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0) \cap A \,\,\,\, |f(x) - a| < \varepsilon$, то $a$ является пределом $f(x)$ в точке $x_0$ по множеству $A$.

Обозначается: $\displaystyle \lim_{x\to x_0, x \in A}f(x) = a$

**Замечание:** $\displaystyle \lim_{x\to x_0, x \in (x_0, +\infty)}f(x)$ обозначается $\displaystyle \lim_{x\to x_0+0}f(x)$

::::

:::: {#theorem-10}

**Теорема:**  Пусть $\displaystyle \lim_{x\to x_0, x \in A}f(x) = a$ и $A_1 \subset A, \,\,\,\, x_0 \in A_1$. Тогда $\exists \displaystyle \lim_{x\to x_0, x \in A_1}f(x) = a$

*Доказательство:* Гейне.

::::

## О-символика для функций, бесконечно малые и бесконечно большие функции. Исчисление бесконечно малых, арифметические свойства предела. Предельный переход в неравенствах. Критерий Коши существования предела функции


:::: {#definition-4}

**Определение:**  $f(x) = \underline{\underline{O}}(g(x))$на $\mathring{B}_{\delta}(x_0)$, при $x \to x_0$, если

$$\exists C>0: \,\,\,\,|f(x)| \le C \cdot |g(x)| \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0)$$

::::

:::: {#definition-5}

**Определение:**  $f(x) = \overline{\overline{o}}(g(x))$, при $x \to x_0$, если

$$f(x) = \alpha(x) \cdot g(x), \,\,\,\, \displaystyle \lim_{x\to x_0}\alpha(x) = 0$$

::::

:::: {#definition-2}

**Определение:**  $f(x)$ -- бесконечно большая функция при $x \to x_0 \,\,\,\, (x \to \infty)$, если:

$$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, (x > \delta) \,\,\,\,\,\,\,\, |f(x)| > \varepsilon$$
Обозначается: $\displaystyle \lim_{x\to x_0}f(x) = \infty$

::::

:::: {#definition-3}

**Определение:**  $f(x)$ - бесконечно малая (функция) при $x \to x_0 \,\,\,\, (x \to \infty)$, если $\displaystyle \lim_{x\to x_0}f(x) = 0 \,\,\,\, (\displaystyle \lim_{x\to \infty}f(x) = 0)$

Обозначается: $\overline{\overline{o}}(1)$, при $x \to x_0$

::::

:::: {#theorem-1}

**Теорема:**  Пусть $f(x)$ бесконечно большая при $x \to x_0$. Тогда $\frac{1}{f(x)}$ бесконечно малая при $x \to x_0$.

*Доказательство:* $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, (x > \delta) \,\,\,\,\,\,\,\, |f(x)| > \varepsilon \Rightarrow \frac{1}{f(x)} < \frac{1}{\varepsilon} \,\,\,\,\blacksquare$

::::

:::: {#theorem-2}

**Теорема:**  $\displaystyle \lim_{x\to x_0}f(x) = a \Leftrightarrow f(x) - a =  \bar{\bar{o}}(1)$, при $x \to x_0$

*Доказательство:* $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, |f(x)| \in B_{\varepsilon}(a) \Rightarrow$

$\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, |(f(x) - a) - 0| < \varepsilon \,\,\,\,\blacksquare$

::::

:::: {#theorem-3}

**Теорема:**  Пусть $f(x) = \overline{\overline{o}}(1), \,\,\,\, g(x) = \overline{\overline{o}}(1), \,\,\,\, h(x) = \underline{\underline{O}}(1)$, при $x \to x_0$. Тогда:

1. $$f(x) \cdot g(x) = \overline{\overline{o}}(1)$$
2. $$\alpha f(x) + \beta g(x) = \overline{\overline{o}}(1)$$
3. $$f(x) \cdot h(x) = \overline{\overline{o}}(1)$$

*Доказательство:* 

1. $f(x) = \overline{\overline{o}} \Rightarrow \forall \displaystyle \{x_n\}_{n = 1}^{\infty}: \left( \forall n \,\,\,\, x_n \ne x_0 \,\,\,\, \exists \displaystyle \lim_{n\to \infty}x_n = x_0 \right)\,\,\,\,\,\,\,\, \exists \displaystyle \lim_{n\to \infty}f(x_n) = 0$
$g(x) = \overline{\overline{o}} \Rightarrow \forall \displaystyle \{x_n’\}_{n = 1}^{\infty}: \left( \forall n \,\,\,\, x_n’ \ne x_0 \,\,\,\, \exists \displaystyle \lim_{n\to \infty}x_n’ = x_0 \right)\,\,\,\,\,\,\,\, \exists \displaystyle \lim_{n\to \infty}g(x_n’) = 0$
Условия на последовательности $x_n$ и $x_n’$ совпадают $\Rightarrow$ множество последовательностей, удовлетворяющих этим условиям совпадают. А значит $\forall \displaystyle \{x_n\}_{n = 1}^{\infty}: \left( \forall n \,\,\,\, x_n \ne x_0 \,\,\,\, \exists \displaystyle \lim_{n\to \infty}x_n = x_0 \right)\,\,\,\,\,\,\,\, \exists \displaystyle \lim_{n\to \infty}f(x_n) \cdot g(x_n) = 0 \,\,\,\,\blacksquare$
2.
3. $f(x) = \overline{\overline{o}}(1) \Rightarrow \displaystyle \lim_{x\to x_0}f(x) = 0 \Rightarrow \forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x: \,\,\,\, 0 < |x - x_0| < \delta \,\,\,\, |f(x)| < \varepsilon$
$h(x) = \underline{\underline{O}}(1) \Rightarrow \exists C > 0: \,\,\,\,|h(x)| < C$

::::

:::: {#theorem-4}

**Теорема:**  Пусть $\displaystyle \lim_{x\to x_0}f(x) = a \ne 0$. Тогда $\exists \mathring{B}_{\delta}(x_0): \,\,\,\, \frac{1}{f(x)} = \underline{\underline{O}}(1)$

*Доказательство:* Перепишу доказательство из конспекта. Ничего не понятно :(
а ладно, может и понятно. не понятно все-таки.

$\exists \mathring{B}_{\delta}(x_0)$, в которой $f(x)$ ограничена по [теореме](#theorem-8) $\Rightarrow \exists \sup_\limits{x \in \mathring{B}_{\delta}(x_0)} f(x)$ и $\exists \inf_\limits{x \in \mathring{B}_{\delta}(x_0)} f(x) \Rightarrow \frac{1}{|f(x)|} \le \max\{\frac{1}{|\sup f|};\frac{1}{|\inf f|}\} \,\,\,\,\blacksquare$ 

::::

:::: {#theorem-5}

**Теорема:**  Пусть $\displaystyle \lim_{x\to x_0}f(x) = a$ и $\displaystyle \lim_{x\to x_0}g(x) = b$. Тогда

1. $\exists \displaystyle \lim_{x\to x_0}\alpha f(x) + \beta g(x) = \alpha a + \beta b$
2. $\exists \displaystyle \lim_{x\to x_0}f(x)\cdot g(x) = a \cdot b$
3. Если $b \ne 0$, то $\exists \displaystyle \lim_{x\to x_0}\frac{f(x)}{g(x)} = \frac{a}{b}$

*Доказательство:* следует из доказанного выше.

::::

:::: {#theorem-6}

**Теорема:**  $$\exists \displaystyle \lim_{x\to x_0}f(x) = a \Leftrightarrow \exists \displaystyle \lim_{x\to x_0+0}f(x) = a \,\,\,\, и \,\,\,\,\exists \displaystyle \lim_{x\to x_0-0}f(x) = a$$

*Доказательство:* записать определение.

::::

:::: {#theorem-11}

**Теорема:**  (Критерий Коши существования предела) 
$$\exists \displaystyle \lim_{x\to x_0}f(x) = a \Leftrightarrow \forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \,\,\,\, \forall x_1, x_2 \in \mathring{B}_{\delta}(x_0) \,\,\,\, |f(x_1) - f(x_2)| < \varepsilon$$

*Доказательство:* $\Rightarrow \,\,\,\, |f(x_1) - f(x_2)| = |f(x_1) - a - (f(x_2) - a)| \le |f(x_1) - a| + |f(x_2) - a| < 2 \varepsilon \,\,\,\,\blacksquare$
$\Leftarrow \,\,\,\, ????$

::::

# Монотонность

## Монотонные функции, теорема о пределе монотонной и ограниченной функции


:::: {#definition-7}

**Определение:**  Пусть $f(x)$ определена на $(a, b)$ и $\forall x_1 < x_2 \in (a, b):$

1. $f(x_1) < f(x_2)$ - функция $f(x)$ возрастающая на $(a, b)$
2. $f(x_1) \le f(x_2)$ - функция $f(x)$ неубывающая на $(a, b)$
3. $f(x_1) \ge f(x_2)$ - функция $f(x)$ невозрастающая на $(a, b)$
4. $f(x_1) > f(x_2)$ - функция $f(x)$ убывающая на $(a, b)$

::::

:::: {#theorem-12}

**Теорема:**  Пусть $\forall x \in \mathring{B}_{\delta}(x_0) \,\,\,\, f(x) \ge g(x)$ и $\exists \displaystyle \lim_{x\to x_0}f(x) = a, \,\,\,\,\exists \displaystyle \lim_{x\to x_0}g(x) = b$. Тогда

1. $a \ge b$
2. Если $a > b$, то $\exists \mathring{B}_{\delta_1}(x_0):\,\,\,\, f(x) > g(x) \,\,\,\, \forall x \in \mathring{B}_{\delta_1}(x_0)$

*Доказательство:*

1. Гейне.
2. Определение для $\varepsilon = \frac{|a - b|}{3}$

::::

:::: {#theorem-13}

**Теорема:**  Пусть $\displaystyle \lim_{x\to x_0}f(x) = \displaystyle \lim_{x\to x_0}g(x) = a$ и $f(x) \le h(x) \le g(x) \,\,\,\, \forall x \in \mathring{B}_{\delta}(x_0)$. Тогда $\displaystyle \lim_{x\to x_0}h(x) = a$.

*Доказательство:* Гейне.

::::

:::: {#theorem-14}

**Теорема:**  Пусть $f(x)$ неубывает и ограничена сверху в $(x_0 - \delta, x_0)$. Тогда $\exists \displaystyle \lim_{x\to x_0-0}f(x)$.

*Доказательство:* $f(x)$ ограничена сверху $\Rightarrow \exists \sup (f(x)) = \alpha \,\,\,\, \forall \varepsilon > 0 \,\,\,\,\exists x_{\varepsilon} \in (x_0 - \delta, x_0): \,\,\,\, f(x_{\varepsilon}) > \alpha - \varepsilon \Rightarrow$, т.к. функция $f(x)$ неубывает $\forall x > x_{\varepsilon} \,\,\,\, x > \alpha - \varepsilon ????$

::::

## Непрерывные функции, локальные свойства непрерывных функций. Точки разрыва, их классификация


:::: {#definition-8}

**Определение:**  Функция $f(x)$ непрерывна в т. $x_0$, если $f(x)$ определена в т. $x_0$ и $\displaystyle \lim_{x\to x_0}f(x) = f(x_0)$

::::

**Упражнение:**<a name="exercise-0"></a> Найдите пять отличий с определением предела и придумайте определение непрерывности "по Гейне".

:::: {#theorem-15}

**Теорема:**  Пусть $f(x), g(x)$ непрерывны в т. $x_0$. Тогда $\forall \alpha, \beta \in \mathbb{R}$

1. $\alpha f(x) + \beta g(x)$ - непрерывна в точке $x_0$.
2. $f(x)\cdot g(x)$ - непрерывна в точке $x_0$.
3. Если $g(x_0) \ne 0$, то $\frac{f(x)}{g(x)}$ - непрерывна в точке $x_0$.

*Доказательство:* Пределы.

::::

:::: {#theorem-16}

**Теорема:**  (Непрерывность композиции) Пусть $f(x)$ непрерывна в т. $x_0$, $y_0 = f(x_0), \,\,\,\, g(y)$ непрерывна в т. $y_0$. Тогда $g(f(x))$ непрерывна в т. $x_0$.

*Доказательство:* Гейне ????.

::::

:::: {#definition-9}

**Определение:**  Пусть $f(x)$ определена в $B(x_0)$ и $f(x)$ не является непрерывной в т. $x_0$. Тогда $x_0$ *точка разрыва* функции $f(x)$.

::::

:::: {#definition-10}

**Определение:**  (Классификация точек разрыва) Пусть $x_0$ точка разрыва функции $f(x)$

1. Если $\exists \displaystyle \lim_{x\to x_0+0}f(x)$ и $\exists \displaystyle \lim_{x\to x_0-0}f(x)$ и

a. $\displaystyle \lim_{x\to x_0+0}f(x) = \displaystyle \lim_{x\to x_0-0}f(x)$, то $x_0$ точка *устранимого* разрыва.
b. $\displaystyle \lim_{x\to x_0+0}f(x) \ne \displaystyle \lim_{x\to x_0-0}f(x)$, то $x_0$ точка разрыва *первого рода*.

2. Если $\not\exists \displaystyle \lim_{x\to x_0+0}f(x)$ и $\nexists \displaystyle \lim_{x\to x_0-0}f(x)$, то $x_0$ точка разрыва *второго рода*. 

**Замечание:** Если предел равен $\pm \infty$, то его не сущесвует.

::::

# Глобальные свойства непрерывных функций


:::: {#definition-11}

**Определение:**  Если функция $f(x)$ непрерывна в каждой точке множества $A \subset \mathbb{R}$, то пишут $f \in C(A)$.

::::

:::: {#theorem-17}

**Теорема:**  (*1-я теорема Вейерштрасса*) Пусть $f(x) \in C[a, b]$ (непрерывна на отрезке). Тогда $f(x)$ ограничена на отрезке $[a, b]$.

*Доказательство:* (От противного) Пусть $f(x)$ не ограничена на $[a, b]$, т.е. $\forall M > 0 \,\,\,\, \exists x_M \in [a, b]: \,\,\,\, |f(x_M)| > M$. Рассмотрим последовательность $\{x_n\}_{n = 1}^{\infty}$: $|f(x_1)| > 1, \,\,\,\, |f(x_2)| > 2, \,\,\,\,\ldots \,\,\,\,\,\,\,\, \forall n \,\,\,\, x_n \in [a, b] \Rightarrow$ последовательность ограничена $\Rightarrow$ существует сходящаяся подпоследовательность $\{x_{n_k}\}_{k = 1}^{\infty}$. Пусть $\displaystyle \lim_{k \to \infty}x_{n_k} = x_0$. А так как $f(x)$ непрерывна на $[a, b]$ и $x_0 \in [a, b]$(Почему?) $\exists \displaystyle \lim_{x\to x_0}f(x_{n_k}) = f(x_0)$, что противоречит $|f(x_{n_k})| > n_k \,\,\,\, \forall k$(Где противоречие?).

::::

:::: {#theorem-18}

**Теорема:**  (*2-я теорема Вейерштрасса*) Если $f(x) \in C[a, b]$, то $\exists \min f(x)$ и $\max f(x)$ на $[a, b]$.

*Доказательство:* По [1-й теореме Вейерштрасса](#theorem-17) $f(x)$ ограничена, а значит $\exists \sup \limits_{x \in [a, b]}f(x) = \alpha$. Хочется доказать, что $\alpha \in [a, b]$. <br>
$\alpha$ - точная верхняя грань, следовательно $\exists x_1 \in [a, b]: \,\,\,\, f(x_1) > \alpha - 1, \,\,\,\,\ldots, \,\,\,\, \exists x_n \in [a, b]: \,\,\,\, f(x_n) > \alpha - \frac{1}{n}, \,\,\,\,\ldots$ $x_n \in [a, b] \,\,\,\,\forall n \Rightarrow \{x_n\}$ - ограничена на $[a, b]$. Значит $\exists \{x_{n_k}\}: \,\,\,\, \exists \displaystyle \lim_{k\to \infty}x_{n_k} = x_m \in [a, b]$(почему?). $\,\,\,\,\alpha - \frac{1}{n_k} < f(x_{n_k}) \le \alpha \Rightarrow \displaystyle \lim_{k\to \infty}f(x_{n_k}) = \alpha$, а также, так как $f(x)$ непрерывна на $[a, b]$, $\displaystyle \lim_{k \to \infty}f(x_{n_k}) = f(x_m) \,\,\,\,\blacksquare$

::::

:::: {#theorem-19}

**Теорема:**  (*О промежуточных значениях*) Пусть $f(x) \in C[a, b], \,\,\,\, A = f(a), \,\,\,\, B = f(b)$. Пусть для определенности $A \le B$. Тогда $\forall C: A \le C \le B \,\,\,\, \exists c \in [a, b]: C = f(c)$.

*Доказательство:* Пусть $C = 0, \,\,\,\, A \le 0, \,\,\,\, B \ge 0$.(В остальных случаях достаточно рассмотреть $f_1(x) = f(x) - C$) Рассмотрим последовательность вложенных отрезков $a_1 = a, \,\,\,\, b_1 = b,\,\,\,\, [a_{n+1}, b_{n+1}] = \begin{cases}
    [\frac{a_n + b_n}{2}, b_n], &\text{ если }\frac{a_n + b_n}{2} \le 0\\
    [a_n, \frac{a_n + b_n}{2}], &\text{ если }\frac{a_n + b_n}{2} > 0
\end{cases}$. По принципу полноты Кантора $\exists c: \forall n \,\,\,\, a_n \le c \le b_n, \,\,\,\, a_n \to c, \,\,\,\, b_n \to c$(почему?). Так как $f(x)$ непрерывна на $[a, b]$ и $\forall n: f(a_n) \le 0 \,\,\,\,\,\,\,\, \exists \displaystyle \lim_{n\to \infty}f(a_n) \le 0$. Аналогично $\exists \displaystyle \lim_{n\to \infty}f(b_n) \ge 0 \Rightarrow \displaystyle \lim_{n\to \infty}f(a_n) = \displaystyle \lim_{n\to \infty}f(b_n) = 0 = f(c) = C \,\,\,\,\blacksquare$

::::

## Теорема о разрывах монотонной функции Теорема о обратной функции к непрерывной и монотонной


:::: {#theorem-20}

**Теорема:**  Пусть $f(x)$ - монотонно возрастает. Тогда $f(x)$ может иметь разрывы только первого рода.

*Доказательство:* Какая-то тут лажа.

::::

:::: {#theorem-21}

**Теорема:**  Пусть $y = f(x)$ непрерывна и строго возрастает на $[a, b]$. Тогда $\exists x = f^{-1}(y)$ непрерывная и строго возрастающая на $[f(a), f(b)]$.

*Доказательство:* $f(x)$ непрерывна на $[a, b] \Rightarrow \forall C: f(a) \le C \le f(b) \,\,\,\, \exists c: f(c) = C$ по [теореме](#theorem-19). Так как функция строго возрастает, такое $c$ единственно для каждого $C$. А значит $\exists x = f^{-1}(y)$. Докажем, что $f^{-1}(y)$ строго возрастает. $\forall x_1, x_2 \in [a, b]: x_1 < x_2 \,\,\,\, f(x_1) < f(x_2) \Rightarrow \forall y_1, y_2 \in [f(a), f(b)]: y_1 < y_2 \,\,\,\, f^{-1}(x_1) < f^{-1}(x_2)$. Докажем от противного, что $f^{-1}(y)$ непрерывна на $[f(a), f(b)]$. Пусть $f^{-1}(y)$ не является непрерывной на $[f(a), f(b)]$. По [теореме](#theorem-20) у $f^{-1}(y)$ могут быть только [разрывы первого рода](#definition-10). Значит на $[f^{-1}(f(a)), f^{-1}(f(b))]$ существует интервал, в котором не существует значений $f^{-1}(y)$. Но $\forall x \in [a, b]: \exists y = f(x) \Rightarrow \exists x = f^{-1}(y) \,\,\,\,\blacksquare$

::::

# Равномерно непрерывные функции, теорема Кантора


:::: {#definition-12}

**Определение:**  Пусть $I \subset \mathbb{R}$ - промежуток. Если $\forall \varepsilon > 0 \,\,\,\, \exists \delta > 0: \forall x_1, x_2 \in I: |x_1 - x_2| < \delta \,\,\,\, |f(x_1) - f(x_2)| < \varepsilon$, то $f(x)$ - *равномерно непрерыва* на $I$.

::::

:::: {#theorem-22}

**Теорема:** (*Кантора о равномерной непрерывности*) Если $f(x)$ непрерывна на $[a, b]$, то $f(x)$ равномерно непрерывна на $[a, b]$.

*Доказательство:* (От противного) Пусть $f(x)$ не является равномерно непрерывной на $[a, b]$, то есть $\exists \varepsilon_0 > 0: \forall \delta > 0 \,\,\,\,\exists x’, x’’ \in [a, b], \,\,\,\, |x’ - x’’| < \delta: \,\,\,\, |f(x’) - f(x’’)| \ge \varepsilon_0$. Построим последовательность: 
$$x_1’, x_1’’ \in [a, b], \,\,\,\, |x_1’ - x_1’’| < 1: \,\,\,\, |f(x_1’) - f(x_1’’)| \ge \varepsilon_0$$
$$x_2’, x_2’’ \in [a, b], \,\,\,\, |x_2’ - x_2’’| < \frac{1}{2}: \,\,\,\, |f(x_2’) - f(x_2’’)| \ge \varepsilon_0$$
$$\vdots$$
$$x_n’, x_n’’ \in [a, b], \,\,\,\, |x_n’ - x_n’’| < \frac{1}{n}: \,\,\,\, |f(x_n’) - f(x_n’’)| \ge \varepsilon_0$$
$$\vdots$$
$\{x_n’\} \subset [a, b] \Rightarrow \exists \{x_{n_k}\}: \,\,\,\, \exists \displaystyle \lim_{k\to \infty}x_{n_k} = x_0$. $|x_{n_k}’ - x_{n_k}’’| < \frac{1}{n_k} \Rightarrow \displaystyle \lim_{k\to \infty}x_{n_k}’’ = x_0$(Почему?). Так как $f(x)$ непрерывна на $[a, b] \,\,\,\, \exists \displaystyle \lim_{k\to \infty}f(x_{n_k}’) = f(x_0)$ и $\exists \displaystyle \lim_{k\to \infty}f(x_{n_k}’’) = f(x_0)$. Но $|f(x_{n_k}’) - f(x_{n_k}’’)| \ge \varepsilon_0$. Противоречие(Где?) $\,\,\,\,\blacksquare$

::::

## Построение показательной функции. Логарифм, степенная функция, синус и косинус


## Замечательные пределы, следствия из них


:::: {#theorem-23}

**Теорема:**  (*Первый замечательный предел*) $$\exists \displaystyle \lim_{x\to 0}\frac{\sin(x)}{x} = 1$$

::::

:::: {#theorem-24}

**Теорема:**  $$\exists \displaystyle \lim_{x\to \infty} \left(1+ \frac{1}{x}\right)^x = e$$

*Доказательство:*

::::

:::: {#corollary-0}

**Следствие:** $$\displaystyle \lim_{x\to 0}(1+x)^{\frac{1}{x}} = e$$

*Доказательство:* очев $\,\,\,\,\blacksquare$

::::

:::: {#corollary-1}

**Следствие:**  $$\displaystyle \lim_{x\to 0}\frac{\ln(1 + x)}{x} = 1$$

*Доказательство:* $\displaystyle \lim_{x\to 0}\frac{\ln(1 + x)}{x} = \displaystyle \lim_{x\to 0}\ln((1 + x)^{\frac{1}{x}}) = \ln(e) = 1 \,\,\,\,\blacksquare$

::::

:::: {#corollary-2}

**Следствие:**  $$\displaystyle \lim_{x\to 0}\frac{e^x - 1}{x} = 1$$

*Доказательство:* Пусть $t = e^x - 1$. Тогда $\displaystyle \lim_{x\to 0}\frac{e^x - 1}{x} = \displaystyle \lim_{t\to 0}\frac{t}{\ln(t + 1)} = 1 \,\,\,\,\blacksquare$

::::

# Производная функции

## Производная суммы, произведения и отношения функций

:::: {#definition-13}

**Определение:**  Пусть $f(x)$ определена в $B(x_0), \,\,\,\, \Delta x = x - x_0$. Если $$\exists \displaystyle \lim_{\Delta x\to 0}\frac{f(x + \Delta x) - f(x)}{\Delta x} = f’(x_0),$$ то $f(x)$ имеет производную $f’(x_0)$ в т. $x_0$.

::::

:::: {#definition-14}

**Определение:**  Пусть $A \subset \mathbb{R}, \,\,\,\, \Delta x = x - x_0$. Если $$\exists \displaystyle \lim_{\Delta x\to 0, \Delta x + x_0 \in A}\frac{f(x + \Delta x) - f(x)}{\Delta x} = f’(x_0),$$ то $f(x)$ имеет производную $f’(x_0)$ по множеству $A$ в т. $x_0$.

::::

**Обозначение:** $\displaystyle \lim_{\Delta x\to 0, \Delta x < 0}\frac{f(x + \Delta x) - f(x)}{\Delta x} \stackrel{def}{=} f’_{-}(x_0) \stackrel{def}{=} f’(x_0 - 0)$

**Обозначение:** $\displaystyle \lim_{\Delta x\to 0, \Delta x > 0}\frac{f(x + \Delta x) - f(x)}{\Delta x} \stackrel{def}{=} f’_{+}(x_0) \stackrel{def}{=} f’(x_0 + 0)$

:::: {#theorem-25}

**Теорема:**  Пусть $f(x)$ имеет производную $f’(x_0)$ в т. $x_0$. Тогда $f(x)$ непрерывна в т. $x_0$.

*Доказательство:* $\displaystyle \lim_{x\to x_0}(f(x) - f(x_0)) = \displaystyle \lim_{x\to x_0}\frac{f(x) - f(x_0)}{x - x_0}\cdot(x - x_0) = f’(x_0)\cdot 0 = 0$. А значит по [теореме](#theorem-2) $f(x)$ непрерывна в т. $x_0 \,\,\,\,\blacksquare$

::::

:::: {#theorem-26}

**Теорема:**  Пусть $\exists f’(x_0)$ и $\exists g’(x_0)$. Тогда $$\exists (f(x) + g(x))’_{|x = x_0} = f’(x_0) + g’(x_0)$$

*Доказательство:* очев $\,\,\,\,\blacksquare$

::::

:::: {#theorem-27}

**Теорема:**  Пусть $\exists f’(x_0)$ и $\exists g’(x_0)$. Тогда $$\exists (f(x) \cdot g(x))’_{|x = x_0} = f’(x_0)\cdot g(x_0) + g’(x_0) \cdot f(x_0)$$

*Доказательство:* $$\displaystyle \lim_{\Delta x\to 0}\frac{f(x + \Delta x) \cdot g(x + \Delta x) - f(x)\cdot g(x)}{\Delta x} =$$ $$=\displaystyle \lim_{\Delta x\to 0}\frac{f(x + \Delta x) \cdot g(x + \Delta x) - g(x + \Delta x) \cdot f(x) - f(x)\cdot g(x) + g(x + \Delta x) \cdot f(x)}{\Delta x} =$$
$$=\displaystyle \lim_{\Delta x\to 0}\frac{g(x + \Delta x)\cdot (f(x + \Delta x) - f(x)) + f(x)\cdot (g(x + \Delta x) - g(x))}{\Delta x} =$$
$$=\displaystyle \lim_{\Delta x\to 0}\frac{g(x + \Delta x)\cdot (f(x + \Delta x) - f(x))}{\Delta x} + \frac{f(x)\cdot (g(x + \Delta x) - g(x))}{\Delta x} =$$
$$=f’(x_0)\cdot g(x_0) + g’(x_0) \cdot f(x_0) \,\,\,\,\blacksquare$$

::::

:::: {#theorem-28}

**Теорема:**  Пусть $\exists f’(x_0)$ и $\exists g’(x_0)$. Тогда $$\exists \left( \frac{f(x)}{g(x)}\right)’_{|x = x_0} = \frac{f’(x_0)\cdot g(x_0) - g’(x_0) \cdot f(x_0)}{g(x_0)^2}$$

*Доказательство:* $$\left( \frac{f(x)}{g(x)}\right)’_{|x = x_0} =$$
$$\displaystyle \lim_{\Delta x\to 0}\frac{\frac{f(x + \Delta x)}{g(x + \Delta x)} - \frac{f(x)}{g(x)}}{\Delta x} =$$
$$\displaystyle \lim_{\Delta x\to 0}\frac{f(x + \Delta x) \cdot g(x) - f(x)\cdot g(x + \Delta x)}{\Delta x \cdot g(x + \Delta x) \cdot g(x)} =$$
$$= \left( \frac{f(x)}{g(x)}\right)’_{|x = x_0} = \frac{f’(x_0)\cdot g(x_0) - g’(x_0) \cdot f(x_0)}{g(x_0)^2} \,\,\,\,\blacksquare$$

::::

## Производная композиции функций, производная обратной функции


:::: {#theorem-29}

**Теорема:**  Пусть $f(x)$ непрерывна строго возрастает в $B(x_0)$, $\exists f^{-1}(y)$ в $B(y_0), \,\,\,\, y_0 = f(x_0)$ и $\exists f’(x_0) \ne 0$. Тогда $\exists \left(f^{-1}(y)\right)’_{|y = y_0} = \frac{1}{f’(x_0)}$.

*Доказательство:* $\left(f^{-1}(y)\right)’_{|y = y_0} = \displaystyle \lim_{y\to y_0}\frac{f^{-1}(y) - f^{-1}(y_0)}{y - y_0} = \displaystyle \lim_{x\to x_0}\frac{x - x_0}{f(x) - f(x_0)} = \frac{1}{f’(x_0)}$ (С чего мы можем заменить $x \to x_0$ на $y \to y_0$?)

::::

:::: {#theorem-30}

**Теорема:**  Пусть $\exists g’(x_0)$ и $\exists f’(g(x_0)$. Тогда $$\exists f(g(x))’_{|x = x_0} = f’(g(x_0))\cdot g’(x_0)$$

*Доказательство:* Пусть $f(x) \ne f(x_0)$ при $x \ne x_0$. $$f(g(x))’_{|x = x_0} = \displaystyle \lim_{x\to x_0}\frac{f(g(x)) - f(g(x_0))}{x - x_0}$$ $$= \displaystyle \lim_{x\to x_0}\frac{f(g(x)) - f(g(x_0))}{x - x_0}\cdot \frac{g(x) - g(x_0)}{g(x) - g(x_0)} = f’(g(x_0))\cdot g’(x_0)\,\,\,\,\blacksquare$$

::::

## Таблица производных

| Функция      | Производная |
| -----------  | ----------- |
| $x^{\alpha}$ | $\alpha \cdot x^{\alpha - 1}$|
| $\sin(x)$    | $\cos(x)$ |
| $\cos(x)$    | $-\sin(x)$ |
| $\tan(x)$    | $\frac{1}{\cos^2(x)}$ |
| $\cot(x)$    | $-\frac{1}{\sin^2(x)}$ |
| $\sin^{-1}(x)$    | $\frac{1}{\sqrt{1 - x^2}}$ |
| $\cos^{-1}(x)$    | $-\frac{1}{\sqrt{1 - x^2}}$ |
| $\tan^{-1}(x)$    | $\frac{1}{1 + x^2}$ |
| $\cot^{-1}(x)$    | $-\frac{1}{1 + x^2}$ |
| $\ln(x)$    | $\frac{1}{x}$ |
| $\log_a(x)$    | $\frac{1}{x\cdot \ln(a)}$ |
| $e^x$    | $e^x$ |
| $a^x$    | $a^x\cdot \ln(a)$ |
| $\sinh(x)$    | $\cosh(x)$ |
| $\cosh(x)$    | $\sinh(x)$ |


# Дифференцируемость функций, первый дифференциал

:::: {#definition-15}

**Определение:**  *Дифференцирование* - это нахождение дифференциала.

::::

:::: {#definition-16}

**Определение:**  Пусть $f(x)$ определена в $B(x_0)$. Если $\exists A \in \mathbb{R}$, такое что
$$f(x + \Delta x) - f(x) = A\cdot \Delta x + \overline{\overline{o}}(\Delta x), \,\,\,\, \Delta x \to 0,$$
то $f(x)$ *дифференцируема* в т. $x_0$, а главная линейная часть $A\cdot \Delta x$ ее полного приращения $f(x + \Delta x) - f(x)$ - *первый дифференциал* $f(x)$ в т. $x_0$.

**Обозначение:** $df(x) \stackrel{def}{=} A\cdot  \Delta x$

::::

## Связь между дифференцируемостью и существованием производной

:::: {#theorem-31}

**Теорема:**  $f(x)$ дифференцируема в т. $x_0 \Leftrightarrow \exists f’(x_0)$.

*Доказательство:* Записать определение того и другого.

::::

:::: {#definition-17}

**Определение:**  Если $f(x)$ дифференцируема во всех точках множества $X \subset \mathbb{R}$, то $f(x) \in \mathcal{D}(X)$ (множество всех дифференцируемых функций на $X$).

::::

### Дифференциал независимой переменной

Пусть $f(x) = x$. Посчитаем дифференциал: $f(x + \Delta x) - f(x) = x + \Delta x - x = \Delta x = dx$. 

## Полукасательные и касательная к графику функции. Геометрический смысл первого дифференциала. Инвариантность первого дифференциала и неинвариантность производной


### Инвариантность первого дифференциала и неинвариантность производной

Берем функцию $f(x)$ считаем дифференциал: $df(x) = f’(x)dx$. Вспоминаем, что $f(x) = f(g(t))$. Ни о чем не заботясь, вставляем: $df(g(t)) = f’(g(t))dg(t) = f’(g(t))g’(t)dt$. Теперь посчитаем дифференциал $f(g(t))$: $df(g(t)) = (f(g(t)))’dt = f’(g(t))g’(t)dt$. Следовательно первый дифференциал инвариантен $\,\,\,\,\blacksquare$.

Попробуем то же самое с производной. Пусть $f’(x)$ производная. Вспоминаем, что $f(x) = f(g(t))$. Ни о чем не заботясь, вставляем: $f’(g(t))$. Посчитаем производную по правилам: $(f(g(t)))’ = f’(g(t))g’(t)$. Следовательно производная неинвариантна $\,\,\,\,\blacksquare$.

### Полукасательные и касательная к графику функции

<iframe src="https://www.desmos.com/calculator/ozskwyjrex?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

:::: {#definition-18}

**Определение:**  Если в т. $x_0 \,\,\,\, f_{-}’(x_0) = f_{+}’(x_0)$, то прямая $y = f(x_0) + f’(x_0)\cdot (x - x_0)$ - *касательная* к графику $f(x)$ в т. $x_0$.

::::

### Геометрический смысл первого дифференциала

$df(x_0) = f’(x_0)dx = f’(x_0)(x - x_0)$. То есть касательная к графику $f(x)$ в т. $x_0$ - это $y = f(x_0) + df(x_0)$.

## Старшие производные. Старшие дифференциалы. Неинвариантность второго дифференциала


![](img/cat.gif){width="200px" height="200px"}

:::: {#definition-19}

**Определение:**  Пусть $f(x)$ определена в $B_{\delta}(x_0)$ и $\forall x \in B_{\delta}(x_0) \,\,\,\, f(x) < f(x_0)$. Тогда $f(x)$ имеет строгий локальный максимум в т. $x_0$.

::::

**Упражнение:**<a name="exercise-1"></a> Вы ведь все поняли? Запишите, не глядя сюда, определение локального минимума.

:::: {#theorem-32}

## Теорема Ферма

**Теорема:**  (Ферма) Пусть $f(x)$ определена в $B_{\delta}(x_0)$ и имеет строгий локальный максимум в т. $x_0$. Тогда <br>
Если $\exists f_{-}’(x_0)$, то $f_{-}’(x_0) \ge 0$<br>
Если $\exists f_{+}’(x_0)$, то $f_{+}’(x_0) \le 0$<br>

*Доказательство:* $\forall x \in B(x_0) \,\,\,\, f(x) < f(x_0)$. $f_{-}’(x_0) = \displaystyle \lim_{\Delta x\to 0, \Delta x < 0}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} \Rightarrow f_{-}’(x_0) \ge 0 \,\,\,\,\blacksquare$

::::

## Необходимый признак локального экстремума

:::: {#corollary-3}

**Следствие:**  Если в условиях теоремы $\exists f’(x_0)$, то $f’(x_0) = 0$.

*Доказательство:* очев $\,\,\,\,\blacksquare$

::::

:::: {#theorem-33}

## Теорема Ролля

**Теорема:**  (Ролля) Если $f(x) \in C[a, b], \,\,\,\, f(x) \in \mathcal{D}(a, b)$ и $f(a) = f(b)$, то $\exists c \in (a, b): f’(c) = 0$.

*Доказательство:* По [2-й теореме Вейерштрасса](#theorem-18) на $[a, b] \,\,\,\, \exists \min{f(x)} = x_{min}$ и $\exists \max{f(x)} = x_{max}$. Если $x_{min} \in (a, b)$, то по [следствию](#corollary-3) $f’(x_{min}) = 0$.

Если $x_{max} \in (a, b)$, то по [следствию](#corollary-3) $f’(x_{max}) = 0$.
Иначе $f(x_{max}) = f(x_{min}) = f(a) = f(b) \Rightarrow f(x) = const \Rightarrow \forall x \in (a, b) \,\,\,\, f’(x) = 0 \,\,\,\,\blacksquare$

::::

## Формула Лагранжа и следствие из неё

:::: {#theorem-34}

**Теорема:**  (Лагранжа) Если $f(x) \in C[a, b], \,\,\,\, f(x) \in \mathcal{D}(a, b)$, то $\exists c \in (a, b): f’(c)\cdot (b - a) = f(b) - f(a)$.

*Доказательство:* Рассмотрим функцию $\varphi (x) = f(x) - \frac{f(b) - f(a)}{b - a}(x - a)$. $\varphi (a) = f(a) = \varphi (b) \Rightarrow$ по [теореме Ролля](#theorem-33) $\exists c \in (a, b): \,\,\,\, \varphi ’(c) = 0 = f’(c) - \frac{f(b) - f(a)}{b - a} \,\,\,\,\blacksquare$

::::

:::: {#corollary-4}

**Следствие:**  Если $\forall x \in (a, b) \,\,\,\, f ’(x) = 0$, то $f(x) = const$.

*Доказательство:*

::::

## Формула Коши. Связь монотонности функции и знака производной


:::: {#theorem-35}

**Теорема:**  (*Формула Коши*) Если $f(x), g(x) \in C[a, b], \,\,\,\, f(x), g(x) \in \mathcal{D}(a, b), \,\,\,\, g’(x) \ne 0 \,\,\,\, \forall x \in (a, b)$, то $\exists c \in (a, b): \frac{f’(c)}{g’(c)} = \frac{f(b) - f(a)}{g(b) - g(a)}$.

*Доказательство:* $g(b) \ne g(a)$ по [теореме Ролля](#theorem-33). Рассмотрим функцию $\varphi (x) = f(x) - \frac{f(b) - f(a)}{g(b) - g(a)}(g(x) - g(a))$. $\varphi (a) = f(a) = \varphi (b) \Rightarrow$ по [теореме Ролля](#theorem-33) $\exists c \in (a, b): \,\,\,\, \varphi ’(c) = 0 = f’(c) - \frac{f(b) - f(a)}{g(b) - g(a)} \,\,\,\,\blacksquare$

::::

:::: {#theorem-38}

**Теорема:**  

1. Пусть $f(x) \in \mathcal{D}(a, b)$ и возрастает на $(a, b)$. Тогда $f’(x) \ge 0$ на $(a, b)$.
2. Пусть $f(x) \in \mathcal{D}(a, b)$ и $f’(x) \ge 0$ на $(a, b)$. Тогда $f(x)$ возрастает на $(a, b)$.
3. Пусть $f(x) \in \mathcal{D}(a, b)$ и $f’(x) > 0$ на $(a, b)$. Тогда $f(x)$ строго возрастает на $(a, b)$.

*Доказательство:* 1. $\forall x_1, x_2 \in (a, b) \,\,\,\, \frac{f(x_2) - f(x_1)}{x_2 - x_1} \ge 0$, так как из $x_2 > x_1$ следует $f(x_2) \ge f(x_1)$. Зафиксируем $x_1$. Тогда из [теоремы](#theorem-12) следует $f’(x_1) \ge 0 \,\,\,\,\blacksquare$

2. почти также.
3. совсем также.

::::

## Отсутствие у производной дифференцируемой функции устранимых разрывов и разрывов первого рода


:::: {#theorem-36}

**Теорема:**  Если $f(x) \in \mathcal{D}(a, b)$, то у $f(x)$ нет разрывов первого рода и устранимых разрывов на $(a, b)$.

*Доказательство:* Ну, лажа тут какая-то.

::::

:::: {#theorem-37}

## Теорема Дарбу о промежуточных значениях производной

**Теорема:**  (Дарбу) Пусть $f(x) \in \mathcal{D}[a, b], \,\,\,\, A = f’(a), \,\,\,\, B = f’(b)$. Тогда $\forall C$ между $A$ и $B \,\,\,\, \exists c \in [a, b]: \,\,\,\, f’(c) = C$.

*Доказательство:* Интересно, я просто устала или тут тоже лажа? Никому не интересно.

короче, и тут котик получился:  

![](img/cat.gif){width="200px" height="200px"}

::::

# Правила Лопиталя


:::: {#theorem-39}

**Теорема:**  Пусть $f(x), g(x) \in \mathcal{D}(B(x_0)),\,\,\,\, g(x) \ne 0 \,\,\,\, \forall x \in \mathring{B}(x_0), \,\,\,\, g’(x_0) \ne 0, \,\,\,\, g(x_0) = f(x_0) = 0.$ Тогда $$\displaystyle \lim_{x\to x_0}\frac{f(x)}{g(x)} = \frac{f’(x_0)}{g’(x_0)}$$ 

*Доказательство:* $$\displaystyle \lim_{x\to x_0}\frac{f(x)}{g(x)} = \displaystyle \lim_{x\to x_0}\frac{f(x) - f(x_0)}{g(x) - g(x_0)} = \displaystyle \lim_{x\to x_0}\frac{\frac{f(x) - f(x_0)}{x - x_0}}{\frac{g(x) - g(x_0)}{{x - x_0}}} = \frac{f’(x_0)}{g’(x_0)} \,\,\,\,\blacksquare$$

::::

:::: {#theorem-40}

**Теорема:**  Пусть $f(x), g(x) \in \mathcal{D}(B(x_0)), \,\,\,\, g(x) \ne 0, \,\,\,\, g’(x) \ne 0, \,\,\,\, \displaystyle \lim_{x\to x_0}f(x) = \displaystyle \lim_{x\to x_0}g(x) = 0.$ Тогда

1. Если $\exists \displaystyle \lim_{x\to x_0}\frac{f’(x)}{g’(x)} = A$, то $\exists \displaystyle \lim_{x\to x_0}\frac{f(x)}{g(x)} = A$.
2. Если $\exists \displaystyle \lim_{x\to x_0}\frac{f’(x)}{g’(x)} = \infty$, то $\exists \displaystyle \lim_{x\to x_0}\frac{f(x)}{g(x)} = \infty$.

*Доказательство:* Доопределим $f(x)$ и $g(x)$ в т. $x_0$ нулями. По [формуле Коши](#theorem-35) $\forall x \in [x_0, ?] \,\,\,\, \exists c: \,\,\,\, \frac{f(x)}{g(x)} = \frac{f(x) - f(x_0)}{g(x) - g(x_0)} = \frac{f’(c)}{g’(c)}$

::::

:::: {#theorem-41}

**Теорема:**  Пусть $f(x), g(x) \in \mathcal{D}(a, +\infty), \,\,\,\, a > 0, \,\,\,\, g(x) \ne 0, \,\,\,\, g’(x) \ne 0, \,\,\,\, \displaystyle \lim_{x\to +\infty}f(x) = \displaystyle \lim_{x\to +\infty}g(x) = 0.$ Тогда

1. Если $\exists \displaystyle \lim_{x\to +\infty}\frac{f’(x)}{g’(x)} = A$, то $\exists \displaystyle \lim_{x\to +\infty}\frac{f(x)}{g(x)} = A$.
2. Если $\exists \displaystyle \lim_{x\to +\infty}\frac{f’(x)}{g’(x)} = \infty$, то $\exists \displaystyle \lim_{x\to +\infty}\frac{f(x)}{g(x)} = \infty$.

*Доказательство:* Рассмотрим $\phi(t) = f(\frac{1}{t}), \,\,\,\, \psi(t) = g(\frac{1}{t})$ на $(0, \frac{1}{a})$. $\phi’(t) = -\frac{1}{t^2}\cdot f’(\frac{1}{t}), \,\,\,\, \psi’(t) = -\frac{1}{t^2}\cdot g’(\frac{1}{t}) \Rightarrow \frac{\phi ’(x)}{\psi ’(x)} = \frac{f’(x)}{g’(x)}$ далее по [теореме](#theorem-40) $\,\,\,\,\blacksquare$

::::

:::: {#theorem-42}

**Теорема:**  Пусть $f(x), g(x) \in \mathcal{D}(a - \delta, a), \,\,\,\, g(x) \ne 0, \,\,\,\, g’(x) \ne 0, \,\,\,\, \displaystyle \lim_{x\to a-0}f(x) = \displaystyle \lim_{x\to a-0}g(x) = 0.$ Тогда

1. Если $\exists \displaystyle \lim_{x\to a-0}\frac{f’(x)}{g’(x)} = A$, то $\exists \displaystyle \lim_{x\to a-0}\frac{f(x)}{g(x)} = A$.
2. Если $\exists \displaystyle \lim_{x\to a-0}\frac{f’(x)(}{g’(x)} = \infty$, то $\exists \displaystyle \lim_{x\to a-0}\frac{f(x)}{g(x)} = \infty$.

*Доказательство:*

1. $\displaystyle \lim_{x\to a-0}\frac{f’(x)}{g’(x)} = A$, то есть $\forall \varepsilon > 0 \,\,\,\, \exists \delta_1 > 0: \,\,\,\, \forall x \in (a  - \delta_1, a) \,\,\,\, |\frac{f’(x)}{g’(x)} - A| < \varepsilon$. Пусть $x_0 \in (a - \delta_1, a)$

::::

# Формула Тейлора

:::: {#definition-20}

**Определение:**  Пусть $\exists f^{(n)}(x_0)$. Выражение $f(x) = \displaystyle \sum_{k = 0}^{n}\frac{f^{(k)}(x_0)}{k!}\cdot (x - x_0)^k + r_n(x, x_0)$ - *формула Тейлора* для $f(x)$ с центром разложения в т.$x_0$.

::::

## Остаточный член в форме Пеано и в общей форме. Остаточный член в форме Лагранжа

:::: {#theorem-43}

**Теорема:**  (Остаточный член в форме Пеано) $$r_n(x, x_0) = \overline{\overline{o}}((x - x_0)^n)$$

*Доказательство:* $$\displaystyle \lim_{x\to x_0}\frac{r_n(x, x_0)}{(x - x_0)^n} = \displaystyle \lim_{x\to x_0}\frac{f(x) - \displaystyle \sum_{k = 0}^{n}\frac{f^{(k)}(x_0)}{k!}\cdot (x - x_0)^k}{(x - x_0)^n} \stackrel{?}{=}$$ 
$$\stackrel{?}{=}\displaystyle \lim_{x\to x_0}\frac{f’(x) - \displaystyle \sum_{k = 1}^{n}\frac{f^{(k)}(x_0)}{(k - 1)!}\cdot (x - x_0)^{k - 1}}{n \cdot (x - x_0)^{n - 1}}\stackrel{?}{=}\ldots \stackrel{?}{=}$$
$$\stackrel{?}{=} \displaystyle \lim_{x\to x_0}\frac{f^{(n - 1)}(x) - f^{(n - 1)}(x_0) - f^{(n)}(x_0)\cdot (x - x_0)}{n! \cdot (x - x_0)} = 0 \,\,\,\,\blacksquare$$

::::

:::: {#theorem-44}

**Теорема:**  (Остаточный член в общей форме) Пусть $f(t) \in \mathcal{D}^n[x, x_0]$ и $f(t) \in \mathcal{D}^{n + 1}(x, x_0), \,\,\,\, \varphi (x) \in C[x, x_0], \,\,\,\, \varphi (x) \in \mathcal{D}(x, x_0), \,\,\,\, \varphi’(x) \ne 0$. Тогда $$\exists c \in (x, x_0): \,\,\,\,r_n(x, x_0) = \frac{f^{(n + 1)}(c) \cdot (x - c)^n}{n!} \cdot \frac{\varphi(x) - \varphi(x_0)}{\varphi’(c)}$$

*Доказательство:* Пусть $\psi(t) = \displaystyle \sum_{k = 0}^{n}\frac{f^{(k)}(t)}{k!}\cdot (x - t)^k$. Тогда $\psi(x_0) = \displaystyle \sum_{k = 0}^{n}\frac{f^{(k)}(x_0)}{k!}\cdot (x - x_0)^k, \,\,\,\, \psi(x) = f(x)$. $$\psi’(t) = \displaystyle \sum_{k = 0}^{n}\frac{f^{(k + 1)}(t)}{k!}\cdot (x - t)^k - \displaystyle \sum_{k = 1}^{n}\frac{f^{(k)}(t)}{(k - 1)!}\cdot (x - t)^{k - 1} = \frac{f^{(n + 1)}(t)}{n!}\cdot (x - t)^n$$
$$\frac{r_n(x, x_0)}{\varphi(x) - \varphi(x_0)} = \frac{\psi(x) - \psi(x_0)}{\varphi(x) - \varphi(x_0)} \stackrel{\text{т. Коши}}{=} \frac{\psi’(c)}{\varphi’(c)} = \frac{1}{\varphi’(c)}\cdot \frac{f^{(n + 1)}(c)}{n!}\cdot (x - c)^n \,\,\,\,\blacksquare$$

::::

:::: {#corollary-5}

**Следствие:**  (Остаточный член в форме Лагранжа) $$r_n(x, x_0) = \frac{f^{(n + 1)}(c)\cdot (x - x_0)^{n + 1}}{(n + 1)!}$$

*Доказательство:* Возьмем $\varphi(x) = (x - x_0)^{n}$. Запишем остаточный член в общей форме: $$\frac{f^{(n + 1)}(c) \cdot (x - c)^n}{n!} \cdot \frac{(x - x_0)^{n} - 0}{n \cdot (x - x_0)^{n - 1}} = \frac{f^{(n + 1)}(c)\cdot (x - x_0)^{n + 1}}{(n + 1)!} \,\,\,\,\blacksquare$$

::::


##  Формула Тейлора для основных элементарных функций. Достаточные условия локального экстремума. Общая схема поиска глобального экстремума функции на отрезке


:::: {#theorem-45}

**Теорема:**  Пусть $f(x) \in \mathcal{D}(x_0)$.
Если при $x < x_0 \,\,\,\, f’(x) < 0$, при $x > x_0 \,\,\,\, f’(x) > 0$, то в т. $x_0$ минимум функции $f(x)$.

*Доказательство:* По [т. Лагранжа](#theorem-34) для $\forall x < x_0 \,\,\,\, \exists c \in (x, x_0): \,\,\,\, f(x_0) - f(x) = f’(c)\cdot (x_0 - x) (1)$. Так как $c \in (x, x_0) \,\,\,\, f’(c) < 0$ и из $x < x_0$ следует $x_0 - x > 0$. Значит правая часть равенства $(1)$ отрицательна $\Rightarrow \forall x < x_0 \,\,\,\, f(x) > f(x_0) \,\,\,\,\blacksquare$

::::

**Упражнение:**<a name="exercise-2"></a> Дописать доказательство, сформулировать теорему для максимума и доказать ее.

**Упражнение:**<a name="exercise-3"></a> Понять почему в доказательстве можно применять т. Лагранжа.

# Выпуклые функции

:::: {#definition-21}

**Определение:**  Для $f(x), \,\,\,\, x_1, \,\,\,\, x_2 \,\,\,\,\,\,\,\, l(x) = \frac{f(x_1)\cdot (x_2 - x) + f(x_2)\cdot (x - x_1)}{x_2 - x_1}$. (Прямая, проходящая через две заданные точки функции)

::::

:::: {#definition-22}

**Определение:**  Пусть $f(x)$ определена на $(a, b)$. Если $\forall x_1 < x_2 \in (a, b)$ и $\forall x \in (x_1, x_2)$:

1. $f(x) \le l(x)$, то $f(x)$ *выпуклая вниз*.
2. $f(x) \ge l(x)$, то $f(x)$ *выпуклая вверх*.

::::

## Достаточное условие строгой выпуклости

:::: {#theorem-46}

**Теорема:**  Если на $(a, b) \,\,\,\, f’’(x) > 0$, то $f(x)$ выпукла вниз на $(a, b)$.

*Доказательство:* $\forall x_1 < x_2 \in (a, b)$

$$l(x) - f(x) = \frac{f(x_1)\cdot (x_2 - x) + f(x_2)\cdot (x - x_1)}{x_2 - x_1} - f(x) \cdot \frac{(x_2 - x) + (x - x_1)}{x_2 - x_1} =$$
$$=\frac{(f(x_1) - f(x))\cdot (x_2 - x) + (f(x_2) - f(x))\cdot (x - x_1)}{x_2 - x_1}$$
По [теореме Лагранжа](#theorem-34) $\exists \xi, \zeta:\,\,\,\, f(x_1) - f(x) = f’(\xi)\cdot (x_1 - x) \,\,\,\, f(x_2) - f(x) = f’(\zeta)\cdot (x_2 - x)$.
$$=\frac{f’(\xi)\cdot (x_1 - x) \cdot (x_2 - x) + f’(\zeta)\cdot (x_2 - x)\cdot (x - x_1)}{x_2 - x_1}=$$
$$=\frac{(x_1 - x) \cdot (x_2 - x)(f’(\xi) - f’(\zeta))}{x_2 - x_1}$$
По [теореме Лагранжа](#theorem-34) $\exists \eta:\,\,\,\, f’(\xi) - f’(\zeta) = f’’(\eta)\cdot (\xi - \zeta)$.
$$=\frac{(x_1 - x) \cdot (x_2 - x) \cdot f’’(\eta)\cdot (\xi - \zeta)}{x_2 - x_1}$$ (Почему $\xi - \zeta >0$?)

::::

:::: {#theorem-47}

**Теорема:**  Если на $(a, b) \,\,\,\, f’’(x) > 0$, то $$\forall x_0, x \in (a, b) \,\,\,\, f(x) > f(x_0) + f’(x_0)\cdot (x - x_0)$$

*Доказательство:* Без ограничения общности докажем для $x_0 < x$.
$$f(x) = f(x_0) + f’(x_0)\cdot (x - x_0) + (f(x) - f(x_0)) - f’(x_0)\cdot (x - x_0) =$$
По [теореме Лагранжа](#theorem-34) $\exists x_0 < \zeta < x:\,\,\,\, f(x) - f(x_0) = f’(\zeta)\cdot (x - x_0)$.
$$= f(x_0) + f’(x_0)\cdot (x - x_0) + (f’(\zeta)\cdot (x - x_0)) - f’(x_0)\cdot (x - x_0) =$$
$$= f(x_0) + f’(x_0)\cdot (x - x_0) + (x - x_0) \cdot (f’(\zeta) - f’(x_0)) =$$
$$=f(x_0) + f’(x_0)\cdot (x - x_0) + (x - x_0)\cdot (\zeta - x_0) \cdot f’’(\xi) \Rightarrow$$
$$(x - x_0 > 0, \,\,\,\, \zeta - x_0 > 0, \,\,\,\, f’’(\xi) > 0)$$
$$f(x) - f(x_0) + f’(x_0)\cdot (x - x_0) = (x - x_0)\cdot (\zeta - x_0) \cdot f’’(\xi) > 0 \,\,\,\,\blacksquare$$

::::

**Упражнение:**<a name="exercise-4"></a> Докажите эту теорему для $f’’(x) < 0$.

:::: {#definition-23}

**Определение:**  Пусть $f(x)$ определена в $B(x_0)$ и $\exists f’(x_0)$.

Если выражение $f(x) - (f(x_0) + f’(x_0)\cdot (x - x_0)$ имеет разный знак при $x < x_0$ и $x > x_0$, $x_0$ - *точка перегиба* графика функции $f(x)$.

::::

## Необходимое и достаточные условия наличия точки перегиба

:::: {#theorem-48}

**Теорема:**  (*Необходимое условие существования точки перегиба*) Пусть $f(x)$ дважды дифференцируема в $B(x_0)$. Если $x_0$ точка перегиба $f(x)$, то $f’’(x_0) = 0$.

*Доказательство:* (от противного) Пусть $f’’(x_0) > 0$. Тогда $\exists B_1(x_0):\,\,\,\, \forall x \in B_1(x_0) \Rightarrow$ по [теореме](#theorem-47) $f(x) - (f(x_0) + f’(x_0)\cdot (x - x_0) > 0 \,\,\,\,\blacksquare$

::::

:::: {#theorem-49}

**Теорема:** (*1-е достаточное условие существования точки перегиба*) Пусть $f(x)$ дифференцируема в $B(x_0)$ и дважды дифференцируема в $\mathring{B(x_0)}$. Если $f’’(x_0)$ имеет разные знаки при $x < x_0$ и $x > x_0$, то $x_0$ - точка перегиба $f(x)$.

*Доказательство:* Из [теоремы](#theorem-47) и [упражнения](#exercise-4) следует, что при $x < x_0$ и $x > x_0$ выражение $f(x) - (f(x_0) + f’(x_0)\cdot (x - x_0)$ имеет разные знаки $\,\,\,\,\blacksquare$.

::::

:::: {#theorem-50}

**Теорема:**  (*2-е достаточное условие существования точки перегиба*) Пусть $f(x)$ трижды дифференцируема в $B(x_0)$. Если $f’’’(x_0) \ne 0$ и $f’’(x_0) = 0$, то $x_0$ - точка перегиба $f(x)$.

*Доказательство:* $f(x) - f(x_0) - f’(x_0)\cdot (x - x_0) = f’(\zeta)\cdot (x - x_0) - f’(x_0)\cdot (x - x_0) = f’’(\xi)\cdot (\zeta - x_0) \cdot (x - x_0)????$

::::

### Асимптоты

:::: {#definition-24}

**Определение:**  Если $f(x)$ определена в $\mathring{B}(x_0)$ и $\displaystyle \lim_{x\to x_0+0}f(x) = \pm\infty$ или $\displaystyle \lim_{x\to x_0-0}f(x) = \pm\infty$, то прямая $y = x_0$ - *вертикальная асимптота* графика функции $f(x)$.

::::

:::: {#definition-25}

**Определение:**  Если $\displaystyle \lim_{x\to \pm\infty}(f(x) - (kx + b)) = 0$ то прямая $y = kx + b$ - *наклонная асимптота* графика функции $f(x)$.

::::

:::: {#theorem-51}

**Теорема:**  Прямая $y = kx + b$ наклонная асимптота графика функции $f(x)$ $\Leftrightarrow \exists \displaystyle \lim_{x\to \pm\infty}\frac{f(x)}{x} = k$ и $\displaystyle \lim_{x\to \pm\infty}(f(x) - kx) = b$.

*Доказательство:* $\displaystyle \lim_{x\to \pm\infty}(f(x) - (kx + b)) = 0 \Rightarrow f(x) - kx = b + \overline{\overline{o}}(1)$, при $x \to \pm\infty \Rightarrow \frac{f(x)}{x} = k + \overline{\overline{o}}(1)$ , при $x \to \pm\infty \,\,\,\,\blacksquare$

::::

