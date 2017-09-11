![js logo](img/js-logo.png)  <!-- .element height="30%" width="30%" -->
## Le développement d'applications JavaScript Front-End en 2017

---

![all logo](img/all-logo.png)  <!-- .element height="80%" width="80%" --->

---

### L'outillage front-end moderne

- Gestion des dépendances
- Transcompilation (traduction d'un language vers un autre)
- Compatibilité avec les différents navigateurs
    - polyfill
    - autoprefixer
- Analyse statique de code (linting)
- Automatisation des tests unitaires et d'intégration
- Assemblage, optimisation, compression et obfuscation du code
- Serveur de développement avec "live reload"

---

![javascript guy](img/javascript-guy.jpg)

---

### Node.js

- Environnement d'exécution JavaScript en dehors du navigateur
- Basé sur le moteur V8 utilisé par Google Chrome
- Utilisé pour le développement JavaScript côté serveur
- Mais aussi pour l'outillage de développement front-end

![node.js logo](img/nodejs-logo.png)  <!-- .element height="30%" width="30%" -->

---

### NPM - Node Package Manager

- Gestionnaire de paquets officiel de Node.js
- Environ 500 000 packets disponibles

![npm logo](img/npm-logo.png)  <!-- .element height="30%" width="30%" -->

---

### ECMAScript 2015 (ES6)

- Norme sur laquelle est basée le language JavaScript
- Apporte de nombreux ajouts au language
- En cours d'implementation dans les navigateurs
- Peut être utilisé dès aujourd'hui avec :
    - Babel (transpiler)
    - Webpack (module bundler)

![babel logo](img/babel-logo.png)  <!-- .element height="30%" width="30%" -->
![webpack logo](img/webpack-logo.png)  <!-- .element height="20%" width="20%" -->

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
[ 'example.fr', 'example.com' ].filter(function (x) {
    return x.endsWith('.fr');
}); // [ 'example.fr' ]
```

```js
[ 'example.fr', 'example.com' ].filter(x => x.endsWith('.fr'));
// [ 'example.fr' ]
```

---

### ECMAScript 2015
### Destructuring - Template Strings

```js
const user = { name: 'John', mail: 'john@mail.com', age: 30 };

function oldHello(user) {
    console.log(
        'Hello ' + user.name + ', you are ' + user.age + ' years old !'
    );
}

function hello({ name, age }) {
    console.log(`Hello ${name}, you are ${age} years old !`);
}

hello(user); // Hello John, you are 30 years old !
```

---

### ECMAScript 2015 - Spread Operator

```js
const obj1 = { a: 1, b: 2 };

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
- Typage statique et facultatif
- Annotations
- Compatible avec du code JavaScript standard
- Améliore grandement la compréhension du code par l'IDE

![ts logo](img/ts-logo.png) <!-- .element height="15%" width="15%" -->

---

![typescript adds types](img/typescript-adds-types.jpg)

---

### TypeScript - Exemple

```typescript
interface Example {
    prop1: string,
    prop2: number
    // optional field
    prop3?: boolean
}

const example: Example = {
  prop1: 'test',
  prop2: 2,
};

function getExample(): Example {
  return { prop1: 'test', prop2: 2 };
}
```

---

![js 2010 vs 2016](img/js-2010-vs-2016.jpg) <!-- .element height="60%" width="60%" -->

---

### les "CLI" - Command Line Utilities

Standardisent et facilitent l'initialisation et l'utilisation de l'outillage

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
npm start

# Construction avec optimisations
npm run build
```

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

### Présentation des Frameworks / Bibliothèques

![angular logo](img/angular-logo.png) <!-- .element height="30%" width="30%" -->
![react logo](img/react-logo.png) <!-- .element height="30%" width="30%" -->
![vue logo](img/vue-logo.png) <!-- .element height="30%" width="30%" -->

---

### Angular

- Framework développé par Google
- Disponible en version stable depuis Septembre 2016
- Réécriture totale d'AngularJS
- Supporte officiellement, recommande, et est écrit avec TypeScript
- Injection de dépendance (singleton)
- Programmation fonctionnelle réactive avec RxJS

![angular logo](img/angular-logo.png) <!-- .element height="20%" width="20%" -->

---

### React

- Bibliothèque développée par Facebook
- Disponible depuis Mars 2013
- Gère la partie "vue" d'une application front-end
- Est utilisé avec d'autres librairies :
    - react-router
    - redux
- Utilise JSX, une extension du language JavaScript permettant de générer du HTML

![react logo](img/react-logo.png) <!-- .element height="20%" width="20%" -->

---

### Vue

- Bibliothèque créée par Evan You, ancien membre de l'équipe AngularJS
- Disponible depuis Février 2014
- Gère la partie "vue" d'une application front-end
- Est utilisé avec des librairies officiellement supportées :
    - vue-router
    - vuex
- Syntaxe particulièrement simple

![vue logo](img/vue-logo.png) <!-- .element height="20%" width="20%" -->

---

### Component Based Architecture

Constitution d'un composant :
- Propriétés / Etat
- Template / Fonction de rendu
- Méthodes
- Fiche de style

---

### Component Based Architecture

Un composant peut :
- Passer des propriétés à ses composants enfants
- Emettre / Recevoir des événements

---

### Component Based Architecture

![cba diagram](img/cba-diagram.png) <!-- .element height="70%" width="70%" -->

source: http://coenraets.org/blog/2014/12/sample-mobile-application-with-react-and-cordova/

---

### Exemple - Angular

hello.component.ts
```typescript
import { Component, Input } from '@angular/core';

@Component({
 selector: 'app-hello',
 template: `
   <div>
      Hello, {{ userName }} !
   </div>
   ` 
})
export class HelloComponent {
  @Input() userName: string;
}
```

```html
<app-hello [userName]="Angular"></app-hello>
```

Hello, Angular !

---

### Exemple - React

HelloComponent.js
```js
import React from 'react';

export default function HelloComponent (props) {
    return (
        <div>
            Hello, {props.userName} !
        </div>
    );
}
```

```js
<HelloComponent userName="React" />
```

Hello, React !

---

### Exemple - Vue

HelloComponent.vue
```html
<template>
    <div>
        Hello, {{ userName }} !    
    </div>
</template>
<script>
    export default {
        props: [ 'userName' ]
    }
</script>
```

```html
<hello-component :userName="vue"></hello-component>
``` 

Hello, Vue !

---

### Exemple - Compteur

![example counter](img/example-counter.png)

---

### Exemple - Angular

```typescript
import { Component } from '@angular/core';

@Component({
 selector: 'app-counter',
 template: `
   <div>
      {{ count }}
      <button (click)="add()">ADD</button>
   </div>
   ` 
})
export class HelloComponent {
  count = 0;
  add() {
    this.count = this.count + 1;
  }
}
```

---

### Exemple - React

```js
import React from 'react';

export default class CounterComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = { count: 0 };
    }
    add() {
        this.setState({ count: this.state.count + 1 });
    }
    render() {
        return (
          <div>
             {this.state.count}
             <button onClick={this.add}>ADD</button>
          </div>
        );
    }
}
```

---

### Exemple - Vue

```html
<template>
    <div>
        {{ count }}   
        <button @click="add">ADD</button>
    </div>
</template>
<script>
    export default {
        data() {
           return { count: 0 }
        },
        methods: {
            add() { 
                this.count = this.count + 1
            }
        }
    }
</script>
```

---

![angular logo](img/angular-logo.png) <!-- .element height="30%" width="30%" -->
![react logo](img/react-logo.png) <!-- .element height="30%" width="30%" -->
![vue logo](img/vue-logo.png) <!-- .element height="30%" width="30%" -->

---

![js logo](img/js-logo.png)  <!-- .element height="30%" width="30%" -->
## Questions ?
