План
============

Предлагаю всем свой план накидать, потом сведем и более подробно распишем.
**Я в процессе пока что...**

Уровень 0 - @basvasilich
 Разбить на лекции
---------------
Это совсем база, после нее уже можно писать совсем простые программы.
Хотя бы проговорить синтаксис операторов нужно. Разные нюансы всегда есть.

  * Переменные, примитивные типы данных, операторы (присваивание, арифметические, логические, битовые, тернарный, ...).
  * Синтаксис базовых control flow операторов (`if`, `for`, `while`, `switch`).
  * Функции. Базовый синтаксис, аргументы, `return`.

Уровень 1 - @shirokoff
 Разбить на лекции
---------------
Это чуть более продвинутый уровень.
Опять-таки все самое необходимое.
http://learn.javascript.ru/#book-toc-137

  * Все — объекты.
  * Методы и свойства в объектах.
  * Object literal. Создание пустого объекта, добавление и изменение его свойств. Удаление свойств. Чтение свойств. Тоже для array literal.
  * Приведение типов.
  * Рекурсия, стек.
  * Scope. Локальные и глобальные переменные.
  * Передача параметров в функции (по ссылке и по значению).
  * Сравнение объектов (по ссылке и по значению).
  * arguments
  * try/catch

Уровень 2 
---------------
Тут всякие закидоны странные, про которые нужно таки знать.
Ну и просто разные продвинутые вещи.
To be continued...

  * hoisting
  * Определение типов (`instanceof`, `typeof`, `Array.isArray`)
  * Различные типа eval'ов.
  * Однотредность. "Асинхронность" (а правильнее неблокирующие операции).


Еще есть тематические блоки.

Все про регэкспы — @edoroshenko
--------------------------
Ну. Понятно.
  * Ключи:
    * m 
    * g
    * i
  * Квантификаторы
  * Жадность квантификаторов
  * Символьные группы

ООП — @nop
-------

  * Собссно теория. Объекты, наследование, полиморфизм, инкпапсуляция, ...
  * Объекты на практике.
  * Конструкторы.
  * Создание через `new`.
  * Методы. Статические методы.
  * `this`.
  * Наследование.
  * Полиморфизм aka duck typing.
  * Динамическое изменение объекта (свойств и методов) и прототипа.

Все про функции — @shirokoff
--------------------------

  * Все способы определения функций.
  * Вложенные функции.
  * First class objects.
  * Замыкания.
  * Контекст. Изменение контекста.
  * Все способы вызова функций.

DOM — @doochik
-------
Ну и вообще все, что происходит в браузере. События. Аякс...

Паттерны — 
---------------
Тут вот что. Я не верю в классические паттерны. Типа синглтона и т.д. Как по мне это все бесполезно. Т.е. это способ назвать что-то, что ты уже сделал, "правильным" словом. Решать задачу знание паттернов имхо не помогает.
Тут я говорю про какие-то реальные и полезные практики, которые мы используем. В широком смысле...

  * События вообще. DOM и кастомные.
  * Event delegation.
  * Декларативность. Например, декларативное описание  в DOM'е реакции на действия пользователя (data-атрибуты).
  * Агрегирование вместо наследования
  * MVC (MVW).
  * Слабосвязность кода.
  * Lazy-действия.
  * Асинхронность. Про это отдельно еще.
  * Синглтон
  * Чейнинг

Асинхронность
-----------------------

  * callback'и.
  * callback hell.
  * promise и future.
  * Последовательное и параллельное выполнение.


Node.js
-----------
  * ???
  * ???

HTML5 — @basvasilich
-----------
  * Обзор ECMAScript5
    * https://developer.mozilla.org/en-US/docs/tag/ECMAScript5 
    * https://developer.mozilla.org/en-US/docs/JavaScript/New_in_JavaScript/1.8.5

  * Обзор полезных JS API.
    * localStorage
      * https://developer.mozilla.org/en-US/docs/Web/Guide/DOM/Storage?redirectlocale=en-US&redirectslug=DOM%2FStorage 
    * HistoryAPI
      * http://diveintohtml5.info/history.html
      * https://developer.mozilla.org/en-US/docs/Web/API/window.history
    * onhashchange
      * http://msdn.microsoft.com/en-us/library/cc288209(VS.85).aspx  
      * https://developer.mozilla.org/en-US/docs/Web/API/window.onhashchange?redirectlocale=en-US&redirectslug=DOM%2Fwindow.onhashchange
    * FormData
    * FileAPI
      * http://docs.webplatform.org/wiki/apis/file
      * https://developer.mozilla.org/en-US/docs/Using_files_from_web_applications
    * JSON parsing
       * https://developer.mozilla.org/en-US/docs/Using_native_JSON 
    * Web Sockets
      * https://developer.mozilla.org/en-US/docs/WebSockets/Writing_WebSocket_client_applications
      * http://www.websocket.org/aboutwebsocket.html
    * Drag ahd Drop
      * https://developer.mozilla.org/en-US/docs/DragDrop/Drag_and_Drop 

Styleguide
---------------
У меня есть свой стайлгайд, могу описать его совсем подробно и объяснить, почему именно так.

Performance
------------------
Тут есть производительность собссно js и есть производительность работы с DOM.

  * Разные странные и неочевидные примеры бенчмарков js-конструкций.
  * jsperf.com.
  * Работа с DOM.
  * Rendering, repaint, reflow.
