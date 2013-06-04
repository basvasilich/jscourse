Объекты
=======

Все — объекты
-------------

В `JavaScript` все (почти) является объектами.

> Objects in JavaScript are mutable keyed collections.

  * Объект — это изменяемая коллекция свойств.
  * Свойство — пара «ключ — значение».
  * Ключ — любая строка.
  * Значение — что угодно.

---

Свойства
--------

(картинка)

---

Свойства. Доступ
----------------

{: .language-javascript }
    //  Получение значения свойства.
    var id = obj.id;

    //  Альтернативный синтаксис.
    var isFoo = obj['is-foo'];

---

Свойства. Изменение
-------------------

{: .language-javascript }
    //  Изменение значения свойства.
    obj.id = 'foo-42';
    obj['is-foo'] = true;

    //  Значением может быть что угодно,
    //  в том числе и `undefined`.
    obj.foo = undefined;

---

Свойства. Удаление
------------------

{: .language-javascript }
    //  Удаление свойства.
    delete obj.id;
    delete obj['is-foo'];

---

Свойства. Итерация
------------------

{: .language-javascript }
    //  Итерация по всем свойствам объекта.
    for (var key in obj) {
        var value = obj[key];
        ...
    }

---

Не все — объекты
----------------

Примитивные типы — `String`, `Number`, `Boolean` ведут себя как объекты,
но являются неизменяемыми.

    var foo = 42;
    foo.bar = 'Hello';

    foo.bar // undefined

---

Не все — объекты
----------------

`null` и `undefined` не являются объектами.

{: .language-javascript }
    var foo = null.foo; //  Ошибка!
    var bar = undefined.bar;

    //  Но. При этом:
    (typeof null === 'object') // true

---

Функции — тоже объекты
----------------------

{: .language-javascript }
    var f = function() {};

    f.foo = 42;
    var foo = f.foo // 42

---

Свойства и методы
-----------------

Методы — это свойства, значениями которых являются функции:

{: .language-javascript }
    obj.doSomething = function() {
        ...
    };

    obj.doSomething();

---

Object literal
--------------

Простое создание объектов:

{: .language-javascript }
    var obj = {}; // Пустой объект.
    obj = {
        foo: 42,
        doSomething: function() {
            ...
        }
    };

---

Доступ из методов к объекту
---------------------------

{: .language-javascript }
    obj = {
        id: 42,
        getId: function() {
            return this.id;
        }
    };
    obj.getId(); // 42

---

`this`
------

Внутри метода `this` указывает на объект,
метод которого вызван. Это позволяет получить
доступ к другим свойствам и методом этого объекта.

{: .language-javascript }
    obj.getId = function() {
        return this.id;
    }

---

`this`
------

`this` указывает на объект только тогда,
когда соответствующая функция вызывается как метод объекта:

{: .language-javascript }
    var getId = obj.getId;

    obj.getId(); // 42
    getId(); // ???

---

Дальше
------

  * Prototype.

  * `hasOwnProperty()`.

  * Создание объектов. Object literal, конструктор, `Object.create`.

  * Наследование.

  * Полиморфизм.

  * Инкапсуляция. Приватность.

  * `instanceof`.

