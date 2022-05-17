# Конспект "JavaScript для начинающих".

<ins>От автора:</ins> написала данный конспект для тех, кто начинает учить JavaScript. Буду дополнять/изменять конспект.

<ins>Цель написания конспекта</ins> - сбор информации по основным темам JavaScript, практика работы с разметкой Markdown.

<ins>Надеюсь, конспект пригодится мне или любому начинающему разработчику.</ins>

И так, поехали.

---

**Самое важное в JavaScript:**

+ Выражения
+ Функции
+ Объекты


Практически все сущность в js - это объекты;\
Объект - набор свой свойств **"<ins>имя</ins>: <ins>значение</ins>"**


Пример объекта:

```js
{
	visible: true, //имя: значение 
	colorDepth: 24,
	title: 'My Image',
	orientation: { //вложенный объект
		angle: 0,
		type: 'landscape'
	},
	pixelDepth: 24,
	width: 1440
}
```
<br>
Массив, функция - это объект;\
Число, строка - это объект (только ведут себя как объект, но они имеют примитивный тип значений);
<br>
<br>

```js
console.log('Hello! I am hungry!');
```

+ **console** - объект;
+ **log (dir, table и тд)** - метод (функция значение одного из свойств объекта);
+ **.** - точечная запись (получение доступа к свойствам объекта);
+ **()** - вызов метода;
+ **'Hello! I am hungry!'** - значение типа 'String'/аргумент.
<br>

**Любое выражение возвращает нам значение.**
<br>
<br>

## Выражения
<br>

**ВСЕГДА ВОЗВРАЩАЕТ ЗНАЧЕНИЕ**
<br>
Выражение | Описание      										 | Результат  		|
----------|------------------------------------| ---------------|
`'abc'`   | строка/String 										 |  `'abc'`	  		|
`10`   	  | число/number  										 |  `10`      		|
`5 + 2`   | выражение с оператором +					 |  `7`       		|
`с = 10`  | оператор присвоения = 						 |  `10`      		|
`'Good' + ' Evening'`| сумма строк   					 |`'Good Evening'`|

**и еще примеры:**
+  `a <= b || c !== d` - выражение с несколькими операторами - результат: `true/false`;
> 
+ `b++;` - вернет значение переменной и увеличит его на 1;
> 
+ `myFunction(c, d)` - внутри функции происходят побочные действия, помимо возврата значения - результат: результат функции;
<br>
<br>

### **Выражение присваивания:**

> **`а = 20;`** 
>+ **а** - <ins>название переменной</ins>,
>+ **20** - <ins>значение, которое присваивается переменной с именем **а**</ins>;
<br>
<br>

### **Выражения с побочными действиями:**

>+ `a = 5;`
>+ `b++;`
>+ `myFunction(c, d);`
<br>

**<ins>Не только возвращется значение, но и выполняет другие действия.</ins>**
<br>
<br>

## **Переменные**
<br>

> **ДАЮТ ВОЗМОЖНОСТЬ ПОВТОРОНОГО ДОСТУПА К ЗНАЧЕНИЯМ**
<br>

Коробка в которую можно что-то поместить, дать этой коробке имя и в дальнейшем обратиться к значению, распаковать, поменять содержимое, выполнить какое-то действие.
<br>
<br>

### **Имена переменных и стили написания**
>**НАЗВАНИЕ ПЕРЕМЕННЫХ ДОЛЖНЫ БЫТЬ ПОНЯТНЫ!**

Cтиль написания:

+ `PascalCase` - именование переменной начинается с заглавной буквы как и последующие слова (без пробелов). Используются для именования типов и классов в JS;

+ `SCREAMING_SNAKE_CASE` - все символы заглавные, вместо пробела используется _ . Применяется для именования переменной, значение которой известны до запуска приложения и не меняются (const);

+ `сamelCase` - каждое слово в переменной пишется с заглавной буквы, кроме первого. Используется во всех остальных случаях, помимо вышеуказанных.
<br>
<br>

### Объявление переменных
<br>

>`let a` - ключевое слово и имя переменной
С помощью ключевого слова даем инструкицю интерпретатору JS создать переменную.
>
>`const c = 10;` - Объявление переменной и присваивание значения.
>
>`a = true;` - присваивание (переназначение).
<br>

+ **let** - можно переназначить, переприсвоить. <ins>Можно не присваивать значение, в таком случае значение будет undefined;</ins>
+ **const** - нельзя переназначить. Обязательно сразу присвоить значение.
+ **var** - ключевое слово до ES6;
<br>
<br>

### **Тип переменной**
<br>

**ОПРЕДЕЛЯЕТСЯ ТИПОМ ПРИСВОЕННОГО ЗНАЧЕНИЕ**
<br>

**Примитивные типы:**

