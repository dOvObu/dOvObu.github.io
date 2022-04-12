---
title: "Достаём закрытое"
layout: def
categories: unity
impMath: false
excerpt: Checkout
---

# {{ page.title }}

просто список всяких методов, которые можно дёрнуть через рефлексию

#### Как посмотреть internal поля ассета

у unity редактора есть режим разработчика в котором появляются  

```
UnityEditor.EditorPrefs.SetBool("DeveloperMode", true);
```

#### Как получить текстуру unity-вого атласа в editor-е?

```
public static Texture2D GetAtlasTexture(this Sprite sprite, SpriteAtlas atlas = null)
{
  if (atlas != null)
  {
    SpriteAtlasUtility.PackAtlases(new[] {atlas}, BuildTarget.Android);
  }
  
  var getActiveAtlasTexture = typeof(SpriteEditorExtension).GetMethod("GetActiveAtlasTexture", BindingFlags.Static | BindingFlags.Public | BindingFlags.NonPublic);
  return (Texture2D)getActiveAtlasTexture.Invoke(null, new[] {sprite});
}
```

можно так mip map bias менять, к примеру

![image](https://user-images.githubusercontent.com/43134602/162986748-446cd831-2f3c-41d7-8072-1bf22820912a.png)
![image](https://user-images.githubusercontent.com/43134602/162986769-6ea0bfc5-9172-40c6-b589-f646ba52abf2.png)

> вообще, mip map используется, чтоб зубцов на маленьких штуках не было

![no mipmaps](https://forum.unity.com/attachments/quad_nomips-gif.909044/)

