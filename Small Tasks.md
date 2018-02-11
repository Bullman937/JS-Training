### 1) Alert
Вывести на страницу любую надпись
```
alert ("I'm JavaScript")
```

### 2) Work with variables
```
var admin;
var name;

name = "Василий";
admin = name;

alert (admin);
```

### 3) Simple page
Создать страницу, которая спрашивает имя и выводит его.
```
var name = prompt ("Ведите ваше имя", "Владислав");

alert ("Привет, " + name + "!")
```

### 4) Checking the standard
Простой пример с оператором if-else
```
var question = prompt ("Каково «официальное» название JavaScript?", '');

if (question == 'ECMAScript'){
	alert ("Верно!")
}
else{
	alert("Не знаете? «ECMAScript»!")
}
```

### 5) get the sign of a number
Простой пример с оператором if-else (2)
```
var question = prompt ("Введите число", '');

if (question>0){
	alert (1);
}
else if (question<0){
	alert (-1);
}
else{
	alert(0)
}
```

### 6) Login verification
Проверка на корректность логина и пароля
```
var login = prompt ("Кто пришёл", '').toLowerCase();

if (login == "admin"){
	var password = prompt ("Введите пароль: ", '');
  if (password == "qwerty"){
  	alert ("Доступ разрешен")
  }
  else if (password == null){
  	alert ("Вход отменен")
  }
  else{
  	alert ("Неверный пароль")
  }
}

else if (login == null){
	alert ("Вход отменен")
}

else{
	alert ("Я тебя не знаю")
}
```

### 7) Ternary operator
Простой пример с использованием "?"
```
var a = prompt ("Введите число А", '0');
var b = prompt ("Введите число B", '0');

result = (a + b < 4) ? "Мало" : "Много";

alert (result)
```

### 8) Login verification vith ternary operator
Проверка на корректность логина и пароля с помощью тернарного оператора
```
var login = prompt ("Введите ваш логин: ", '').toLowerCase();

var message = (login == "admin") ? "Привет!" :
  (login == "director") ? "Здравствуйте!" :
  (login == "") ? 'Необходимо ввести логин' :
  "Я тебя не знаю";

alert (message);
```

### 9) Check IF
Если возраст меньше 18 и больше 90 включительно, то закрыть доступ
```
var age = prompt ("Введите ваш возраст", '');

if (age>=18 && age<=90){
	alert ("Доступ разрешен")
}
else{
	alert ("Нет доступа")
}
```

### 10) Check IF (2)
Если возраст меньше 18 и больше 90 включительно, то открыть доступ
```
//---------------------- Вариант №1--------------------------
var age = prompt ("Введите ваш возраст", '');

if (age < 18 || age > 90){
	alert ("Доступ разрешен")
}
else{
	alert ("Нет доступа")
}
```

```
//---------------------- Вариант №2--------------------------
var age = prompt ("Введите ваш возраст", '');

if (!(age>=18 && age<=90)){
	alert ("Доступ разрешен")
}
else{
	alert ("Нет доступа")
}
```

### 11) Output of even numbers
С помощью цикла FOR вывести четные числа от 0 до 10
```
//---------------------- Вариант №1--------------------------
for (var i=1; i<10; i++){
	if (i%2 == 0){
  	alert (i);
  }
}
```

```
//---------------------- Вариант №2--------------------------
for (var i=0; i<=10; i++){
	if (i%2 == 1) continue
  	alert (i);
}
```

### 12) Change FOR to WHILE
Переписать код с циклом FOR на код с циклом WHILE
```
for (var i = 0; i < 3; i++) {
  alert( "номер " + i + "!" );
}
```

```
var i = 0;
while (i<3) {
  alert( "номер " + i + "!" );
  i++;
}
```

### 13) Repeat cycle until input is incorrect
Написать цикл, который предлагает prompt ввести число, большее 100. Если посетитель ввёл другое число – попросить ввести ещё раз, и так далее.
```
var question;

do {
  question = prompt("Введите число больше 100?", 0);
} while (question<=100 && question!=null);
```