1. *string* (**строка**); 
2. *boolean* (**логический**) - **true/false**; 
3. *number* (**число**);
4. *null* - **значение отсутствует**; 
5. *undefuned* - **значения нет (не определенно)**; 
6. *symbol* (**символ**); 
7. *bigint*;
<br>

**Ссылочный тип:**
- *object (объект)* - переменная содержит ссылку на область в памяти где находится объект.
<br><br>

### **Динамическая типизация**
- *JS* - динамически типизируемый язык. Тип переменной не указывается, когда она объявляется.
<br><br>

**Правила работы с переменными:**
- Все переменные объявлять перед их использованием
- Стараться использовать **<ins>const</ins>** везде, где это возможно.
<br>
<br>

## **Объекты**
<br>

>*Объект* - набор свойств - **ключ: значение**.
>
>Порядок св-в не имеет значения.
>
>*Метод* - св-во объекта, которое является функцией.
<br>
<br>

**Добавление свойств:**
+ Точечная запись (Dot notation): `obj.new-property = true;`
+ Скобочная запись (Bracket notation): `obj['new-property'] = true;`

*Новое св-во обязательно в кавычках ' ', в виде строки.*

Такой синтаксис применим, если необходимо задать ключ свойства объекта, значением переменной.

```js
let nameVariable = 'new-property';
obj[nameVariable] = true;
```
В итоге, в объекте появится свойство:

```js
new-property: true,
```
Удаление свойств:
```js
delete obj.new-property // при помощи оператора delete
```
Вложенные свойства

```js
const myCity = {
 city: 'New York',
 info: {
   isPopular: true,
   country: 'USA',
 },
 street: 'Lenina',
}; 
```

Чтобы получить значение свойства с ключом *isPopular*
```js
console.log(myCity.info.isPopular);
```
Можно комбенировать записи:
```js
delete myCity.info['isPopular'];
```
Такую запись лучше использовать когда в [ ] какое-то выражение, например название переменной.
<br><br>

### **Сокращенный формат записи свойств**
<br>

*Когда используются переменные в формировании объекта и название переменной совпадает с названием ключа свойства объекта:*

```js
const name = 'Anastasia';
const postsQty = 24;

const userProfile = {
 name: name,
 postsQty: postsQty,
 hasSignedAgreement: false,
};
```

*Сокращенный вариант*
```js
const userProfile = {
 name,
 postsQty,
 hasSignedAgreement: false,
}; 
```

Сокращенные свойства рекомендуется размещать в начале объекта
<br><br>

### **Глобальные Объекты**
<br>

> + *window* - веб браузеры;
> + *global* - Node.js;
> + *globalThis* - унифицированный глобальный объекта;

**Свойства глобальных объектов**

> + *consol;*
> + *window.consol;*
> + *global.console;*

### **Методы объекта**
<br>

*Метод - свойство объекта, значение которого - функция*
```js
const myCity = {
 city: 'New York',
 cityGreeting: function () {
   console.log('Greetings!!!');
 }
};
myCity.cityGreeting(); // вызов метода cityGreeting

const myCity = {
 city: 'New York',
 cityGreeting() {
   console.log('Greetings!!!');
 }
};
myCity.cityGreeting();
```
Если значение свойства функция - можно убирать ключевое слово `function` и ставить круглые скопки после названия свойства, без двоеточия.
<br>

Метод вызывается со скобками, свойство - без.
myCity.cityGreeting(); - метод myCity.cityGreeting; - свойство.
<br><br>

## **JSON**
<br>

JAVASCRIPT OBJECT NOTATION - формат обмена данными
Набор свойства в двойных кавычках, разных типов. Передаётся в виде строки.

Конвертация JSON в JS объект (распарсить)
JSON.parse(аргумент)
Конвертация JS объекта в JSON
JSON.stringify(аргумент)

Мутация в JS
Копирование примитивных типов происходит по значению (copy by value)
Копирование ссылочного типа (copy by reference) - меняется исходный объект

Как избежать мутаций:\
Метод assign (не работает на вложенные объекты)
```js
const person = {
 name: 'Bob',
 age: 25,
};

const person2 = Object.assign({}, person);
person2.favoriteСolor = 'black';
```

Spread syntax - оператор разделения объекта на свойства (не работает на вложенные объекты)
```js
const person = {
 name: 'Bob',
 age: 25,
};

const person2 = {...person};
person2.favoriteСolor = 'black';
JSON.parse - JSON.stringify
const person = {
 name: 'Bob',
 age: 25,
 favoriteСolor: {
   oneColor: 'black',
   twoColor: 'green',},
};

const person2 = JSON.parse(JSON.stringify(person));
person2.favoriteСolor.oneColor = 'blue';
```
<br>

### **Мутация в JS**
<br>

