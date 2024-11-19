# О попятном движении планет
 
![](opop_1.png)

В астрономии известно явление, когда при наблюдении планет их видимое среди звезд движение меняет направление на небольшой срок, в результате планета проходит как бы по петле. В работе авторы стараются
подробно рассмотреть это явление, предлагается способ найти некоторые характеристики попятного движения планет.
Формализуем задачу. Рассмотрим движение двух материальных точек по круговым концентрическим траекториям с постоянной угловой скоростью. Такая модель хорошо описывает поведение настоящих планет
и потенциально допускает обобщение задачи с учетом наклонения орбит. Обозначим как $\overline{r}_1$, $\overline{r}_2$ — радиус-векторы планет, $\overline{\omega}_1$, $\overline{\omega}_2$ — угловые скорости, $\overline{v}_1$, $\overline{v}_2$  — скорости. $\overline{a}_1$, $\overline{v}_2$   — радиусы орбит.

![](opop_2.png)

*Рис. 1: Схема к задаче о попятном движении. Планеты 1 и 2 движутся по круговым орбитам вокруг Солнца (их радиус-векторы — r1 и r2). r —
вектор, соединяющий планеты, соответствует направлению наблюдения, его изменения отражаются
в перемещении планеты на фоне далёких звёзд.*

Положение планеты на небе Земли определяется направлением вектора $\overline{r} = \overline{r}_1 + \overline{r}_2$. Движение планеты
связано с угловой скоростью $\overline{\omega}$ вектора $\overline{r}$ (прямой связи со смещением вектора $\overline{r}$ нет, т.к фоновые звезды удалены на бесконечность.) Заметим, что $\overline{\omega}$ связана с движением планеты относительно Земли:

$$
\overline{\omega} \times \overline{r} = \overline{v}_2 - \overline{v}_1.
$$

Отсюда легко выражается $\omega$: 

$$
\overline{\omega} = \frac{\overline{r} \times (\overline{v}_2 - \overline{v}_1)}{|\overline{r}|^2}.
$$

Остаётся установить зависимость этой величины от
времени. Скорости легко переписать через радиус- векторы планет и их угловые скорости. Для радиус-вектора
зависимость от времени имеет вид:

$$
\overline{r}_n = \begin{pmatrix} a_n \sin \omega_n t \\ a_n \cos \omega_n t \end{pmatrix}.
$$

Тогда справедливо:

$$
|\overline{r}|^2 = a_1^2 + a_2^2 - 2a_1a_2(\sin \omega_1t \sin \omega_2t + \cos \omega_1t \cos \omega_2t).
$$

С числителем выражения $\overline{\omega} = \frac{\overline{r} \times (\overline{v}_2 - \overline{v}_1)}{|\overline{r}|^2}$ можно немного поработать:


$\overline{r} \times (\overline{v}_2 - \overline{v}_1) = $
$a_1^2 \omega_1 + a_2^2 \omega_2 - (\overline{r}_1, \overline{r}_2)(\overline{\omega}_1 + \overline{\omega}_2) = $
$a_1^2 \omega_1 + a_2^2 \omega_2 - a_1 a_2 (\sin \omega_1 t \sin \omega_2 t + \cos \omega_1 t \cos \omega_2 t)(\overline{\omega}_1 + \overline{\omega}_2) =$
$a_1^2 \omega_1 + a_2^2 \omega_2 - a_1 a_2 (\overline{\omega}_1 + \overline{\omega}_2) \cos(\omega_1 - \omega_2) t$.


Нам интересна ширина петли попятного движения.
Попятное движение ограничено точками стояния, то
есть моментами с нулевой угловой скоростью (моменты смены направления движения). То есть нам хочется знать, какой интервал времени разделяет нули выражения $\overline{\omega} = \frac{\overline{r} \times (\overline{v}_2 - \overline{v}_1)}{|\overline{r}|^2}$, совпадающие с нулями выражения $\overline{r} \times (\overline{v}_2 - \overline{v}_1) = a_1^2 \omega_1 + a_2^2 \omega_2 - (\overline{r}_1, \overline{r}_2)(\overline{\omega}_1 + \overline{\omega}_2) = a_1^2 \omega_1 + a_2^2 \omega_2 - a_1 a_2 (\sin \omega_1 t \sin \omega_2 t + \cos \omega_1 t \cos \omega_2 t)(\overline{\omega}_1 + \overline{\omega}_2) = a_1^2 \omega_1 + a_2^2 \omega_2 - a_1 a_2 (\overline{\omega}_1 + \overline{\omega}_2) \cos(\omega_1 - \omega_2) t$
То есть нужно решать уравнение:

