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

![image](https://user-images.githubusercontent.com/43134602/162963619-952e8691-6dd3-4e12-ab5f-ca40a26623ab.png)
![image](https://user-images.githubusercontent.com/43134602/162963669-ff2d9a1e-44b8-49de-9320-39f8be9a7588.png)

может понадобиться, чтоб зубцов на маленьких штуках не было

![no mipmaps](https://forum.unity.com/attachments/quad_nomips-gif.909044/)