> Копирование примитивных типов происходит по значению (copy by value);
> 
> Копирование ссылочного типа (copy by reference) - меняется исходный объект;
<br>

### **Как избежать мутаций?**
<br>

*Метод **assign** (не работает на вложенные объекты)*
```js
const person = {
 name: 'Bob',
 age: 25,
};

const person2 = Object.assign({}, person);
person2.favoriteСolor = 'black';
```
**Spread syntax** - *оператор разделения объекта на свойства (не работает на вложенные объекты)*
```js
const person = {
 name: 'Bob',
 age: 25,
};

const person2 = {...person}; //... оператор разделения объекта на свойства.
person2.favoriteСolor = 'black';
JSON.parse - JSON.stringify
const person = {
 name: 'Bob',
 age: 25,
 favoriteСolor: {
   oneColor: 'black',
   twoColor: 'green',},
};

const person2 = JSON.parse(JSON.stringify(person));
person2.favoriteСolor.oneColor = 'blue'; */
```
<br>

## **Функции**
<br>

*<ins>Блок кода, который можно выполнять многократно</ins>*

Функция может быть:
> 1. именованной;
> 2. анонимной;
> 3. присвоенна переменной;
> 4. аргументом при вызове другой функции;
> 5. значение свойства объекта (методом);

Структура функции
```js
function myFN(a, b) {
 return a + b;
}

console.log(sum(3, 11));
```

+ *function* - ключевое слово
+ *myFN* - имя функции
+ *(a, b)* - параметры, ведут себя как переменные. Значения определяются в момент вызова функции.
+ *{...}* - тело функции
+ *return* - возвращение результата. После инструкции с ключевым словом return - функция прекращает выполнение дальнейших инструкций. Если нет return, то возвращает undefined.
+ *sum(3, 11)* - вызов функции с аргументами.
<br>
<br>

### **Передача значения по ссылке**
### **Колбэк функции**
<br>

Функция вызывается внутри другой функции
```js
function anotherFunction() {
 console.log('Hola');
}

function fnWithCallback(callbackFunction) {
 callbackFunction();
}
fnWithCallback(anotherFunction);
```
<br>

### **Правила работы с функциями**
<br>

> Называйте функции исходя из выполняемых задач;
> 
> Одна задача- одна функция (single properts);
> 
> Не рекомендуется изменять внешние относительно функции переменные (pure function);

<br>

### **Области видимости**
<br>

Определяет границы действия переменной.

1. Глобальные переменные (window, global, новые переменные);
2. Локальные переменные;

*Типы области видимости*
1. Глобальная область видимости;
2. Область видимости функции;
3. Область видимости блока (любой код между { } ).
<br><br>

### **Области видимости**
*Определяет границы действия переменной*

1. Глобальные переменные (window, global, новые переменные)
2. Локальные переменные

*Типы области видимости:*
1. Глобальная область видимости
2. Область видимости функции
3. Область видимости блока (любой код между { } )
<br><br>

*Строгий режим (strict mode)*\
Инструкция интерпретатору JS анализировать код более пристально 

`'use strict'` - строка должна быть первой в глобальной области видимости или в области видимости функции.
<br><br>

**Операторы - это встроенная функция**

*Основные операторы:*
1. Арифметические `+ - * /`
2. Сравнения `=== !== <= >=`
3. Логические `! && ||`
4. Присваивания `=`

*Текстовые операторы:*
1. `typeof`
2. `instanceof`
3. `new`
4. `delete`

Еще операторы:
+ `,` - можно объявить несколько переменных
<br><br>

**Операнд (аргументы)** - то, что находится вокург операторов.

*Унарные и бинарные операторы*\
*Унарный оператор* - всегда один операнд
```js
a++
+a
typeof a
delete obj.a
}
```
*Бинарный оператор* - два операнда
```js
a = 5;
a + b;
a += b;
```
*Инфиксная запись*\
Оператор находится между операндами
```js
a = true;
a + b;
a > b;
```
*Префиксная запись*\
Оператор стоит перед операндом
```js
++a;
typeof a;
```
*Постфиксная запись*\
Оператор стоит после операндами
```js
a++
myFunction()
() - тоже оператор
```
*Приоритетность операторов*\
Можно понять логически или восспользоваться таблицой приоритетности
<br><br>

### **Логические операторы**
> + `!` - не (всегда позвращает значение типа Boolean)
> 
> + `&&` - и (возвращает значение одного из операндов)
> 
> + `||` - или (возвращает значение одного из операндов)

*Ложные значения*\
Значения, которые при приведении к логическому типу дают `false`

> 1. Boolean(value) -> false
> 2. false
> 3. 0
> 4. ''
> 5. undefined
> 6. null\
*Все остальные - истынные значения*

**typeof** - показывает тип данных
унарный, префиксный, текстовый оператор.

Значение всегда строка, которая показывает тип.

