---
title: "Переменные и константы в C#"
layout: def
categories: c#
impMath: false
excerpt: Checkout
---

# {{ page.title }}

## Переменные

Определяются так:

```
тип имя;
```

Потом можно им присваивать значения сколь угодно раз:

```
string name;

name = "Tom";
Console.WriteLine(name);

name = "Jack";
Console.WriteLine(name);

name = "Boris";
Console.WriteLine(name);
```

Можно присвоить сразу (проинициализировать):

```
string name = "Tom";
```

## Константы

Константы как переменные, но их можно только проинициализировать:

```
string NAME = "Tom";
// NAME = "Jack"; уже написать нельзя
```
