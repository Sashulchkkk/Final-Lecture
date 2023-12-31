# Final-Lecture

# План автоматизации

#### Объект тестирования

Веб-сайт Нетологии:
*  тестирование возможности записаться на обучение профессии «Тестировщик ПО»

#### Валидные данные студента
* Имя: Александра
* Номер телефона: +79281294040
* Email: SashaLavrova@Email.ru

## Перечень автоматизируемых сценариев (навигации)

1. Каталог курсов → Программирование
    * Нажать сверху в меню "Каталог курсов";
    * В выпадающем меню нажать "Программирование";
    * Выбрать из списка "Тестировщик ПО";
    * Опционально: Нажать на кнопку "Записаться" (тогда ожидается, что страница прокрутится до раздела "Выберите свой вариант обучения");
    * В разделе "Выберите свой вариант обучения" у варианта "Базовый" нажать на кнопку "Выбрать";

2. Каталог курсов → Поиск → Клик на подсказку
    * Нажать сверху в меню "Каталог курсов";
    * В выпадающем меню в поле "Какой курс вам нужен?" набрать "тест";
    * Ожидается, что вылезет подсказка "Тестировщик ПО"
    * Выбрать из списка "Тестировщик ПО";
    * Опционально: Нажать на кнопку "Записаться" (тогда ожидается, что страница прокрутится до раздела "Выберите свой вариант обучения");
    * В разделе "Выберите свой вариант обучения" у варианта "Базовый" нажать на кнопку "Выбрать";

3. Каталог курсов → Поиск → Все курсы
    * Нажать сверху в меню "Каталог курсов";
    * В выпадающем меню в поле "Какой курс вам нужен?" набрать "тест";
    * Ожидается, что вылезут подсказки;
    * Нажать "Все курсы по запросу «тест»";
    * Выбрать из списка "Тестировщик ПО";
    * Опционально: Нажать на кнопку "Записаться" (тогда ожидается, что страница прокрутится до раздела "Выберите свой вариант обучения");
    * В разделе "Выберите свой вариант обучения" у варианта "Базовый" нажать на кнопку "Выбрать";

4. Через раздел Направления обучения
    * В разделе "Направления обучения" нажать "Программирование"
    * Выбрать из списка "Тестировщик ПО";
    * Опционально: Нажать на кнопку "Записаться" (тогда ожидается, что страница прокрутится до раздела "Выберите свой вариант обучения");
    * В разделе "Выберите свой вариант обучения" у варианта "Базовый" нажать на кнопку "Выбрать";

5. Через подвал
    * В подвале страницы нажать "Программирование"
    * Выбрать из списка "Тестировщик ПО";
    * Опционально: Нажать на кнопку "Записаться" (тогда ожидается, что страница прокрутится до раздела "Выберите свой вариант обучения");
    * В разделе "Выберите свой вариант обучения" у варианта "Базовый" нажать на кнопку "Выбрать";


## Перечень автоматизируемых сценариев (заполнения и отправки формы)

1. Нормальный сценарий
    * В открывшуюся форму ввести Данные студента;
    * Нажать "Перейти к оплате";
    * Ожидается, что откроется форма оплаты И в базу данных будут занесены Данные студента.

2. С незаполненными полями
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что не все поля заполнены.

3. С некорректным именем
    * В открывшуюся форму ввести Данные студента, притом в поле Имя ввести "$$$";
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что поле Имя заполнено неправильно.

4. С некорректным телефоном
    * В открывшуюся форму ввести Данные студента, притом в поле Телефон ввести "$$$";
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что поле Телефон заполнено неправильно.

5. С некорректным email адресом
    * В открывшуюся форму ввести Данные студента, притом email ввести без символа ".";
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что email заполнен неправильно.

6. С незаполненным полем Имя
    * В открывшуюся форму ввести Данные студента, но не заполнять поле Имя;
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что не все поля заполнены.

7. С незаполненным полем Телефон
    * В открывшуюся форму ввести Данные студента, но не заполнять поле Телефон;
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что не все поля заполнены.

8. С незаполненным полем Электронная почта
    * В открывшуюся форму ввести Данные студента, но не заполнять поле Электронная почта;
    * Нажать "Перейти к оплате";
    * Ожидается, что появится подскаска говорящая что не все поля заполнены.


### Перечень используемых инструментов с обоснованием выбора
* Java 8 - наиболее распространенная версия в настоящее время
* Junit 5 - позволяет создавать автоматизированные тесты на java 
* Selenide - для автоматизации UI тестов на java c простым синтаксисом
* Faker - как генератор случайных имён
* lombok - упрощает написание программ на java
* Allure - генератор отчётов тестирования

### Перечень необходимых разрешений, данных и доступов
* Разрешение на тестирование и автоматизацию.
* Доступ к БД и API сайта.

### Перечень и описание возможных рисков при автоматизации
* У тестировщика нет достаточного опыта в работе с инструментарием 
* Нет документации к тестируемому приложению. О корректном поведении приходится строить догадки.
* UI: непрерывный процесс совершенствования браузеров 

### Перечень необходимых специалистов для автоматизации
* Тестировщик ПО.

### Интервальная оценка с учётом рисков (в часах)
* Без рисков: до 8 часов:
    * 1 час на исследование приложения;
    * 1 час на покурить, кофе и планирование =) ;
    * 2 часа на написание основы тестов и утилит;
    * 1 час на написание самих сценариев;
    * 2 часа на отладку сценариев;
    * 1 час на описание багов и отчёт.  
* С рисками: до 16 часов:
    * 8 часов без рисков + ещё 8 часов на:
        * случай если возникннут трудности при поиске локаторов элементов;
        * В ходе выполнения проекта изменится структура сайта;
