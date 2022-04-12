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

в unity редакторе есть режим разработчика

```
UnityEditor.EditorPrefs.SetBool("DeveloperMode", true);
```

![image](https://user-images.githubusercontent.com/43134602/162987344-163a0bf3-fd8d-49e3-9339-b8ebae0d6cf8.png)

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

можно так mip map bias менять (чем выше, тем более размыто)

> вообще, mip map используется, чтоб зубцов на маленьких штуках не было
![no mipmaps](https://forum.unity.com/attachments/quad_nomips-gif.909044/)

