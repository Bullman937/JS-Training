### 1.1) Alert
Вывести на страницу любую надпись
```
alert ("I'm JavaScript")
```

### 1.2) Work with variables
```
var admin;
var name;

name = "Василий";
admin = name;

alert (admin);
```

### 1.3) Simple page
Создать страницу, которая спрашивает имя и выводит его.
```
var name = prompt ("Ведите ваше имя", "Владислав");

alert ("Привет, " + name + "!")
```

### 1.4) Checking the standard
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

### 1.5) get the sign of a number
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

### 1.6) Login verification
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

### 1.7) Ternary operator
Простой пример с использованием "?"
```
var a = prompt ("Введите число А", '0');
var b = prompt ("Введите число B", '0');

result = (a + b < 4) ? "Мало" : "Много";

alert (result)
```

### 1.8) Login verification vith ternary operator
Проверка на корректность логина и пароля с помощью тернарного оператора
```
var login = prompt ("Введите ваш логин: ", '').toLowerCase();

var message = (login == "admin") ? "Привет!" :
	(login == "director") ? "Здравствуйте!" :
  (login == "") ? 'Необходимо ввести логин' :
  "Я тебя не знаю";

alert (message);
```