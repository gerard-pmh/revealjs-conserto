# Les Frameworks JavaScript en 2017

---

# La gestion des dépendences en HTMTL

---

index.html
```html
<script src="script-1.js"></script>
<script src="script-2.js"></script>
<script src="script-3.js"></script>
```

---

script-1.js
```js
var myFramework = {
  doSomething: function() {
    return 'original function';
  }
};
```

script-2.js
```js
myFramework.doSomething = function() {
  return 'silently overrided function';
};
```

script-3.js
```js
myFramework.doSomething();
```

---

![Question Stack Overflow](img/stack-dep.png)

---

![Question Stack Overflow 2](img/stack-dep-2.png)

---

### Les avantages de de l'import via HTML
- Simple, mise en place rapide
- Supporté nativement par le navigateur

---

### Les inconvenients
- Le JavaScript "s'empile", résultats imprédictibles
- Complexe à gérer avec de grosses applications