### 14) Rewrite SWITCH to IF
Написать if..else, соответствующий следующему switch:
```
switch (browser) {
  case 'IE':
    alert( 'О, да у вас IE!' );
    break;

  case 'Chrome':
  case 'Firefox':
  case 'Safari':
  case 'Opera':
    alert( 'Да, и эти браузеры мы поддерживаем' );
    break;

  default:
    alert( 'Мы надеемся, что и в вашем браузере все ок!' );
}

```

```
var question = prompt ("Введите ваш браузер:", '').toLowerCase();

if (question == "ie"){
  alert ("О, да у вас IE!")
}
else if (question == "chrome" || question == "firefox" || question == "safari" || question == "opera"){
  alert ("Да, этот браузер мы поддерживаем")
}
else{
  alert ("Мы надеемся, что и в вашем браузере все ок!")
}
```

### 15) Rewrite IF to SWITCH
Переписать код с использованием одной конструкции switch:
```
var a = +prompt('a?', '');

if (a == 0) {
  alert( 0 );
}
if (a == 1) {
  alert( 1 );
}

if (a == 2 || a == 3) {
  alert( '2,3' );
}
```

```
var a = +prompt('a?', '');

switch (a) {
  case 0:
    alert( 0 );
    break;

  case 1:
    alert( 1 );
    break;

  case 2:
  case 3:
    alert( '2,3' );
    break;
}
```

### 16) Fuunction MIN
Написать функцию, которая возвращает наименьшее из двух чисел
```
function min(a,b){
	if (a>b){
  	return a;
  }
  return b;
}

alert (min(6,5))
```

### 17) Fubction POW
Написать функцию возведения числа в степень
```
var x = +prompt("Введите число:", '');
var n = +prompt("Введите степень:", '')

function pow(x,n){
	var result = 1;
  for(i=0; i<n; i++){
  	result *= x;
  }
  return result;
}

alert (x + " в степени " + n + " = " + pow(x,n))
```

### 18) The sum of numbers up to this point
Написать функцию sumTo(n), которая для данного n вычисляет сумму чисел от 1 до n
```
//---------------------- Вариант №1--------------------------
function sumTo(n){
	if n == 1) return 1;
	return n + sumTo(n-1)
}

alert(sumTo(3)) // 1+2+3 = 6
```

```
//---------------------- Вариант №2--------------------------
function sumTo(x){
	var sum = 0;
	for (i=0; i<=x; i++){
  	sum += i;
  }
  return sum;
}

alert(sumTo(5)) // 1+2+3+4+5 = 15
```

### 19) Calculate factorial
Написать функцию, которая вычисляет факториал числа
```
//---------------------- Вариант №1--------------------------
function factorial (n){
	if (n==1){
  	return 1;
  }
  else{
  	return n* factorial (n-1);
  }
}

alert(factorial (5)) // 1*2*3*4*5 = 120
```

```
//---------------------- Вариант №2--------------------------
function factorial (n){
  if (n==1){
    return 1;
  }
  else{
    var result = 1;
    for (var i=1; i<=n; i++){
      result *= i;
    }
  }
  return result;
}

alert(factorial (6))
```

### 20) Addition of prices
Сложить 2 дробных числа
```
var a = 0.1;
var b = 0.2

alert ((a+b).toFixed(1)) //необходимо округлить до 1 знака для более наглядного вычисления
```

### 21) Math random (0, max)
Вывести случайно число из диапазона 0..max
```
var max = +prompt("Введите максимальное число", 1);

alert (Math.random() * max)
```

### 22) Math random (min, max)
Вывести случайное число из диапазона min..max, введенным пользователем
```
var min = +prompt("Введите минимально число", 0);
var max = +prompt("Введите максимальное число", 0);

if (min>max){
  alert ("min>max, так нельзя")
}
else{
  alert (getRandomArbitary(min,max))
}

function getRandomArbitary(min, max){
  var rand = Math.round(Math.random() * (max - min) + min);
  return rand;
}
```

