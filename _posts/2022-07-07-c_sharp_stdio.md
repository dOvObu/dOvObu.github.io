---
title: "Консольный ввод/вывод в C#"
layout: def
categories: c#
impMath: false
excerpt: Checkout
---

# {{ page.title }}

```
Console.WriteLine("Текст с переносом строки");
Console.Write("Текст без переноса строки");
Console.WriteLine("-----------");
Console.Write("Введи текст: ");
string text = Console.ReadLine(); // Из консоли читается именно текст
Console.WriteLine("Вы ввели " + text);
Console.WriteLine($"Вы ввели {text}");
Console.WriteLine("Я написал число {1}, а вы ввели {0}", text, 42);
```

Допустим, в консоль хотелось бы вводить целое число, или число с плавающей точкой.

Тогда нужно прочитать строку с числом, а потом преобразовать её к нужному типу данных.

```
int num = Convert.ToInt32("42");
double weight = Convert.ToDouble("1,82"); // символ разделителя целых и десятичных устанавливается вместе с системным языком
double height = Double.Parse("1.82", CultureInfo.InvariantCulture); // но так можно жёстко привязаться к точке
decimal pi Convert.ToDecimal("3,1415926535898");
```
