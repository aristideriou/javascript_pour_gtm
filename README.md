# javascript_pour_gtm

## Chapitre 4 : Déclaration de variables

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

var myOtherInteger = 10;
var myOtherString = 'Welcome';

console.log(myInteger + myOtherInteger);
console.log(myInteger + myOtherString);
```

## Chapitre 5 : Focus sur les tableaux et objets

```javascript
var myArray = ['product1','product3','product546'];
myArray[1]; //renvoie 'product3'
myArray[2] = 'newproduct' ; //modifie le 3ème élément de l'array

var myArray = ['product1','product3','product546'];
myArray.push('product4');
myArray.pop();

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

## Chapitre 6 : Méthodes et propriétés - Exemples avec des Math et window.document.

```javascript
var pi = Math.PI;
console.log(pi); // Affiche la valeur de PI : 3.141592653589793

var nombreArrondi = Math.round(4.7);
console.log(nombreArrondi); // Affiche : 5

var nombreInferieur = Math.floor(4.7);
console.log(nombreInferieur); // Affiche : 4

var nombreAleatoire = Math.random();
console.log(nombreAleatoire); // Affiche un nombre aléatoire entre 0 et 1

var url = window.document.location.href;
console.log(url); // Affiche l'URL complète de la page

var nomHote = window.document.location.hostname;
console.log(nomHote); // Affiche le nom de domaine de la page
```

## Chapitre 7 : Factoriser son code avec des fonctions

```javascript

//Déclaration d'une fonction simple sans paramètre et affichage d'un message
function direBonjour() {
    console.log("Bonjour !");
}
direBonjour(); // Appel de la fonction, affiche : Bonjour !

//Déclaration d'une fonction avec des paramètres et affichage d'un message personnalisé
function saluer(prenom) {
    console.log("Bonjour, " + prenom + " !");
}
saluer("Alice"); // Appel de la fonction, affiche : Bonjour, Alice !

//Déclaration d'une fonction qui retourne une valeur
function additionner(a, b) {
    return a + b;
}
var somme = additionner(3, 4);
console.log(somme); // Affiche : 7

// Déclaration et exécution immédiate d'une fonction anonyme
(function() {
    console.log("Ceci est une IIFE !");
})(); // Affiche : Ceci est une IIFE !

```

## Chapitre 8 : Les structures de boucles (if / else, switch, while…)

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

var laxistTest = firstNumber == otherNumber; //renvoie true
var strictTest = firstNumber === otherNumber; //renvoie false

var myNumber = 17;
var myOtherNumber = 12;

if(myNumber > 12 && myOtherNumber > 12){
	console.log('Mes deux nombres sont supérieurs à 12');
}

if(myNumber > 15 || myOtherNumber > 15){
	console.log('Au moins un des deux nombres est supérieur à 15');
}

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

```

## Chapitre 9 : Manipulation du DOM et event listeners

```javascript

/*
<div id="maDivAnimee" style="width: 100px; height: 100px; background-color: blue; transition: width 2s;"></div>
<button id="animerDiv">Animer la div</button>
*/

document.getElementById('animerDiv').addEventListener('click', function() {
    var div = document.getElementById('maDivAnimee');
    div.style.width = "200px";
});

document.getElementById('maDivAnimee').addEventListener('transitionend', function() {
    alert('Animation terminée !');
});


//Exemple de la page de démo
ver newsletterButton = document.getElementById("custom");
  newsletterButton.addEventListener("click", () => {
    newsletterButton.innerHTML = "Merci, vous êtes maintenant abonné";
    dataLayer.push({
      event: "newsletterSubscription",
      clientType: "Prospect",
      source: "Popup",
      frequency: "Hebdo"
      ]
    });
  });
```

## Chapitre 10 : Cookies et local storage 

```javascript

// Création d'un cookie
document.cookie = "username=John Doe; expires=Fri, 31 Dec 2023 12:00:00 UTC; path=/";

// Accès à tous les cookies
console.log(document.cookie); // Affiche quelque chose comme : username=John Doe; ...

// Suppression d'un cookie
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";

// Ajout d'une donnée
localStorage.setItem('prenom', 'John');

// Accès à une donnée
console.log(localStorage.getItem('prenom')); // Affiche : John

// Suppression d'une donnée
localStorage.removeItem('prenom');

// Ajout d'une donnée
sessionStorage.setItem('nom', 'Doe');

// Accès à une donnée
console.log(sessionStorage.getItem('nom')); // Affiche : Doe

// Suppression d'une donnée
sessionStorage.removeItem('nom');

```