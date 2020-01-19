# Игра "Меню"

## 🌯 Купи свою шаурму.

<p>В разделе шаурмы будет <b>несколько подразделов</b> например: <b>соусы</b>, <b>наполнение</b> и т.д.</p>
<p>Вы можете выбрать ингридеенты, после чего нажать на кнопку и получить цену за вашу шаурму и количество колорий, содиржащихся в ней.</p>

## 🍺 Запей

<p>Потом вы можете купить напиток или несколько напитков. Разделы тоже есть.</p>
<p>Принцып колорий и цены тот же, что и с шаурмой.</p>

## Ближайшие обновления

### Меню

* Напитки
* Ингридеенты

### Подсчет

* Количество колорий
* Подсчёт стоимости заказа.

## Благодарности

* Исходный код на YouTube: https://www.youtube.com/watch?v=PjmMIngDj0c&list=PLM7wFzahDYnG-oMkclNX0FIcLZR18hFDM&index=5

## Созданное мной

* Новое меню
* CSS стили
* Подсчёт стоимости напитков
* Весь раздел <b>"Ближайшие обновления"</b>

## Скриншоты и объяснения 🤳🏻

### Пример напитков:

<img src="./immages/capture-20200119-162555.png">

### Покупка:

<img src="./immages/capture-20200119-164521.png">

<p>Вы можете увидеть, что лаваш выделен серой галачкой, потому что он обязателен. Он стоит <b>20 рублей</b></p>
<p>Допустим, вы выбрали сыр за <b>20 рублей</b>, салат за <b>50 рублей</b>, свиное мясо за <b>60 рублей</b>, а из соусов тартар за <b>20 руб</b> и кетчуп за <b>10 рублей.</b></p>
<p><b>Итого: 20 + 20 + 50 + 60 + 20 + 10 = 180 руб.</b></p>
<p>Далее вы просто нажимает на кнопку <b>"Счет"</b> и вам показывают количество колорий, параметры, которых вы можете найти в коде и цену шавермы, которую мы посчитали раньше.</p>
<p>Точно тоже самое происходит и с напитками</p>

## Код

### HTML

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Меню</title>
    <link rel="stylesheet" href="./css/style.css">
</head>
<style>
body {
    background: url(./immages/download.jpg);
    -moz-background-size: 100%;
    -webkid-background-size: 100%;
    -o-background-size: 100%;
    background-size: 100%;
    margin: 10px 720px 10px 720px;
    line-height: 20px;
    font-size: 25px;
    font-family: Arial, Helvetica, sans-serif;
}
</style>
<body style="background-attachment: fixed" topmargin="0">
    <table border="1" cellpadding="0" cellspacing="0" width="550" heigth="900" bgcolor="#ffffff">
    <th>
    <h1>Шаурма меню</h1>
    <p><input type="checkbox" checked disabled data-cost="20" data-kkal="75" class="menu">Лаваш     <font color="orange">(20руб)</font></p>
    <hr>
    <h2>Наполнение</h2>
    <p><input type="checkbox" checked data-cost="20" data-kkal="100" class="menu">Сыр     <font color="orange">(20руб)</font></p>
    <p><input type="checkbox" checked data-cost="50" data-kkal="50" class="menu">Салат     <font color="orange">(50руб)</font></p>
    <p><input type="checkbox" checked data-cost="60" data-kkal="210" class="menu">Свиное мясо     <font color="orange">(60руб)</font></p>
    <p><input type="checkbox" checked data-cost="80" data-kkal="180" class="menu">Куриное мясо     <font color="orange">(80руб)</font></p>
    <hr>    
    <h2>Соусы</h2>
    <p><input type="checkbox" checked data-cost="10" data-kkal="10" class="menu">Кетчуп     <font color="orange">(10руб)</font></p>
    <p><input type="checkbox" checked data-cost="20" data-kkal="12" class="menu">Тартар     <font color="orange">(20руб)</font></p>
    <p><input type="checkbox" checked data-cost="20" data-kkal="35" class="menu">Сычуанский соус     <font color="orange">(20руб)</font></p>
    <hr>
    <h3>Итого:</h3>
    <p>Калорийность: <span id="kkal"></span> Цена: <span id="cost"></span></p>
    <button id="result">Счет</button>
    <hr>
    <h1>Напитки</h1>
    <hr>
    <h2>Гозированные</h2>
    <p><input type="checkbox" checked data-costn="40" data-kkall="100" class="menun">Кока-кола холодная 0.33л.     <font color="orange">(40руб)</font></p>
    <p><input type="checkbox" checked data-costn="60" data-kkall="100" class="menun">Кока-кола 0.33л.    <font color="orange">(60руб)</font></p>
    <p><input type="checkbox" checked data-costn="50" data-kkall="90" class="menun">Мохито 0.33л.     <font color="orange">(50руб)</font></p>
    <p><input type="checkbox" checked data-costn="40" data-kkall="90" class="menun">Пепси 0.33л.     <font color="orange">(40руб)</font></p>
    <p><input type="checkbox" checked data-costn="30" data-kkall="75" class="menun">Лимонад 0.33л.     <font color="orange">(30руб)</font></p>
    <hr>
    <h2>Горячие</h2>
    <h3>Кофе</h3>
    <p><input type="checkbox" checked data-costn="300" data-kkall="300" class="menun">Капучино большой 0.3л.     <font color="orange">(300руб)</font></p>
    <p><input type="checkbox" checked data-costn="200" data-kkall="200" class="menun">Капучино средний 0.2л.     <font color="orange">(200руб)</font></p>
    <p><input type="checkbox" checked data-costn="100" data-kkall="100" class="menun">Капучино маленький 0.15л.     <font color="orange">(100руб)</font></p>
    <hr>
    <h3>Чай</h3>
    <p><input type="checkbox" checked data-costn="50" data-kkall="30" class="menun">Чай 0.15л.     <font color="orange">(50руб)</font></p>
    <hr>
    <h3>Итого:</h3>
    <p>Калорийность: <span id="kkall"></span> Цена: <span id="costn"></span></p>
    <button id="resultn">Счет</button>
    <p></p>
    </th>
    </table>
    <script src="./js/script.js"></script>
</body>
</html>

```

### JavaScript

```

document.getElementById('result').onclick = getResult;

function getResult() {
    var menu = document.getElementsByClassName('menu');
    var cost = 0;
    var kkal = 0;

    for (var i = 0; i < menu.length; i++) {
        if (menu[i].checked) {
            cost += parseFloat(menu[i].getAttribute('data-cost'));
            kkal += parseFloat(menu[i].getAttribute('data-kkal'));
        };
    }
    document.getElementById('cost').innerHTML = cost;
    document.getElementById('kkal').innerHTML = kkal;
};

document.getElementById('resultn').onclick = getCostN;

function getCostN() {
    var menun = document.getElementsByClassName('menun');
    var costn = 0;
    var kkall = 0;

    for (var i = 0; i < menun.length; i++) {
        if (menun[i].checked) {
            costn += parseFloat(menun[i].getAttribute('data-costn'));
            kkall += parseFloat(menun[i].getAttribute('data-kkall'));
        };
    }
    document.getElementById('costn').innerHTML = costn;
    document.getElementById('kkall').innerHTML = kkall;
};

```

### CSS

```

body {
    margin: 20px 720px 20px 720px;
    margin-bottom: 20px;
    line-height: 20px;
    font-size: 25px;
}

```