Две формы записи:
```js
typeof(10)
typeof 10
```
**Оператор НЕ ! (отрицание)**\
Чаще всего используется в условных инструкциях
```js
!10         // false
!0          // true
!'abc'      // false
!undefined  // true
```
**Оператор НЕ НЕ !! (отрицание отрицание)**\
Можно легко конвектировать любое значение в булевое
```js
!!10        // true
!0          // false
!'abc'      // true
!undefined  // false
```
**Операторы && и ||**\
Являются операторами короткого замыкания (short circuit)\
**Выражение возвращает значение.**
> Выражение 1 && Выражение 2
<br>

Если Выражение 1 ложо, то Выражение 2 игнорируется. И возвращается результат Выражения 1 как как результат всего выражения Выражение 1 && Выражение 2 (возвращает перое ложно, либо последний операнд)
<br>

> Выражение 1 || Выражение 2

Если Выражение 1 истина то Выражение 2 игнорируется. И возвращается результат Выражения 1 как как результат всего выражения Выражение 1 || Выражение 2 (возвращает перое истина, либо последний операнд)
<br><br>

**Оператор разделения объекта на свойства ...**

```js
const button = {
 width: 200,
 text: 'Buy',
};

const redButton = {
 ...button,        // скопировали объект
 color: 'red',     // добавили свойство
};
```
**Объединение объектов с помощью ...**

```js
const buttonInfo = {
 text: 'Buy',
};

const buttonStyle = {
 color: 'yellow',
 width: 200,
 height: 300,
};

const button = {
 ...buttonInfo,
 ...buttonStyle
};

console.log(button);
```
**Конкатинация строк**\
Оператор + для соединения строк

```js
'Hello ' + 'World'
```
**Переменные в конкатинации**

```js
const hello = 'Hello';
const world = 'World';
const greeting = hello + ' ' + world;
```
**Шаблонные строки (template string literal)**

```js
const hello = 'Hello';
const world = 'World';

const greeting = `${hello} ${world}`;
```

**Функциональные выражения**\
Разница между объявленной функцией и функциональным выражением

*Объявленная функция*

```js
function myFn(a, b) {
 let c;
 a = a = 1;
 c = a + b;
 return c;
}
```
*Функциональное выражение*

```js
function(a, b) {
 let c;
 a = a = 1;
 c = a + b;
 return c;
}
```
**Функциональные выражения всегда анонимные**

Присвоение функционального выражения переменной

```js
const myFunction = function(a, b) {
 let c;
 a = a = 1;
 c = a + b;
 return c;
};

myFunction(5, 3);
```
<br><br>

### **Стрелочные функции**
**Всегда анонимные**

```js
(a, b) => {
 let c;
 a = a = 1;
 c = a + b;
 return c;
}
```
*Присвоение стрелочной функции*

```js
const myFunction = (a, b) => {
 let c;
 a = a = 1;
 c = a + b;
 return c;
};
```
*Сокращения в стрелочных функциях:*\
1. Если один параметр, то круглые скобки можно опустить

