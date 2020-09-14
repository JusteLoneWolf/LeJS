# IJVS010

### Documentation

[MDN](https://developer.mozilla.org/fr/docs/Apprendre/JavaScript), [WSCHOOL](https://www.w3schools.com/js/default.asp)

### Variable

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
        hello = 'bonjour'
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

### Operateur

== egale a
```js
let x = 5

x == 5 //true
```
=== egale a et egale au type
```js
let x = 5

x === 5 //true
x === '5' // false
```

!= pas egale
```js
let x = 5

x != 6 //true
```

!== pas egale et pas le meme type
```js
let x = 5

x !== 5 //false
x !== 6 //true
x !== '5' // true
```

\> plus grand que
```js
let x = 5

x > 7 // false
```

\< plus petit que
```js
let x = 5
x < 7 //true
```

\>= plus grand ou egale
```js
let x = 5

x >= 5 //false
```
\<= plus petit ou egale
```js
let x = 5

x <= 7 //true
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

### Structure des donnée

#### Objet

```js
let objet = {animal : "dog"}

console.log(objet) // return {animal : "dog}
console.log(objet.animal) // retourne dog
```

#### Array
````js
let array = ["a","b","c"]

console.log(array) // retourne ["a","b","c"]
console.log(array[0]) //retourne a
````

#### Melange

```js
let melange = [{animal : "dog"},{animal : "cat"}]

console.log(melange) //retoune [{animal : "dog"},{animal : "cat"}]

console.log(melange[0]) // retourne {animal : "dog"}
console.log(melange[0].animal) // retourne dog

```

### Boucle

- for, while

```js
for (let i = 0; 0 <i;i++){
console.log(i) // retourne 1,2,3,4,5,6,7,8,9,10,
}

let i = 0
while (0<i){
i++
console.log(i) // retourne 1,2,3,4,5,6,7,8,9,10,
}
```

- for of... for in

```js
const array1 = ['a', 'b', 'c'];

for (const element of array1) {
  console.log(element); // retourne a,b,c
}

const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`); //retoune "a: 1" "b: 2" "c: 3"

}
```


### Methode
- typeof permet de voir quel est le type de variable
```js
let string = "salut"

console.log(typeof string) // retourne String
```

```js
let string = "salut"

console.log(string.toUpperCase()) // returne SALUT
let UpperString = "SALUT"

console.log(UpperString.toLowerCase()) // retourne  salut
```

### Fonction
```js
function hello() {
  console.log("salut")
}

hello() // retourne salut


function hello2(text) {
  console.log(text)
}

hello2("Hello") // retourne Hello

function hello3(text) {
  return text
}

console.log(hello3('Hey')) // retourne hey

function hello4(text = "Salut") { //si text n'est pas definit la valeur par defaut seras Salut
  return text
}

console.log(hello4('Hey')) // retourne hey
console.log(hello4()) // retourne Salut
```