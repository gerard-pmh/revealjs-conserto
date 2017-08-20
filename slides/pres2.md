### Le développement d'applications JavaScript Front-End en 2017

---

### Node.js

- Environnement d'exécution JavaScript en dehors du navigateur
- Basé sur le moteur V8 utilisé par Google Chrome
- Utilisé pour le développement JavaScript côté serveur
- Mais aussi pour l'outillage de développement front-end

---

### NPM - Node Package Manager

- Gestionnaire de paquets officiel de Node.js
- ~ 500 000 packets disponibles

---

### L'outillage front-end moderne

- Gestion des dépendances
- Transcompilation (Traduction d'un programme d'un language vers un autre)
- Compatibilité avec les différents navigateurs (polyfills, autoprefixer)
- Analyse statique de code ("linting")
- Automatisation des tests unitaires et d'intégration
- Assemblage, optimisation, compression et obfuscation du code
- Serveur de développement avec "live reload"

---

### ECMAScript 2015

- Norme sur laquelle est basée le language JavaScript
- Apporte de nombreux ajouts au language
- En cours d'implementation dans les navigateurs
- Peut être utilisé dès aujourd'hui avec Babel

---

### ECMAScript 2015 - let and const

```js
if (condition) {
    var varExample = 'example';
    let letExample = 'example';
}
console.log(varExample); // depends on condition
console.log(letExample); // always undefined

const constExample = 'example';
constExample = 'example2'; // error
```

---

### ECMAScript 2015 - Modules

framework.js
```js
export const framework = {
    doSomething() {
        // ...
    }
}
```

app.js
```js
import { framework } from 'framework.js';

framework.doSomething();
```

---

### ECMAScript 2015 - Classes

framework.js
```js
export class Framework {
    property;
    
    constructor(property) {
        this.property = property;
    }
    
    doSomething() {
        // ...
    }  
}
```

app.js
```js
import { Framework } from 'framework.js';

const framework = new Framework('example');

framework.doSomething();
```

---

### ECMAScript 2015 - Arrow Functions

```js
[ 1, 2, 3 ].filter(function (x) {
    return x > 1;
}); // [ 2, 3 ]
```

```js
[ 1, 2, 3 ].filter(x => x > 1); // [ 2, 3 ]
```

---

### ECMAScript 2015 - Destructuring

```js
const [ a, b, c ] = [ 1, 2 ,3 ];

console.log(b) // 2
```

---

### ECMAScript 2015 - Spread Operator

```js
const obj1 = { a: 1, b: 2};

const obj2 = { ...obj1, c: 3 } // { a: 1, b: 2, c: 3 }
```

---

### ECMAScript 2015 - Default Parameters

```js
function example(a = 'default parameter') {
    console.log(a);
}

example(); // 'default parameter'
```

---

### TypeScript

- Language de programmation libre et open source développé par Microsoft
- Basé sur ES2015
- Système de typage statique et facultatif
- Compatible avec du code JavaScript standard
- Améliore grandement la compréhension du code par l'IDE

---

### TypeScript - Exemple

```typescript
interface Example {
    prop1: string,
    prop2: number
    prop3?: boolean
}

const example: Example = {
  prop1: 'test',
  prop2: 2,
};
```

---

### Webpack - Module Bundler

- Gère principalement l'assemblage des dépendances et modules
- Rôle central dans l'outillage front-end

(image du site webpack)

---

### les "CLI" - Command Line Utilities

Standardisent et facilite l'initialisation et l'utilisation de l'outillage

---

### Vue CLI

```bash
# Installation global du CLI
npm install --global vue-cli

# Initialisation du projet
vue init webpack my-app

cd my-app

# Installation des dépendances
npm install

# Serveur de développement
npm run dev

# Construction avec optimisations
npm run build
```

---

### Angular CLI

```bash
# Installation global du CLI
npm install --global @angular/cli

# Initialisation du projet et installation des dépendances
ng new my-app

cd my-app

# Serveur de développement
ng serve

# Construction avec optimisations
ng build
```

---

### Create React App

```bash
# Installation global du CLI
npm install --global create-react-app

# Initialisation du projet et installation des dépendances
create-react-app my-app

cd my-app

# Serveur de développement
ng start

# Construction avec optimisations
npm run build
```

---

### Présentation des Frameworks / Bibliothèques

- React
- Angular
- Vue

---

### React

- Bibliothèque développée par Facebook depuis 2013
- Gère la partie "vue" d'une application front-end
- Combiné à d'autres librairies ...

---

### l'architecture en composants

un composant est constitué
- d'un template
- d'une fiche de style
- de propriétés
- d'un etat
- de methodes pouvant être appellées depuis le template
il peut emettre des evenements à son composant parents,
et passer des propriétés à ses composants enfants

---

### exemples

- vue
- react
- angular

---

### support desktop et mobile
