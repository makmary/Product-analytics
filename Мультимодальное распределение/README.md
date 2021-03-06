# Product Analytics

Добрый день, коллеги,
многие из Вас просили дать ссылки на дополнительные материалы по теме выявления мультимодальности в распределении, которая выходит за рамки нашего курса, и частично вытекающей из неё задачи по выявлению нескольких распределений в смеси; часть студентов уже получила ответ в ЛС, поскольку задача заинтересовала многих, размещаем ссылки на материалы в отдельном топике:

Вначале ещё раз напомним основные алгоритмы:
1) определения мультимодальности распределения;
примеры: классические методы определения экстремумов, метод адаптивного сглаживания, метод ядерной оценки плотности (KDE-метод), тесты на унимодальность;
2) выявления масок эмпирических распределений в выборке, представляющей из себя смесь распределений.
Примеры: KMM-алгоритм (Kernel Mean Matching), EM-алгоритм (Expectation-Maximization), и другие алгоритмы.
Существуют методы и библиотеки визуализации смеси распределений.
Методы могут быть основаны как на классических стат.тестах, так и на методах кластеризации и снижения размерности.

Дополнительные материалы по KDE:
https://medium.com/intel-student-ambassadors/kernel-density-estimation-with-python-using-sklearn-c50b3c337871
https://jakevdp.github.io/blog/2013/12/01/kernel-density-estimation/
https://www.statsmodels.org/stable/examples/notebooks/generated/kernel_density.html
https://scikit-learn.org/stable/auto_examples/neighbors/plot_kde_1d.html
Дополнительные материалы по unidip:
https://www.kdd.org/kdd2016/subtopic/view/skinny-dip-clustering-in-a-sea-of-noise
https://pypi.org/project/unidip/
Дополнительные материалы по GMM, хорошие и легкие для понимания и чтения, с большим кол-вом практических примеров:
https://towardsdatascience.com/gaussian-mixture-modelling-gmm-833c88587c7f
https://medium.com/swlh/ml-gmm-em-algorithm-647cf373cd5a
Дополнительные материалы по EM-алгоритму для смешанных моделей:
https://ranalytics.github.io/data-mining/104-Other-Clustering-Methods.html#sec_10_4_3
Чтобы прояснить вкратце суть методов: GMM и EM решают применительно к задаче выявления смеси нескольких распределений в исходном распределении задачу выявления, если применять моделирование, то можно пробовать рассматривать различные алгоритмы кластеризации, и определять центры в получившихся кластерах как моды (как центры ограниченной изолиниями области с наибольшей плотностью распределений внутри; расстояние между изолиниями - это, условно, границы каждого столбика гистограммы, которые определяются кол-вом разрядов bins; такое изображение можно рассматривать как развертку "вид сверху"):

