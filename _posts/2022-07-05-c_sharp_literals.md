---
title: "Литералы в C#"
layout: def
categories: c#
impMath: false
excerpt: Checkout
---

# {{ page.title }}

## Логические

- true
- false.

## Целочисленные

- 0, 1, -24, 213
- 0b11, 0b1010, 0b10001
- 0x01, 0xFF, 0x0A

## Вещественные

- 3.14 , 100.01 , -0.24
- 5.4e3, 3.5E-4 

## Символьные

```
Console.WriteLine('3'); // 3
Console.WriteLine('B'); // B
Console.WriteLine('N'); // N
Console.WriteLine('\n'); // перенос строки
Console.WriteLine('\t'); // табуляция
Console.WriteLine('\\'); // обратный слеш
Console.WriteLine('\x5A'); // Z из таблицы смиволов ASCII
Console.WriteLine('\u0420'); // P из таблицы Unicode
```

## Строковые

```
string text = "Пример строки";
string textWithText = $"Начало строки {text} Конец строки\n"; // {} -- это усы
// с помощью усов можно в строку добавлять что-угодно, для чего есть преобразование в строку
```

## null

Плейсхолдер для объектов