> a => { // тело функции }

2. Если тело функции состоит из одного выражения, то фигурные скобки можно опустить

> (a, b) => a + b

(неявно возвращает результат, без return).
<br>

### **Значения параметров функции по умолчанию**

```js
function multByFactor(value, multiplier = 1) {
 return value * multiplier;
}

console.log(multByFactor(10, 2));
console.log(multByFactor(5));
```
*Неявный возврат*

```js
const newPost = (post, addedDt = Date()) => ({
 ...post,
 addedDt,
});

const firstPost = {
 id: 777,
 autor: 'Ananas',
};

console.log(newPost(firstPost));
```
*Возврат при помощи **return***

```js
const newPost = (post, addedDt = Date()) => {
 return {
   ...post,
   addedDt,
 };
};

const firstPost = {
 id: 777,
 autor: 'Ananas',
};

console.log(newPost(firstPost));
```
<br>

### **Обработка ошибок**

```js
const fnWithError = () => {
 throw new Error('Some error');
};

fnWithError();

console.log('Continue...');
//log не отобразится из-за ошибки
```
<br>

### **TRY/CATCH**

```js
try {
 // выполнение блока кода
} catch (error) {
 //этот блок выполняется в случае возникновения ошибок в блоке try
}
const fnWithError = () => {
 throw new Error('Some error');
};

try {
 fnWithError();
} catch (error) {
 console.error(error);
 console.log(error.massage);
}

console.log('Continue...');
```
<br>

### **Инструкции**
**Выражение всегда возвращает значение**\
Инструкция выполняет определенные действия.
<br><br>

## **Массивы**
*Объект с цифровыми именами свойств*

*Формат записи массивов*

```js
const myArray = [1, 2, 3];
console.log(myArray);
const myArray2 = new Array (1, 2, 3);
console.log(myArray2);
```
**Методы массивов (основные)**
1. **push** (добавить в конец массива)
2. **pop** (удалить элемент с конца массива, возвращает удаленный элемент)
3. **shift** (удаляет первый элемент массива и возвращает его если присвоить его)
4. **unshift** (добавить элемент в начале массива )
5. **forEach**
6. **map**
<br><br>

**Методы массивов** - функции высшего порядка в массивах (функции, методы протатипов).

```js
const myArray = [1, 2, 3];
console.log(myArray);

myArray.push('a');    // добавить в конец

myArray.pop('b');     // удалить с конца

myArray.shift(4);   // удаляет первый элемент

myArray.unshift(11); // добавить элемент в начале
```
**forEach**\
Перебирает все элементы массива и выполняет определенные действия с каждым элементом. Метод не меняет оригинальный массив.
Для каждого элемента массива будет вызывать колбек функцию.

```js
const myArray = [1, 2, 3];
console.log(myArray);
Короткая запись

myArray.forEach(item => console.log(item * 2));
Обычная запись

myArray.forEach(function(item) {
 console.log(item * 2);
});
```

**forEach** возвращает undefined, так как служит только для перебора элементов массива и выполнение определенных действий с каждым элементом перебора

```js
const res = myArray.forEach(item => console.log(item * 2));

console.log(res);  // undefined 
```
<br>

### **MAP**
Перебирает все элементы массива, выполняет определенные действия с каждым элементом как и forEach, но возвращает новый массив.

```js
const myArray = [1, 2, 3];

const newArray = myArray.map(item => item * 3);
```
<br>

### **Деструктуризация объекта**
*Создание новых переменных относительно свойств объекта (на основе свойств объекта).*\
Можно создать так

```js
const userProfile = {
 name: 'Ananas',
 commentsQty: 23,
 hasSignedAgreement: false,
};


const name = userProfile.name;
const commentsQty = userProfile.commentsQty;
const hasSignedAgreement = userProfile.hasSignedAgreementy;
//Правильнее так

const {name, commentsQty} = userProfile;

//или отдельно

const {hasSignedAgreement} = userProfile;
```

В фигурных скобках, название новых переменных, которые совпадают с ключами свойств объекта, на основе которого новые переменные и создаются (имя объект указывается справа, после знака присваивания). Порядок имен переменных в квадратных скобках не имеет значение, так как название переменных и ключа свойств одинаковые.
<br><br>

### **Деструктуризация массива**
<br>
Почти тоже самое, что и в деструктуризации объектов, но фигурные скобки заменяем на квадратные и учитывем то, что порядок элементов в массиве имеет значение. Название переменных в квадратных скобках произвольные, но значения соответствуют индексу массива на основе которого переменные создаются.
<br><br>

```js
const fruits = ['Apple', 'Banana'];
const [apple, fruitTwo] = fruits;

console.log(apple);     // Apple
console.log(fruitTwo);  // Banana
```
<br>

### **Деструктуризация параметров функции**
*Если функция получает объект в качестве параметров, то можно применить деструктуризацию этого объекта, чтобы использовать только необходимые свойства*

```js
const userProfile = {
 name: 'Ananas',
 commentsQty: 0,
 hasSignedAgreement: false,
};

const userInfo = ({name, commentsQty}) => {
 if (!commentsQty) {
   return console.log(`User ${name} has no comments`);
 }
 return console.log(`User ${name} has ${commentsQty} comments`);
};
userInfo(userProfile);
```
<br>

### **Условные инструкции**
> if
> 
> if ... else
> 
> if ... else if (if ... else if ... else)
> 
> switch
> 
> тернарный оператор

**Инструкия IF**
```js
if (условие) {
 // блок кода, выполняется однократно, если условие правдиво
}
let val = 10;

if (val > 5) {
 val+=20;
}
console.log(val);
```
**Инструкия IF ELSE**

```js
if (условие) {
 // блок кода, выполняется однократно, если условие правдиво
} else {
 // блок кода, выполняется однократно, если условие ложно
}
let val = 10;

if (val < 5) {
 val+=20;
} else {
 val -= 20;
}
console.log(val);
```
**Инструкия IF ELSE IF**

```js
if (условие 1) {
 // блок кода, выполняется однократно, если условие 1 правдиво
} else if (условие 2) {
 // блок кода, выполняется однократно, если условие 2 правдиво
} else {
 // блок кода, выполняется однократно, если предыдущие условия ложны
}
const age = 18;

if (age >= 18) {
 console.log('Is adult');
} else if (age >= 12) {
 console.log('Is teenager');
} else {
 console.log('Is child');
}
```

**Использование IF в функциях**

```js
const sumPositiveNumbers = (a, b) => {
 if (typeof(a) !== 'number' || typeof(b) !== 'number') {
   return 'One of the arguments is not a number';
 }

 if (a <= 0 || b <= 0) {
   return 'Numbers are not positive';
 }

 return a + b;
};
```

**SWITCH**\
Альтернатива для if...if else...if

```js
switch (выражение) {
 case A:
   // Действие если выражение === А
   break;
 case B:
   // Действие если выражение === B
   break;
 default:
   // действие по умолчанию
}
```
**break** - остановка (выход).\
Если не установить, то проверка по case продолжится.
<br>

**switch** - проверка на строгое равенство
```js
const month = 5;
switch (month) {
 case 12:
   console.log('Декабрь');
   break;
 case 1:
   console.log('Январь');
   break;
 case 2:
   console.log('Февраль');
   break;
 default:
   console.log('Это не зимний месяц');
}
```
<br>

### **Тернарный оператор**
**У тернарного оператора три операндами** 

Конструкция с тернарным оператором - это выражение, а выражение всегда возвращает значение.

> **Условие ? Выражение 1 : Выражение 2**

В условиях может быть любое выражение (проверка на true)

__Если условие правдиво, то возвращается результат Выражения 1
Если условие ложно - результат Выражения 2;__

**Можно писать так:**
```js
Условие
 ? Выражение 1
 : Выражение 2
```
**Примеры:**
```js
const value = 11;

value
 ? console.log('Условие истенно')
 : console.log('Условие ложно');

const value1 = 11;
const value2 = 25;

value1 && value2
 ? myFunction(value1, value2)
 : myFunction();
let value = 11;

console.log(value >= 0 ? value : -value);

let res = value >= 0 ? value : -value;
console.log(res);
```
<br>

### **Циклы**
***
1. for
2. for...in...
3. while
4. do...while
5. for...of...
***
<br>

1. **Цикл for**

**for**(Начальная инструкция; Условие; Итерационное действие) {
// Блок кода, выполняемый на каждой итерации
}
```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
**Для перебора массивов не нужен цикл for**

Лучше использовать функции высшего порядка - **"forEach", "map", "reduce"**

Вот как всё таки применяется for для массивов:
```js
const myArray = ['first', 'second', 'third'];

for (let i = 0; i < myArray.length; i++) {
  console.log(myArray[i]);
}
```
**Метод forEach**
```js
const myArray = ['first', 'second', 'third'];

myArray.forEach((element, index) => {
  console.log(element, index);
});
// first 0
// second 1
// third 2
```
**element** - каждый элемент массива
**index** - индекс каждого элемента (параметр опционален);
<br><br>

**Цикл while**

Выполняет блок кода, пока условие правдиво, если условие ложно, то не выполниться ни разу.
```js
while (Условие) {
  // Блок кода, выполняемый на каждой итерации
}
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```
*Если не указать изменение i, то есть убрать i++, то цикл будет бесконечный.*
<br><br>

**Цикл do while**

Выполнится как минимум один раз
```js
do {
  // Блок кода, выполняемый на каждой итерации (выполняется хотя бы один раз)
}
while (Условие)
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);
```
Сначала выводится 0, увеличивается на единицу i++; и уже после этого проверяется условие while (i < 5)

Применяется тогда, когда блок кода нужно выполнить хотя бы раз
<br><br>

**Цикл for in (для *объектов*)**

Можно выполнять действия с каждым свойством объекта.
```js
for (key in Object) {
  // Действия с каждым свойством объекта
  // Значения свойства - Object[key]
}
```
+ key - название переменной (название свойства объекта)

+ Object - объект 
 
+ Object[key] - значение свойства
```js
const myObject = {
  x: 10,
  y: true,
  z: 'abc',
};

