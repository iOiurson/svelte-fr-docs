---
title: Évènements DOM
---

Nous avons déjà rapidement évoqué qu'il était possible d'écouter n'importe quel évènement sur un élément avec la directive `on:` :

```html
<div on:mousemove={handleMousemove}>
	Le curseur se trouve à la position ({m.x} ; {m.y})
</div>
```
