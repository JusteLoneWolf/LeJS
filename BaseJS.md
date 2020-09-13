# IJVS010

### Documentation

----

[MDN](https://developer.mozilla.org/fr/docs/Apprendre/JavaScript), [WSCHOOL](https://www.w3schools.com/js/default.asp)

### let, const, var

---
- let peux être utilisé partout dans un bloc mais une fois sorti d'un bloc il seras plus defini mais il peu etre reassigné
    
```js
      let hello = 'hello'
      console.log(hello) // retourne hello
      hello = 'bonjour' 
      console.log(hello) // retourne bonjour
      let hello = "salut" //retourne une erreur (hello is already defined)
      console.log(hello) 
```
 - const peux être utilisé partout dans un bloc mais une fois sorti d'un bloc il seras plus defini mais il ne peux pas etre vide ni reassigné
 ```js
        const hello = 'hello'
        console.log(hello) // retourne hello
        hello = 'bonjour' // retourne hello
        console.log(hello) // error 
```

- var comme let mais beaucoup plus borderline 

```js
        var hello = "bonjour"
        console.log(hello) // retourne hello
        hello = "Hola"
        console.log(hello) // retourne hello
        var hello = "salut"
        console.log(hello) //retourne salut
```

### Condition

- #### If & if....else & if....else if

```js
let x = 1

if(x ===1){
    console.log("x est egale a 1")
}

if(x === 10){
    console.log("x est egale a 10")
}else {
    console.log("x n'est pas egale a 10")
}

if(x ===10){
    console.log("x est egale a 10")
}else if (x === 1){
    console.log("x est egale a 1")
}else{
    console.log("x n'est pas egale a 10 ni a 1")
}
```

- Switch...case...default

```js
let x = 10

switch (x) {
    case "1":
        console.log("x est egale a 1")
        break
    case "10":
        console.log("x est egale a 10")
        break
    default:
    //s'execute si aucune des condition n'est remplit
    console.log("x n'est pas egale a 1 ni a 10")
}
```