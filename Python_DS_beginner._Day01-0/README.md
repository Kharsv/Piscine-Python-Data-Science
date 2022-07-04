# DAY 01 – Трудно жить без даты
## Работа с датами в Python
В рамках этого дня вы лучше поймете структуру языка Python и научитесь работать с датами.

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

Крайне часто в практике работы с данными приходится обрабатывать месяцы, дни недели, часы, периоды и так далее - одним словом, то, что можно описать как дату и время. Эта сущность достаточно сложная, потому как не всегда однозначно можно определить операции над ними. 31 января плюс один месяц - это 31 февраля? Нет, ведь в феврале всего 28 дней. Или 29 - зависит от года. Сложности наподобие этой отнимают возможность хранить дату и время в обычных целочисленных переменных, поэтому в каждом языке программирования высокого уровня есть сущность, которая описывает все необходимые параметры даты и времени, учитывая все нюансы календаря и часовых поясов. Понимание того, как правильно вести работу с датами и временем, очень важно для любого разработчика, в том числе и того, кто занимается анализом данных, поэтому этот урок посвящен овладению этим навыком.

Однако просто уметь использовать класс datetime - мало. Любой код нужно структурировать так, чтобы его легко можно было потом понимать и переиспользовать, то есть его нужно грамотно декомпозировать. В этом помогают функции. В этом уроке вам предстоит не только познакомиться с сущностями для работы с датами и временем, но и структурировать свой код работы с этими сущностями так, чтобы его было удобно использовать в разработке.

<details><summary>Напомним расписание бассейна</summary>



**Day 00. В начале был 0**

Знакомство с базовыми сущностями Python: типы данных, операторы. Знакомство с интерпретируемым языком.

**Day 01. Трудно жить без даты           ←    Вы находитесь здесь**

Сущности Python для обработки даты и времени, декомпозиция кода на функции. Знакомство с pandas

**Day 02.И волки сыты**

Работа в датафреймами, построение графиков. Задача классификации и логистическая регрессия.

**Day 03. Ветер дует, потому что деревья качаются**

Деревья решений.

**Day 04. Школа 21**

Обучение без учителя. Кластеризация. Снижение размерности признакового пространства.

**Team 00. Шестой подвиг Геракла**

Групповой проект: очистка данных и построение регрессора.

**Day 06. Пива нет**

Обработка текстов. Векторизация текстов. Методы мешка слов, TF-IDF.

**Day 07. На что похожа ерунда?**

Семантический анализ текстов. Модель Word2vec, doc2vec. Использование градиентного бустинга для задачи классификации текстов.

**Day 08. Один в поле - (не) n-грамма**

Обработка текстов методом n-грамм. Тематическое моделирование.

**Day 09. Котопёс**

Искусственные нейросети. Переиспользование топологий. Сверточные нейросети. Классификация изображений.

**Day 10. Мне не нужны твои советы**

Рекомендателные системы. Кластерные рекомендации. Пользователь-ориентированные и контент-ориентированные рекомендации. Матричное разложение в рекомендательных системах.

**Team 01. Усы, лапы и хвост**

Групповой проект. Разработка системы классификации пользователей по фотографии.
</details>


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

Использование дат и времени встречается повсеместно в работе специалистов по Data Science. Наша цель - научиться свободно работать с сущностями модуля datetime, оформлять код в функции, а также использовать этот код применительно к датафреймам с данными.


## Глава IV
### Задание

Сегодня вы научитесь работать с датами и с теми сущностями, которыми дата и время представлены в питоне.


Напомним, что вы продолжаете работать в Jupyter Notebooks / Google Colab. Ноутбук этого дня бассейна вы сможете найти здесь: `src/d01_task.ipynb`.


Что нужно сделать:
1. Описать функции для определения даты рождения друга по их описаниям из блокнота:
  - month_of_birth
  - day_of_birth
  - get_month
  - get_day
2. Написать код, рассчитывающий количество рабочих часов с использованием методов модуля datetime.
  - Описать функции:
    - input_date
    - date_to_datetime
    - delta_time
    - day_of_the_week
    - calculating_hours
  - Описать тесты к этим функциям
3. Написать код, который изменяет исходный excel-файл с датами путем добавления колонок, которые перечислены в блокноте, и сохраняет его. 

## Глава V
### Сдача работы и проверка

1. Вам нужно загрузить в GIT в папку `src` свой Jupyter Notebook.
    1. Он должен содержать в себе весь требуемый код.
    2. Он должен называться `d01_desc.ipynb`.
