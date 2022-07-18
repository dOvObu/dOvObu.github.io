---
title: "Добавление gameObject-ов в Editor Mode и в Prefab Mode"
layout: def
categories: unity
impMath: true
excerpt: Checkout
---

# {{ page.title }}

Можно дёргать кнопки из пользовательского интерфейса unity через рефлексию

```
public static void AddStandard<T>(GameObject root) =>
  AppDomain.CurrentDomain.GetAssemblies()
    .First(asm => asm.GetName().Name.Equals("UnityEditor.UI")).DefinedTypes
    .First(type => type.Name.Equals("MenuOptions"))
    .GetMethod($"Add{nameof(T)}", BindingFlags.Public | BindingFlags.Static)
    ?.Invoke(null, new []{ new MenuCommand(root) });

```