for (let key in myObject) {
  console.log(`${key}:${myObject[key]}`);
}

// x:10
// y:true
// z:abc
```
<br>

**forEach для объектов (методы keys и values)**
```js
const myObject = {
  x: 10,
  y: true,
  z: 'abc',
};

Object.keys(myObject).forEach(key => {
  console.log(key, myObject[key]);
});

// x 10
// y true
// z abc
```
*Object.keys(myObject)* - метод keys переменной Object, для получения всех ключей объекта в виде массива (массив свойст) и далее перебор элементов этого массива forEach.

Можно сразу перебирать значения свойств объекта
```js
const myObject = {
  x: 10,
  y: true,
  z: 'abc',
};

Object.values(myObject).forEach(value => {
  console.log(value);
});

// 10
// true
// abc
```
*Object.values(myObject) - поучение всех значений свойств объекта в виде массива*
<br>

**Цикл for in (для массивов)**
__!!! ТАК ДЕЛАТЬ НЕ РЕКОМЕНДУЕТСЯ__

```js
const myArray = [true, 10, 'abc', null];

for (const key in myArray) {
  console.log(myArray[key]);
}

// true
// 10
// abc
// null
```
<br>

**Цикл for of**

> for (Element of Iterable) {
  // Действия с определенным элементом
}

**Для строк**
```js
const myString = 'Hey';