### 23) Make the first character capitalized
Написать функцию ucFirst(str), которая возвращает отфармотированную полученную строку с заглавным первым символом
```
var word = "пРиВЕт".toLowerCase();

function ucFirst (str){
  str = str[0].toUpperCase() + str.slice(1);
  return str;
}

alert (ucFirst(word))
```

### 24) Check spam
Написать функцию checkSpam(str), которая возвращает true, если строка содержит „viagra“ или „XXX“, а иначе false.
```
var word = prompt("Введите запрос", '').toLowerCase()

function checkSpam(str){
	while (str.indexOf('viagra') || str.indexOf('xxx')){
  	alert ("Данный запрос недопустим");
    break;
  }
}

checkSpam(word)
```

### 25) Cut the string
Создать функцию truncate(str, maxlength), которая проверяет длину строки str, и если она превосходит maxlength – заменяет конец str на "...", так чтобы ее длина стала равна maxlength.
```
var string = prompt("Введите строку", '');
var maxLength = +prompt("Введите максимальное количество отображаемых символов");

function truncate(str, maxlength){
	if(str.length > maxlength){
		return str = str.slice(0, maxlength+1) + "..."
  }
  else{
  	return str
  }
}

alert(truncate (string, maxLength))
```

### 26) Select number
Есть стоимость в виде строки: "$120". То есть, первым идёт знак валюты, а затем – число.
Создать функцию extractCurrencyValue(str), которая будет из такой строки выделять число-значение, в данном случае 120.
```
var string = "$120"

function extractCurrencyValue(str){
  var result = +str.slice(1)
  return result;
}

alert(extractCurrencyValue(string));
```

### 27) Is object empty?
Написать функцию, которая возвращает true, если в объекте есть свойства, и false, если свойст нет
```
function isEmpty(obj) {
	var counter = 0;
  for (var key in obj){
  	counter++;
  }
  if (counter>0){
  	return true;
  }
  else{
  	return false;
  }
}

var person = {};

alert(isEmpty(person)); // false
person.name = "Владислав";
alert(isEmpty(person)); // true
```

### 28) Sum of propertis
Есть объект salaries с зарплатами. Напишсать код, который выведет сумму всех зарплат.
```
var salaries = {
  "Вася": 100,
  "Петя": 300,
  "Даша": 250
};

var counter = 0;
for (var key in salaries){
	counter += salaries[key]; 
}

alert (counter)
```

### 29) The property with the highest value
Есть объект salaries с зарплатами. Написать код, который выведет имя сотрудника, у которого самая большая зарплата.
```
var salaries = {
  "Вася": 100,
  "Петя": 300,
  "Даша": 250
};

var max = 0;
var name = "Нет сотрудников"
for (var key in salaries){
	if(salaries[key] > max){
  	max = salaries[key];
    name = key;
  }
}

alert (name)
```

### 30) Multiply Numerical Properties by 2
Создать функцию multiplyNumeric, которая получает объект и умножает все численные свойства на 2. 
```
var salaries = {
  "Вася": 100,
  "Петя": 300,
  "Даша": 250,
  title: "My menu"
};

function multiplyNumeric(obj){
  for (var key in obj){
    if (typeof(obj[key]) == 'number'){
      obj[key] *= 2
    }
  }
  return obj
}

console.log(multiplyNumeric(salaries))
```

### 31) Get the last element of array
Получить последний элемент из массива
```
var arr = ['one', 'two', 'three', 'four', 'five', 'six',]

var lastElement = '';

for (var i=0; i<arr.length; i++){
	lastElement = arr[i];
}
alert (lastElement)
```

### 32) Add new elements to array
Добавить новый элемент в начало и конец массива
```
var arr = ["one", "two", "three", "four", "five", "six",]

arr.push("seven") // добавить элемент в конец
alert (arr)
arr.unshift("zero") // добавить элемент в начало
alert (arr)
```

