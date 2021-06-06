## Курсовой проект по дисциплине "Проектирование информационных систем"

## Иванов Артём Эдуардович, ИДБ-17-06

### 1. Определение требований к модели [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

**Тема ВКР:** исследование применения искусственных нейронных сетей в поисковых системах

**Объект исследований:** искусственные нейронные сети

**Предмет исследований:** применение искусственных нейронных сетей в поисковых системах

**Процессы верхнего уровня:** [✋](https://github.com/stankin/design-part-2/wiki/sem1)
* **А1 ** Управлять преобразованиями.
* **А2 ** Подготовить преобразования.
* **А3 ** Настроить преобразования.
* **А4 ** Оценить качество преобразований.
* **А5 ** Проанализировать проблемы.

**Точка зрения:** Заказчик приложения.

**Цель моделирования:** Определение автоматизируемых функций.

### 2. Функциональное моделирование процессов (IDEF0) [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

* A-0 (контекстная диаграмма)

![A-0](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%201.png)

* A0 (диаграмма верхнего уровня)

![A0](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%202.png)

* A2 (декомпозиция процесса/процессов внутренней среды)

![A2](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%203.png)

* A3 (декомпозиция процесса/процессов внутренней среды)

![A3](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%204.png)

* A4 (декомпозиция процесса/процессов внутренней среды)

![A4](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%205.png)





### 3. Функциональное моделирование программных и информационных средств (DFD) [✋](https://github.com/stankin/design-part-2/wiki/LR-2)

**Конфигурация технических средств:** Рабочие станции (ПК).

**Конфигурация программных средств:** Многоуровневые.

**Допустимые виды хранилищ и их размещение:** Запоминающее устройство ПК.

* A32 Автоматизация процесса А32

![A32](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%206.png)

* A33 Автоматизация процесса А33

![A33](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/model%207.png)

### 4. Описание выбранного процесса [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате прецедента (Use Case) [✋](https://github.com/stankin/design-part-2/wiki/LR-4)

Диаграмма UML Use Case
![p4](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/uml%201.png)

**4.1 Идентификатор прецедента:** А33

**4.2 Название прецедента:** Преобразование речи в запрос

**4.3 Контекст:** А3

**4.4 Участники (actors) и цели (goals):**

| Участник  | Категория  | Цель (goal) |
|---|---|---|
|Web браузер |Инструмент| Обеспечить работоспособность системы |
| Специалист | Внешний  | Ввести голосовой запрос |
| Голосовой помощник | Инструмент| Преобразовать речь в голос, перейти на сайт или поисковую систему |


**4.5 Предусловия (pre-conditions):**

* Web браузер

* Пользователь

* Голосовой помощник


**4.6 Постусловия (post-conditions):**

* Открытый сайт или в поисковая система

**4.7 Основной поток выполнения (main flow)**:

| Участник  | Действие (activity)  | Ожидаемый результат |
|---|---|---|
|Пользователь|Запускает программу|Открытие голосового помощника|
|Пользователь|Озвучивает запрос|Полученный запрос|
|Голосовой помощник|Выполняет запрос|Переход на сайт или в поисковую систему|


**4.8 Исключения (exceptions):**

| Условие (риск) | Последствия | Реакция |
|---|---|---|
| Голосовой помощник не правильно распознает слова	 | Пользователь не может перейти на сайт или в поисковую систему  | Обратиться к разработчкику |

**4.9 Альтернативы (alternates):**

Не предусмотрено.

**4.10 Временные параметры:**

* **Триггер (событие, стартующее прецедент):** Необходимость перейти на сайт или в поисковую систему.
* **Номинальная частота повторения прецедента:** 10-12 раз в день.
* **Продолжительность прецедента:** 3 минуты.

### 5. Описание структуры объекта [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате ERD (Class) [✋](https://github.com/stankin/design-part-2/wiki/LR-5)

* **Описываемый объект:** голосовой помощник.

* **Диаграмма UML Class:**

![p5](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/uml%202.png)

### 6. Описание алгоритма [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Sequence) [✋](https://github.com/stankin/design-part-2/wiki/LR-6)

* **Описываемые процессы и потоки данных:** А33

* **Диаграмма UML Sequence:**

![p6](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/uml%203.png)

### 7. Описание состава [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Component) [✋](https://github.com/stankin/design-part-2/wiki/LR-7)

* **Описываемый объект:** Струкрутра программных средств системы

* **Диаграмма UML Component:**

![p7](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/uml%204.png)

### 8. Демонстрация реализации (личная страница)

https://artyom-ivanov627.github.io/Ivanov-page/#!/topics
### 9. Подготовка к интерпретации построенных моделей

**9.1 Используемые паттерны проектирования и разработки [✋](https://github.com/stankin/design-part-2/wiki/sem2):**

**9.1.1 Процессная модель для сравнения:** Задача: Необходимость в автоматизированной системе перехода на сайт или в поисковую систему пользователям Способ решения: при помощи методологии PDCA:
1. Этап Plan (планирование)
Выявление проблемы:
* Процесс ручного ввода пользователями запросов является затратным по времени.
* Цель: автоматизация процесса ввода запросов с помощью голосового помощника
* Требования: повысить производительность и эффективность без увеличения трудозатрат
* Ожидаемый результат: разработано автоматизированное средство преобразования голоса в запрос
* Ресурсы, необходимые для достижения ожидаемого результата: разработанные требования для состава запроса, наличие ПК
* Процессы (запланированные действия):
* Разработать голосового помощника
* Создать необходимые процедуры, которые будут преобразовывать речь в запросы
* Разработать нейросеть, определяющую, что нужно открыть - сайт или поисковую систему
2. Этап Do (Выполнение) Разработчики-аналитики выполняют поставленные задачи
3. Этап Check (Проверка): По итогу разработки произвести апробацию, и в случае успеха, произвести внедрение
4. Act (Улучшение): При успешной работе системы она внедряется в компанию с дальнейшей возможностью доработки.
* Используемые в разработке паттерны и фреймворки:
* Паттерн Посредник - это поведенческий паттерн проектирования, который позволяет уменьшить связанность множества классов между собой, благодаря перемещению этих связей в один класс-посредник



**9.2 Используемые паттерны выявления проблем [✋](https://github.com/stankin/design-part-2/wiki/sem3):**
* Муда: трата времени на ручной ввод запросов
* Мура: неправильно сформированный запрос
* Мури: единовременное использование функций голосового помощника многими пользователями

**9.3 Возможные антипаттерны [✋](https://github.com/stankin/design-part-2/wiki/sem4):**

| Категория  | Антипаттерн (риск) | Действие по избежанию |
|---|---|---|
| Разработка | Spaghetti code. Спагетти-код —Ход выполнения программы похож на спагетти, т.е извилистый и очень запутанный код. | изучение правил написания кода, переписывание кода |
| Архитектура | Большой комок грязи (Big ball of mud) | разработать "читаемую" архитектуру системы |
| Организация | Аналитический паралич. Неоправданно большие затраты на анализ и проектирование. | проанализировать приоритеты |
| Среда | Чрезмерное усложнение | стараться упростить систему |

### 10. Интерпретация построенных моделей [✋](https://github.com/stankin/design-part-2/wiki/cp-guide)

**10.1 Определение числовых показателей для поставленной цели моделирования:**

Выявление процессов, нуждающихся в повышении качества.

![1](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/Proc.png)

Способ получения: извлечение из диаграмм IDEF0 и DFD.

**10.2 Определение числовых показателей для цели потенциального проекта автоматизации: [✋](https://github.com/stankin/design-part-2/wiki/interpret_process)**

Числовыми показателями являются время и трудозатраты.

**10.3 Расчет потенциального эффекта от автоматизации:**

Староста группы в любом учебном заведении в случае ожидания сообщения от преподавателя, в среднем, тратит 3 минут на проверку почты и пересылку необходимых сообщений. Таких проверок в день (8 часов) насчитывается около 5 штук, каждый раз при этом ему нужно зайти в почту. Этот процесс отнимает драгоценное время, в связи с этим, было принято разработать интеллектуальную систему обработки сообщений в приложении Telegram.

После внедрения системы старосте не придется отправлять сообщения, так как это сделает система за него. Итого экономия: 0.25Ч  в день, в месяц (0.25) * 30 = 7.5 часов.
При наличии 1 старосты в каждой из 200 групп и при их активности в 8 часов в день, ежемесячная экономия времени составит 7.5 * 200 ~ 1500 чел/мес.

**10.4 Определение числовых показателей и расчет затрат на реализацию проекта автоматизации:**

Расчет сложности разработки методом FPA IFPUG:

![3](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/FPA%20IFPUG.jpg)

Расчет трудозатрат на разработку «с нуля» методом COCOMO II:

![4](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/COCOMO%20II.jpg)

**10.5 План-факт сравнение для затрат на реализацию: [💻](https://docs.google.com/spreadsheets/d/11KghKnPycU-EtbHJ3dKK5FQjPntsd9ZQ9LVSzg9Ou5E/edit#gid=1983994942)**

![4](https://github.com/Artyom-Ivanov627/kurs/blob/main/img/Plan.jpg)

**Из расчета:**

SLOC = 7056 строк кода

PM (Трудозатраты) = 18.5 человеко-месяцы

TDEV (Полный срок разработки, месяцы) = 8.4 месяцев

**Исходя из значений по факту:**

SLOC = 5000 строк кода

PM (Трудозатраты) = 800 человеко-часы

TDEV (Полный срок разработки) = 8 месяцев

Готовность = 80%

**ВЫВОДЫ**

Исходя из результатов таблицы п.10.5 можно сделать вывод, что за счет использования готовых функций и библиотек удалось сократить строки кода (языки программирования Python) в 3.1 раза. Также, за счет сокращения тестирования, объема документации, и использования CASE, удалось сократить срок разработки с 8.4 месяцев до 8. Срок окупаемости разработки сократился в 3.1 раза. На данный момент работа выполнена на 100%.