for (const letter of myString) {
  console.log(letter);
}

// H
// e
// y
```
<br>

**Для массивов**
```js
const myArray = [true, 10, 'abc', null];

for (const element of myArray) {
  console.log(element);
}

// true
// 10
// abc
// null
```
**!!! FOR OF НЕ ДЛЯ ОБЪЕКТОВ**
<br><br>

## **МОДУЛИ**
*Позволяют структурировать код*

*Позволяюь избегать дублирования блоков кода*

**EXPORT/IMPORT (ES6)**

> moduleOne.js => moduleTwo.js export... => import...

Связь модулей. 

Из модуля moduleOne.js экспортируются (переменные, функции и тд), а в moduleTwo.js импортируются с первого модуля

moduleOne.js Экспортируем функцию myName (теперь доступна для других модулей)

```js
const myName = () => {
  console.log('Ananas');
};

export default myName;  // экспорт функции
moduleTwo.js
```
Импортируем функцию *myName* из модуля *moduleOne.js*
```js
impoort printMyName from './moduleOne.js';

printMyName();  // Ananas
'./moduleOne.js' - строка-путь ( ./ - находятся в одной папке, .js - можно опускать)
```
myName и printMyName - отличаются названия, что допускается при default экспорте

**Несколько экспортов**
```js 
moduleOne.js
const one = 1;
const two = 'two';

export {
  one,
  two
}

moduleTwo.js
import {
  one,
  two
} from './moduleOne.js';

console.log(one);  // 1
console.log(two);  // two
```
Имена переменных должны совпадать, но их можно переименовать при импорте
```js
moduleTwo.js

import {
  one as oneRenamed
  two
} from './moduleOne.js';

console.log(oneRenamed);  // 1
console.log(two);  // two
as - указать новое имя, после импорта
```

**Правила работы с модулями**

1. Модули должны быть одноцелевыми
2. Распологайте все export инструкции внизу файла
3. Распологайте все import инструкции сверху файла
4. По возможности используйте export default
5. Сначала import из внешних пакетов, а потом собственных
<br><br>

## **Классы и прототипы**
Синтаксис классов появился в ES6

С помощью классов можно создавать шаблоны, либо заготовки для объектов и потом, на основании этих заготовок создавать экземпляры объектов

`class ...`

классы позволяют создавать прототипы для обюъектов
на основании прототипов создаются экземпляры
экземпляры могут иметь собственные свойства и методы
экземпляры наследуют свойства и методы прототипов

```js
class Comment {
  constructor(text) {
    this.text = text;
    this.votesQty = 0;
  }

  upvote() {
    this.votesQty +=1;
  }
}
```
+ `class` - ключевое слово

+ `Comment` - название класса (PascalCase notation)

+ `{}` - внутри всё что касается класса( свойтсва и методы)

+ `constructor` и `upvote` - методы, в скобках () - опциональные параметры и далее тело {} конкретного метода

+ `this` - спец переменная указывает на экземпляр класса (ссылается на новый экземпляр)
<br><br>

**Создание экземпляров класса**
```js
const firstComment = new Comment('First comment');
```
`new `- префиксный унарный оператор (вызывается функция constructor);

`upvote` - унаследован свойства экземпляра;
<br><br>

**Цепочка прототипов**

`firstComment => Comment => Object`
<br><br>

**Проверка принадлежности instanceof**
```js
console.log(firstComment instanceof Comment);
console.log(firstComment instanceof Object);

// true
// true
```
<br>

**Вызов унаследованных методов**
```js
const firstComment = new Comment('First comment');

firstComment.upvote();
console.log(firstComment.votesQty);

firstComment.upvote();
console.log(firstComment.votesQty);

firstComment.upvote();
console.log(firstComment.votesQty);

// 1
// 2
// 3
```
<br>

**Проверка принадлежности свойств экземпляру объекта hasOwnProperty**
<br>

*Есть ли у firstComment собственное свойство*
```js
const firstComment = new Comment('First comment');

console.log(firstComment.hasOwnProperty('text'));

console.log(firstComment.hasOwnProperty('votesQty'));

console.log(firstComment.hasOwnProperty('hasOwnProperty')); // наследуется от класса  Comment

console.log(firstComment.hasOwnProperty('upvote')); // наследуется от класса  Comment

// true
// true
// false
// false
```
<br>

**Создание нескольких экземпляров**
```js
const firstComment = new Comment('First comment');
const secondComment = new Comment('Second comment');
const thirdComment = new Comment('Third comment');
```
<br>

### **Статические методы**
*Метод доступен как свойство класса и не наследуется экземплярами класса*
```js
class Comment {
  constructor(text) {
    this.text = text;
    this.votesQty = 0;
  }

