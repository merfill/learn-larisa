# Репозиторий для обучения Ларисы

## Предварительные сведения

* Все реализуем в python3
* Пока все программируем в ноутбуках, поэтому надо уметь запускать код в Jupyter Notebook
* Используем pandas и numpy для загрузки данных из csv и предварительной обработки
* Используем sklearn и scipy для машинного обучения
* Используем matplotlib для отображения данных в ноутбуке

## Первый проект

В качестве данных (dataset) для первого проекта будет использовать Iris data -- базу ирисок (цветов). Почитать про нее можно, например, здесь: 
https://en.wikipedia.org/wiki/Iris_flower_data_set. Это база измерений цветов ириса трех сортов:
* setosa
* versicolor
* virginica

Для каждого сорта заданы четыре значения измерения: длина и ширина чашелистника (sepal) и лепестка (petal), в Википедии нарисовано,
что это такое. По этим четырем значениям можно попытаться построить модель, которая предстказывает сорт цветка по данным значениям.
Такая задача (предсказание класса (сорта) по значениям) называется задачей классификации. Наша конечная цель состоит в том, чтобы
научиться строить такие модели на основе разных алгоритмов. Но, сначала надо научиться загрузать данные в память и проводить первичный
анализ.

### Загрузка и обработка данных

Чтобы загрузить данные, будем использовать библиотеку sklearn:
```python
from sklearn.datasets import load_iris
data = load_iris().data
```

Код загрузки и первичной обработки данных будет лежать в ноутбуке iris\_load.ipynb. Что надо сделать с данными:
* Загрузить на машину и после этого в память процесса
* Загруженные данные представлены как numpy array -- массив библиотеки numpy. В книжке, которую я тебе присылал, по работе с данными, есть
  целая глава про работу с numpy. Можно также почитать быстрое введение на https://docs.scipy.org/doc/numpy/user/quickstart.html или
  может найдешь другой текст на русском языке. Коротко говоря, numpy -- это библиотека для быстрой работы с таблицами данных, которые
  называются массивами -- arrays. С элементами массивов можно прозводить различные операции очень быстро, чем эта библиотека и занимается
* После освоения numpy идем дальше и работаем с pandas. Это тоже библиотека для работы с данными, но предоставляющая более широкие
  возможности. С колонками данных можно работать через символьные имена, а не числовые индексы, также есть еще несколько хороших методов,
  которых не имеется в numpy.

Курс по numpy: https://docs.scipy.org/doc/numpy/user/quickstart.html.
Хороший учебный курс по pandas: https://bitbucket.org/hrojas/learn-pandas. Будем по нему учиться.


### Отображение данных

Для отображения данных используем PCA -- метод снижения размерности. Для каждой строки -- описания конкретного цветка, имеется четыре значения.
Эти четыре значения можно представить как вектор, т.е. точку в четырехмерном пространстве значений (если не понятно, спрашивай). Изобразить
точки в четырехмерном пространстве невозможно, поэтому обычно используется метод снижения размерности. Мы попробуем снизить размерность до
трех и двух измерений и затем показать, как это будет выглядеть для разных классов. Для снижения размерности исопльзуются два основных
метода: PCA и t-SNE. Попробуем оба. Иначе говоря, необходимо научится предобрабатывать и показывать данные. Еще попробуем различные методы
нормализации данных.

### Классификация линейной регрессией


### Классификация логистической регрессией


### Кластеризация методом K-средних


### Классификация на основе лесов деревьев