### 33) Create array in 5 steps
1) Создайте массив styles с элементами «Джаз», «Блюз».
2) Добавьте в конец значение «Рок-н-Ролл»
3) Замените предпоследнее значение с конца на «Классика». Код замены предпоследнего значения должен работать для массивов любой длины.
4) Удалите первое значение массива и выведите его alert.
5) Добавьте в начало значения «Рэп» и «Регги».
```
var arr = ["Джаз", "Блюз"];

arr.push("Рок-н-Ролл")
alert (arr);

arr[arr.length-2] = "Классика"
alert (arr);

arr.shift(arr[0]);
alert (arr);

arr.unshift("Рэп", "Рэгги")
alert (arr);
```

### 34) Array's elements calculator
Напиcать код, который:

1) Запрашивает по очереди значения при помощи prompt и сохраняет их в массиве.
2) Заканчивает ввод, как только посетитель введёт пустую строку, не число или нажмёт «Отмена».
3) При этом ноль 0 не должен заканчивать ввод, это разрешённое число.
4) Выводит сумму всех значений массива.
```
var numbers = [];

while (true) {
  var value = prompt("Введите число", 0);
  if (value == "" || value == null || isNaN(value)){
    break;
  }
  numbers.push(+value);
}

var sum = 0;
for (var i=0; i<numbers.length; i++){
	sum += numbers[i]
}

alert ("Элементы в массиве: " + numbers);
alert ("Сумма элементов массива: " + sum);
```

### 35) Search in array
Создать функцию find(arr, value), которая ищет в массиве arr значение value и возвращает его номер, если найдено, или -1, если не найдено.
```
var arr = ["test", 2, 1.5, false];

function find (arr, value){
  var findest = '';
  for (var i=0; i<arr.length; i++){
    if (value === arr[i]){
      findest = i;
      return findest;
    }
  }
  return -1;
}

alert(find (arr, 2)); // 1
alert(find (arr, false)); // 3
alert(find (arr, 0)); // -1
```

### 36) Filtered array
Создать функцию filterRange(arr, a, b), которая принимает массив чисел arr и возвращает новый массив, который содержит только числа из arr из диапазона от a до b. То есть, проверка имеет вид a ≤ arr[i] ≤ b. Функция не должна менять arr.
```
var arr = [5, 4, 3, 8, 0];

function filtered (arr, a, b){
	var filteredArr = [];
  for (var i=0; i<arr.length; i++){
  	if (i>=a && i<=b){
    	filteredArr.push(arr[i]);
    }
  }
  return filteredArr;
}

alert(filtered(arr,0,2));
```

### 37) Add class to string
В объекте есть свойство className, которое содержит список «классов» – слов, разделенных пробелом. Создать функцию addClass(obj, cls), которая добавляет в список класс cls, но только если его там еще нет.
```
var obj = {
  className: 'open menu'
}

function addClass(obj, cls){

  for (var key in obj){
    var arr = obj[key].split(' ');
  }

  for (i=0; i<=arr.length; i++){
    if (arr[i] == cls){
      var str = arr.join(' ')
      obj.className = str;
      return obj;
    }
    if (i == arr.length && arr[i] !== cls){
      arr.push(cls);
      var str = arr.join(' ')
      obj.className = str;
      return obj;
    }
  }
}

addClass (obj, "new")
```

### 38) Function camelSize
Напиcать функцию camelSize(str), которая преобразует строки вида «my-short-string» в «myShortString».
То есть, дефисы удаляются, а все слова после них получают заглавную букву.
```
function camelsize(str){
	var arr = str.split('');
  for (var i=0; i<arr.length; i++){
  	if (arr[i] == "-"){
    	arr[i+1] = arr[i+1].toUpperCase();
    	arr.splice(i,1);
    }
  }
  var string = arr.join('')
  return string;
}

alert(camelsize ('-webkit-transition'));
```
