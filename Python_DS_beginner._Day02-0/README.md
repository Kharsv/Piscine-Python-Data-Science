# DAY 02 – И волки сыты
## Синтаксис Python
В рамках этого дня вы начнете знакомиться с анализом табличных данных и классическими методами машинного обучения.

## Оглавление

1. [Глава I](#глава-i) \
    1.1. [Преамбула](#преамбула)
2. [Глава II](#глава-ii) \
    2.1. [Общая инструкция](#общая-инструкция)
3. [Глава III](#глава-iii) \
    3.1. [Цели](#цели)
4. [Глава IV](#глава-iv) \
    4.1. [Задание](#задание)
5. [Глава V](#глава-v) \
    5.1. [Сдача работы и проверка](#сдача-работы-и-проверка)

## Глава I
### Преамбула

В анализе данных очень важны навыки работы с табличными данными и умение грамотно визуализировать эти данные, то есть строить информативные графики, позволяющие понять какие-то зависимости в данных или их статистические характеристики. Табличные данные - это те, которые можно хранить в таблице в виде: одна строка - один объект. Для работы с табличными данными в питоне есть популярная библиотека pandas. Помимо множества операций с самими данными, эта библиотека умеет работать со многими форматами хранения таблиц, такими как csv или excel. Визуализировать данные нам помогут библиотеки matplotlib (можно использовать как отдельно, так и прямо из объектов pandas) и seaborn.

В этом уроке вы познакомитесь с некоторыми стандартными преобразованиями данных, которые приходится совершать над большинством наборов данных, а также научитесь работать с файлами, в которых хранятся данные - считывать и записывать их. Кроме того, вы познакомитесь с методами графического анализа данных, который исползуется для первичной аналитики данных и позволяет улучшить качество данных для обучения моделей. Также вы решите свою первую задачу машинного обучения.



## Глава II
### Общая инструкция

Методология Школы 21 может быть не похожа на тот образовательный опыт, который с вами случался ранее. Ее отличает высокий уровень автономии: у вас есть задача, вы должны ее выполнить. По большей части вам нужно будет самим добывать знания для ее решения. Второй важный момент – это peer-to-peer обучение. В образовательном процессе нет преподавателей и экспертов, перед которыми вы защищаете свой результат. Вы это делаете перед таким же учащимися, как и вы сами. У них есть чек-лист, который поможет им выполнить приемку вашей работы качественно.

Роль Школы 21 заключается в том, чтобы обеспечить через последовательность заданий и оптимальный уровень поддержки такую траекторию обучения, при которой вы освоите не только hard skills, но и научитесь самообучаться.

* Не доверяйте слухам и предположениям о том, как должно быть оформлено ваше решение. Этот документ является единственным источником, к которому стоит обращаться по большинству вопросов.
* Ваше решение будет оцениваться другими учащимися бассейна.
* Подлежат оцениванию только те файлы, которые вы выложили в GIT.
* В вашей папке не должно быть лишних файлов – только те, что были указаны в задании.
* Есть вопрос? Спросите коллегу справа. Не помогло? Спросите коллегу слева.
* Не забывайте, что у вас есть доступ к интернету и поисковым системам.
* Обсуждение заданий можно вести и в Slack бассейна.
* Будьте внимательные к примерам, указанным в этом документе – они могут иметь важные детали, которые не были оговорены другим способом.
* И да пребудет с вами Сила!



## Глава III
### Цели

Наша цель - научиться работать с библиотеками pandas, matplotlib и seaborn, а именно: считывать/записывать данные, преобразовывать считанные данные, строить информативные графики и делать выводы, которые помогут в дальнейшем улучшить качество решения задач машинного обучения. Кроме того, после прохождения этого урока вы должны будете понимать, как ставятся задачи машинного обучения и какие метрики используются в качестве критериев качества решения.


## Глава IV
### Задание

Сегодня вы будете писать небольшие скрипты на Python. Вся работа у нас идет в Jupyter Notebooks / Google Colab. Ноутбук этого дня вы сможете найти здесь: `src/d02_task.ipynb`.


Что нужно сделать:
1. Написать функции time_change(df) и log_reg(y, X). Первая должна добавлять в датафрейм df столбец Order_time_sec_delta по описанию из блокнота, вторая - реализовывать агоритм логистической регрессии.
2. Написать код, который проведет преобразование времени из датафрейма через синус и косинус, после чего построить классификатор на новых признаках. Сравнить результаты.


## Глава V
### Сдача работы и проверка

1. Вам нужно загрузить в GIT в папку `src` свой Jupyter Notebook.
    1. Он должен содержать в себе весь требуемый код.
    2. Он должен называться `d02_desc.ipynb`.

