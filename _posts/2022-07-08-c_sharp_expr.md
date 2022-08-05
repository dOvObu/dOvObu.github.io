---
title: "Операции"
layout: def
categories: c#
impMath: false
excerpt: Checkout
---

# {{ page.title }}

## С цифрами

сложение, вычитание, умножение, деление

```
Console.WriteLine(1 + 1); // 2
Console.WriteLine(1 - 1); // 0
Console.WriteLine(2 * 2); // 4

int a = 10;
int b = a / 3;
Console.WriteLine(a); // 3

float c = 10f;
float d = c / 3f;
Console.WriteLine(d); // 3.333333
```

остаток от целочисленного деления

```
Console.WriteLine(3  % 2); // 1
Console.WriteLine(10 % 4); // 2
```

инкремент

```
int i = 0;
int j = ++i;
Console.WriteLine($"{i}, {j}"); // 1, 1

i = 0;
j = i++;
Console.WriteLine($"{i}, {j}"); // 1, 0
```

дикремент

```
int i = 0;
int j = --i;
Console.WriteLine($"{i}, {j}"); // -1, -1

i = 0;
j = i--;
Console.WriteLine($"{i}, {j}"); // -1, 0
```

## Побитовые

и, или, отрицание или (xor), отрицание, сдвиги влево и вправо

```
Console.WriteLine(0b010 & 0b101); // 0
Console.WriteLine(0b010 | 0b101); // 7, т.к. это 0b111
Console.WriteLine(0b111 ^ 0b010); // 0, т.к. 0b000111 ^ 0b000010 это 0b000111, а побитовое отрицание этого эт 0b11111111111111111111111111111000
// xor может использоваться как дешманский способ шифрования
int key = 2;
int encrypted = 7 ^ key;
Console.WriteLine(encrypted ^ key); // 7
Console.WriteLine(~0b101); // -6, т.к. это 0b11111111111111111111111111111010
Console.WriteLine(0b0111 << 1); // 14, т.к. это 0b1110
Console.WriteLine(0b0100 >> 2); // 1, т.к. это 0b0001
```

Побитовые сдвиги, по сути, работают как умножение, либо деление на 2 несколько раз.


## С присвоением

Для всех операций описанных выше, кроме инкримента, дикремента и отрицания, есть опирации с присвоением

```
int i = 2;
i += 5; // это буквально значит i = i + 5 , но пишется немного короче
Console.WriteLine(i); // 7
i &= 6;
i >>= 1;
Console.WriteLine(i); // 3
```

## С логикой

Можно числа друг с другом сравнивать и получать true либо false

```
Console.WriteLine($"{42 < 24}, {42 > 24}"); // false, true
Console.WriteLine(0 <= 0); // true, потому что 0 равен 0
Console.WriteLine(0 <= 10); // true
Console.WriteLine(0 >= 10); // false
Console.WriteLine(0 >= -10); // true
```

Можно сравнивать вообще практически что угодно, равны ли друг другу объекты одинакового типа или не равны:

```
Console.WriteLine("dsakldas" == null); // false
Console.WriteLine("dajdw" == "dajdw"); // true
Console.WriteLine(3254 != 6452); // false, потому что эти числа действительно друг другу не равны
Console.WriteLine("asdjkl" != null); // true
```

Из логических утверждений можно составлять ещё большие утверждения, с помощью логических операторов **и**, **или** и **не**

```
Console.WriteLine(false && false); // false
Console.WriteLine(true && false); // false
Console.WriteLine(true && true); // true

Console.WriteLine(false || false); // false
Console.WriteLine(true || false); // true
Console.WriteLine(true || true); // true

Console.WriteLine(!true); // false
Console.WriteLine(!false); // true
```

Примечательно, что логические операторы **и** и **или** -- линивые, т.е. если выражение перед **и** даст false, либо выражение перед **или** даст true, то вторая часть выражения вычисляться не будет.