  upvote() {
    this.votesQty +=1;
  }

  static mergeComments(first, second) {
    return `${first} ${second}`;
  }
}

Comment.mergeComments('First comment.', 'Second comment.');
```
<br>

Расширение других классов **extends**
```js
class NumbersArray extends Array {
  sum() {
    return this.reduce((el, acc) => acc += el, 0);
  }
}

const myArray = new NumbersArray(2, 5, 7);

console.log(myArray);
myArray.sum();
```
**Array** - родительский класс для NumbersArray 

*constructor* не нужен, так как расширяя Array, конструктор родительского класса вызовется автоматически.

Цепочка прототипов

`mArray => NumbersArray => Array => Object`

Что такое прототип?
> У каждого экземпляра есть скрыто свойство `__proto__`
>
>Свойство `prototype` класса - равно свойсту `__proto__` любого экземпляра
>
> `Comment.prototype === firstComment.__proto__`
<br><br>

## **Промисы**
*Позволяют обрабатывать отложенные во времени события*

**Асинхронный запрос** - не знаете, когда получите ответ (не сразу, а через какое-то время);

**Промис** - это обещание предоставить результат позже (возвращает ошибку, если предоставить невозможно);
<br><br>

**Состояния промиса:**
1. **ожидание (pending)** - промис создаётся;
2. **исполнен (resolved)** - результат получен;
3. **откланен (rejected)** - вернул ошибку;
<br><br>

**Создание промиса**\
Только созданный промис в состоянии ожидания(pending)

```js
const myPromise = new Promise((resolve, reject) => {
  
  //Выполнение асинхронных действий
  
   //Внутри этой функции нужно в результате вызвать одну из функций resolve или reject
 
});
```
+ **new** - (вызывается constructor) создает новый экземпляр класса Promise(присутствует в js) и присвоен переменной;
+ **(resolve, reject) => {}** - колбек функция;
+ **resolve, reject** - два обязательных параметра;
+ **{}** - в теле колбек функции нужно вызвать resolve или reject;
+ **resolve** - передать какой-то результат (данные) и когда была вызвана функция resolve, промис считается исполнен (меняется состояние с состояния ожидания);

Если возникла ошибка, то нужно вызвать функцию reject и передать ту ошибку, которая возникла. В таком случае промис считается откланенным/
<br><br>

*Получение рузультата промиса*:
```js
myPromise
  .then(value => {
    //Действие в случае успешного исполнения промиса
    //Значение value - это значение, переданное в вызове функции resolve внутри Промиса
  })
  .catch(error => {
    //Действие в случае отклонения Промиса
    //Значение error - это значение, переданное в вызове функции reject внутри Промиса
  });
```
У объекта **myPromise** доступны методы **.then** и **.catch**.

В **.then** и **.catch** в параметрах нужно предать функцию с одним параметром (**value или error**).

*Практика по использованию промисов и fetch:*

```js
fetch('https://jsonplaceholder.typicode.com/todos/55')
  .then(response => {
    console.log(response);
    return response.json();
  })
  .then(json => console.log(json));
  .catch(error => console.error(error));
Вызов fetch внутри промиса
const getData = (url) => 
  new Promise((resolve, reject) =>
    fetch(url)
      .then(response => response.json());
      .then(json => resolve(json));
      .catch(error => reject(error));
    );

getData('https://jsonplaceholder.typicode.com/todos/55')
  .then(data => console.log(data));
  .catch(error => console.log(error.massage));
```
<br><br>

## **ASYNC/AWAIT**
*Специальный синтаксис для упрощения работы с промисами*

**Асинхронные функции**\
Функция, которая вместо какого-то значения (undefined, cnстрокачисло и тд), возвращает промис.

> Чтобы создать асинхронную функцию, нужно добавить ключевле слово **acync**

Традиционное объявление - ключевое слово перед функцией
```js
acync function asuncFn() {
  //Всегда возвращает Промис
};
```
Другие типы функций - ключевое слово после = (перед началом функции)

```js
const asyncFn = async () => {
  //Всегда возвращает Промис
};
const asyncFn = async () => {
  return 'Success';
};

asyncFn()
 .then(value => console.log(value));
const asyncFn = async () => {
  throw new Error('There was an error!');
};

asyncFn()
  .then(value => console.log(value))
  .catch(error => console.log(error.message));
```
### **Главное в ASYNC/AWAIT**
+ `async/await` - это синтаксическая надстройка над промисами
+ `await` синтаксис возможен только внутри async функции
+ `async` функция всегда возвращает Promise
+ `async` функция ожидает результата инструкции await и не выполняет последующие инструкции.







