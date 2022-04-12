---
title: "Достаём закрытое"
layout: def
categories: unity
impMath: false
excerpt: Checkout
---

# {{ page.title }}

просто список всяких методов, которые можно дёрнуть через рефлексию

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
