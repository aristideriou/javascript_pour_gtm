# javascript_pour_gtm

## Chapitre 5 : Déclaration de variables

```javascript
var myBoolean = true;
var myInteger = 27;
var myFloat = 32.4;
var myString = 'hello World';
console.log(myFloat);
typeof(myInteger);
typeof(myString);
myInteger.toString();
Number('4');
typeof(Number('4'));
```

## Chapitre 6 : Focus sur les tableaux et objets

```javascript
var myArray = ['product1','product3','product546'];
myArray[1]; //renvoie 'product3'
myArray[2] = 'newproduct' ; //modifie le 3ème élément de l'array

var myArray = ['aa','bbb'];
typeof myArray; 
Array.isArray(myArray);

var user = {
	'firstName' : 'Michel',
	'lastName' : 'Dupont',
	'age' : 30,
	'isClient' : false
};

user.firstName; //renvoie 'Michel'
user.lastName = 'Dubois'; //modifie la valeur de la clé lastName à la volée
user.country = 'Spain'; //ajoute une clé 'country' avec une valeur 'Spain'

var products = [
{
'id' : 432342,
'name' : 'Baskets Nike',
'size' : 43,
'price' : 132
},
{
'id' : 88643,
'name' : 'iPhone 22',
'size' : 512,
'price' : 4000
},
]
```

## Chapitre 7 : Utiliser des méthodes : exemples avec des tableaux et Math.

```javascript
var myArray = ['product1','product3','product546'];
myArray.push('product4');
myArray.pop('product4');

window.document.location.hostname
window.document.location.pathname

Math.round(2.24)

Math.random()

Math.random()*1000

Math.abs(-18)

```

## Chapitre 8 : Factoriser son code avec des fonctions

```javascript

function logStuffToConsole() {
	console.log('Bonjour à tous!');
}

//La fonction en elle-même est, pour l'heure, juste déclarée, mais pas appelée

logStuffToConsole();
//On appelle ensuite la fonction pour afficher le message dans la console

function logStuffToConsole(utilisateur) {
	console.log('Bonjour ' + utilisateur + ' et bienvenue!');
}

logStuffToConsole('Paul Dupont');

function multiplyBy42(userNumber) {
	return userNumber*42;
}

var myMultipliedNumber = multiplyBy42(24);
//Devrait retourner 1008 si tout se passe bien

(function () {
  console.log('Je vais être exécuté!');
})();

```

## Chapitre 9 : Les structures de boucles (if / else, switch, while…)

```javascript
var firstNumber = 17;

if ( firstNumber > 12){
	console.log('le nombre est supérieur à 12!');
}

if ( firstNumber > 17){
	console.log('le nombre est strictement supérieur à 17!');
}
else {
	console.log('le nombre n'est pas strictement supérieur à 17...');
}

if ( firstNumber > 17){
	console.log('le nombre est strictement supérieur à 17!');
}
else if ( firstNumber < 17 ) {
	console.log('le nombre est strictement inférieur à 17...');
}
else {
	console.log('le nombre doit être exactement égal à 17');
}

laxistTest = firstNumber == otherNumber; //renvoie true
laxistTest = firstNumber === otherNumber; //renvoie false

var myNumber = 17;
var myOtherNumber = 12;

if(myNumber > 12 && myOtherNumber > 12){
	console.log('Mes deux nombres sont supérieurs à 12');
}

if(myNumber > 15 || myOtherNumber > 15){
	console.log('Au moins un des deux nombres est supérieur à 15');
}

var myNumber = 17;
var control = 0;

if(myNumber > 12){
	control = 1;
}
else{
	control = 2;
}
//Un peu long à écrire, non?

myNumber > 12 ? control = 1 : control = 2;
//Ecriture équivalente avec un ternaire

var myArray = ['riri','fifi','loulou'];

for (var i = 0; i < myArray.length; i++) {
	console.log(myArray[i]);
}

var product = {
	'id' : 432342,
	'name' : 'Baskets Nike',
	'size' : 43,
	'price' : 132
}

for (var item in product){
	console.log(item);
	console.log(products[item]);
}
```

## Chapitre 10 : La manipulation du DOM

```javascript

document.querySelector("#content > div.editorial-feed-zone.light.lg\\:mt-10 > div > div:nth-child(1) > div > div.common-container.flex-1.pt-5.lg\\:ml-5.lg\\:py-0 > div > div > div:nth-child(3) > div > a > div.flex.flex-col.justify-between.relative.ml-3 > div:nth-child(1) > div.mt-1 > h3")

document.querySelectorAll('div')
```

## Chapitre 12 : Les event listeners 

```javascript
function headerClick(){
	console.log('Click on header');
}
//On commence par déclarer la fonction qui sera appelée lors de l'action utilisateur, mais pour l'instant, elle n'est pas appelée
 
var headerSelector = document.querySelector('#header > div > .');
//On met notre sélecteur dans une variable

headerSelector.addEventListener('click',headerClick);
//On "attache" notre fonction "headerClick" à l'action de clic sur l'élément concerné par notre sélecteur CSS
```

## Chapitre 13 : Cookies et local storage 

```javascript

document.cookie = "username=Michel Michel; expires=Thu, 18 Dec 2022 12:00:00 UTC; path=/";

localStorage.setItem('userId', '123456');
//Créer une entrée de local storage

var cat = localStorage.getItem('userId');
//Récupérer une entrée de local storage

localStorage.removeItem('userId');
//Supprimer une entrée de local storage

```
