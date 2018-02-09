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