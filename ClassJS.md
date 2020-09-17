# Classe en javascript

### Documentation

[MDN](https://developer.mozilla.org/fr/docs/Apprendre/JavaScript), [WSCHOOL](https://www.w3schools.com/js/default.asp)

 ---
 
 ## Une classe simple 

- Une classe va permettre de crée des objet et cette objet seras composé de variable et de fonction, on peu aussi utilisé la class pour rassemble des fonction

```js
class MaClasse {
  name = 'Shela'
    get(){
    return this.name // retourne Shela
    }   
}

let obj = new MaClasse() //on initialise MaClasse
console.log(obj.get()) // on appelle la fonction get de la class MaClass
```

## La Class constructor

### Contrutor simple

- Cette est la meme chose que la classe simple mais on peu injecté des valeur dedant

```js
class MaClass {
  constructor(name) {
        this.name = name
    }
    monnom(){
        return this.name
    }

}

let obj = new MaClass("Michelle")

console.log(obj.monnom()) // va retourne Michelle
```

### Constructor "Static"

- C'ets la meme chose qu'un constructor simple mais on peux faire avec des variable fix mais c'est variable peuvent etre appellé dans n'importe quelle endroit

```js
class MaClass {
  constructor({name: '',age:'', }) {
        this.name = name
        this.age = age
    }
    getnom(){
        return this.name
    }
    getage(){
        return this.age
    }   


}

let obj = new MaClass({age:14,name:'Angella'})

console.log(obj.getnom()) // va retourne Michelle
```