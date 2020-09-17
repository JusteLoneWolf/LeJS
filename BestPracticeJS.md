# Best Practice JS / NodeJS

# Les variable

Les variable sont stocké dans le cache de la ram donc ca devient vite consommateur en ram et qu'il faut soit les évité soit les limité

Dans un fichier de configuration nommé config.js (NodeJS) 
```js
module.exports ={
    personne1 :{
        nom :'Michel'
    },
    personne2 :{
        nom :'Gerard'
    } 
 }
```
Dans mon index.js
```js
const config = require('./config.js')

console.log(config)
/*
retourne :{
    personne1 :{
            nom :'Michel'
        },
        personne2 :{
            nom :'Gerard'
        } 
}
Donc tous cela est stocker dans la ram
*/

// et si je veux juste prendre la valeur nom de personne1 on doit faire
console.log(config.personne1.nom) // retourne michelle

// Mais le mieux faire dans ce cas la seras plutot de faire

const {personne1} = require('./config.js')

console.log(personne1)

/*
retourne :{
    personne1 :{
            nom :'Michel'
        },
}
Donc la seulement le contenue de personne1 est stocker et ca prendre deux fois moins de place sur la ram
*/

// et pour prendre la valeur nom il faudrat juste faire

console.log(personne1.nom) // retourne michelle
```

Evite les variable inutile 
```js
// Mauvais
let hello = "hello"
console.log(hello)

// Bon 
console.log('hello')
```

## Boucle

- forEach
La boucle forEach est equivalent au for...of
```js
const array1 = ['a', 'b', 'c'];
array1.forEach(element =>{
console.log(element)// retourne a,b,c
})
// Mais préféré l'utilisation de la boucle for...of elle seras plus rapide sur de plus grosse donnée et moins consommateur niveau ram et cpu
for (const element of array1) {
  console.log(element); // retourne a,b,c
}
```
