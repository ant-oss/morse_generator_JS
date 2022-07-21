# morse_generator_JS
Une bibliothèque JavaScript permettant de convertir du morse, et de pouvoir envoyer le code par audio

## Utilisation
Cette bibliothèque est assez simple à utiliser.

### Convertir des messages en morse

Exemple pour convertir "hello" en morse

```
var converter = new MorseConverter();
var str = "hello";
var converted = converter.convertString("morse", str);

console.log(converted) //Sortie :  ".... . .-.. .-.. --- "
```

### Convertir des messages en texte

Exemple pour convertir ".... .." en texte

```
var converter = new MorseConverter();
var str = ".... ..";
var converted = converter.convertString("texte", str);

console.log(converted) //Sortie :  "hi"
```