$$
\cos(\omega_1 - \omega_2)t = \frac{a_1^2 \omega_1 + a_2^2 \omega_2}{a_1 a_2 (\omega_1 + \omega_2)}.
$$

Строго говоря, запись выше некорректна (кто определил векторное деление?), имеется в виду система из
трёх уравнений, записанных по координатам (отдельно для каждой). Вспомним также, что в естественной
системе отсчёта угловая скорость имеет единственную ненулевую координату в рамках данной задачи,
для остальных координат выражение тривиально. Получаем выражение для $t$:

$$
t = \pm \arccos \left( \frac{a_1^2 \omega_1 + a_2^2 \omega_2}{a_1 a_2 (\omega_1 + \omega_2)} \right) / (\omega_1 - \omega_2)
$$

То есть, время движения по петле (учитываем симметрию нулей, а также факты: выражение внутри арккосинуса имеет знак угловой скорости, угловая скорость планет сонаправлена):

$$
t_{петли} = 2 \arccos \left( \frac{a_1^2 \omega_1 + a_2^2 \omega_2}{a_1 a_2 (\omega_1 + \omega_2)} \right) / (\omega_1 - \omega_2)
$$

Полученная формула хорошо воспроизводит известные наблюдательные данные, так для наблюдений с
Земли график зависимости и экспериментальные
точки представлены на рис. 2.

![](opop_3.png)

*Рис. 2: Зависимость периода попятного движения
планет Солнечной системы при наблюдении с Земли.
Точки — реальные значения (для Меркурия, Венеры,
Марса, Юпитера и Сатурна, в порядке удаления от
Солнца), кривая — теоретическая зависимость, результаты хорошо сходятся.*

Чтобы найти размер петли достаточно получить угол
между радиус-векторами $\overline{r}$ в моменты стояния (подставить выражение для $t$ в определение ветора $\overline{r}$). Выражение получится достаточно громоздкое, приводить его мы не будем.
Рассмотрим еще одну интересную характеристику взаимного движения планет: угловое ускорение вектора $\overline{r}$. Для этого требуется рассмотреть ускорения материальных точек (планет):

$$
\overline{w}_n = \overline{\omega}_n \times \omega_n \times \overline{r}_n = -|\overline{\omega}_n|^2 \overline{r}_n
$$

Удобно перейти во вращающуюся систему отсчета,
связанную с одной из точек, тогда нужно записть уравнение:

$$
\overline{w}_2 = \overline{w}_{2(1)} + \overline{\omega}_1 \times \overline{\omega}_1 \times \overline{r}_2 + 2 \overline{\omega}_1 \times \overline{v}_{2(1)}.
$$

Здесь 
$\overline{w}_{2(1)}$ — ускорение второй планеты во вращающейся системе отсчета первая планета — Солнце, аналогично определяется $\overline{v}_{2(1)}$. Последнее слагаемое —
ускорение Кориолиса. Из последнего выражения получаем $\overline{w}_{2(1)}$, тогда легко можно выразить и угловое
ускорение:

$$
\overline{w}_{2(1)} = \overline{\varepsilon} \times \overline{r}
$$

Тогда справедливо:

$$
\overline{\varepsilon} = \frac{\left((|\overline{\omega}_1|^2 - |\overline{\omega}_2|^2\right) \overline{r}_2 - 2(\overline{\omega}_1, \omega) \overline{r}) \times \overline{r}}{\left|\overline{r}\right|^2} = \frac{\left(|\overline{\omega}_1|^2 - |\overline{\omega}_2|^2\right) (\overline{r}_1 \times \overline{r}_2)}{\left|\overline{r}\right|^2}.
$$

В таком случае зависимость модуля углового ускорения $\varepsilon$ от времени представляется довольно красиво:

$$
\frac{a_1 a_2 (\omega_1^2 - \omega_2^2) (\sin \omega_1 t \cos \omega_2 t - \sin \omega_2 t \cos \omega_3 t)}{a_1^2 + a_2^2 - 2 a_1 a_2 (\sin \omega_1 t \sin \omega_2 t + \cos \omega_1 t \cos \omega_2 t)}.
$$

Полученные в работе результаты можно использовать
при работе с задачами по механике (кинематика точки, сложное движение точки, неинерциальные системы отсчета). За ценные консультации авторы благодарят Суглобова Святослава.