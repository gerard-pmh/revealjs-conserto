# Les Frameworks JavaScript en 2017

---

# Classic Script

---

my-framework.js
```js
var myFramework = {
  doSomething: function() {
    // ...
  }
};
```

main.js
```js
myFramework.doSomething();
```

index.html
```html
<script src="my-framework.js"></script>
<script src="main.js"></script>
```

---

![Question Stack Overflow](img/stack-dep.png)

---

![Question Stack Overflow 2](img/stack-dep-2.png)

---

### Avantages
- Simple, mise en place rapide
- Supporté nativement par les navigateurs
- Possibilité d'utiliser des Content Delivery Network (CDN)

---

### Inconvénients
- "Pollution" du scope global
- Complexe avec beaucoup de composants / dépendances

---

# Les Modules ES2015

---

my-framework.js
```js
export const myFramework = {
  doSomething() {
    // ...
  }
};
```

main.js
```js
import { myFramework } from './my-framework';

myFramework.doSomething();
```

---

index.html
```html
<script src="bundle.js"></script>
```

```bash
npm install -g rollup
rollup main.js --format iife --output bundle.js
```

---

bundle.js
```js
(function () {
'use strict';

const myFramework = {
  doSomething() {
    // ...
  }
};

myFramework.doSomething();

}());
```

---

### Avantages
- Chaque module a son propre scope, seul les variables exportées sont visibles par les autres modules et nécessitent un import explicite
- Facilite la construction d'applications complexes

---

### Inconvénients
- Support partiel par les navigateurs
- Utilisation des CDN difficile

---

![Google 1](img/google-dep.png)
![Google 2](img/google-es6-module.png)
