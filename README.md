# Anomaly-detection-
Детекция аномалий в данных. Статистический подход
<p>Цель работы – выявить в наборе данных аномалии разными методами детекции. 
 <p>Набор данных – статистика заражения коронавируса в некоторых европейских странах. 
<h3>Этапы достижения цели:</h3>
<ul>
<li>•	Загрузка датафрейма; 
<li>•	Расчёт среднего, среднеквадратичного отклонения;
<li>•	Расчет дисперсии и смещения. 
<li>•	Построение нормального распределения;
<li>•	Визуализация данных;
<li>•	Заключение вывода- обнаружение аномалий
</ul>
  <h3>Ход работы </h3>
Моей первоначальной целью было найти данные по статистике Covid-19. (data.csv)
<p>Была взята статистика нескольких европейских стран, количество случаев заражения за каждый день 
<p>В статистике, если распределение данных приблизительно нормальное, то около 68% значений данных находятся в пределах одного стандартного отклонения от среднего, а около 95% находятся в пределах двух стандартных отклонений, и около 99,7%лежат в пределах трех стандартных отклонений. Итак, 95% из нас используют около двух стандартных отклонений в качестве порога. Все, что выходит за порог, считается аномальной точкой. 
<p>
 <p>
<p>Также, был рассмотрен алгоритм Isolation Forest. Изолирующий лес — это алгоритм машинного обучения для обнаружения аномалий. Это алгоритм обучения без учителя, который выявляет аномалии, изолируя выбросы в данных. Изолирующий лес основан на алгоритме дерева решений. Он изолирует выбросы, случайным образом выбирая функцию из заданного набора функций, а затем случайным образом выбирая значение разделения между максимальным и минимальным значениями этой функции. Это случайное разбиение объектов создаст более короткие пути в деревьях для аномальных точек данных, тем самым отличая их от остальных данных. Алгоритм Isolation Forest основан на том принципе, что аномалии — это немногочисленные и разные наблюдения, что должно облегчить их идентификацию. Изолирующий лес использует ансамбль деревьев изоляции для заданных точек данных, чтобы изолировать аномалии. Isolation Forest рекурсивно создает разделы в наборе данных, случайным образом выбирая объект, а затем случайным образом выбирая значение разделения для объекта. Предположительно, для аномалий требуется изолировать меньшее количество случайных разделов по сравнению с «нормальными» точками в наборе данных, поэтому аномалии будут точками, которые имеют меньшую длину пути в дереве, причем длина пути представляет собой количество ребер, пройденных от корневого узла. Используя Isolation Forest, мы можем не только быстрее обнаруживать аномалии, но и требовать меньше памяти по сравнению с другими алгоритмами. Этот алгоритм очень хорошо работает и с небольшим набором данных.  В добавленной колонке anomaly -1 показывает наличие аномалии, а 1 означает ее отсутствие

<p>Затем, была построена функция распределения для каждой из стран. Также , были выведены графики функции распределения по отдельности для каждой из рассматриваемых стран. 
<h3> Вывод </h3>
В ходе работы были проанализированы существующие библиотеки для языка программирования Python, которые упрощают работу с алгоритмами для поиска аномалий в данных. Исследовав набор данных были построены функции распределения, использовались 2 метода детекции аномалий: с помощью среднеквадратичного отклонения и Isolation Forest. Были изучены виды аномалий , а также различные методы детекции.
