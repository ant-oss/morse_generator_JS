# morse_generator_JS
Une bibliothèque JavaScript permettant de convertir du morse, et de pouvoir envoyer le code par audio

## Utilisation
Cette bibliothèque est assez simple à utiliser :

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

### Émettre le signal audio
Pour émettre le signal, il faut renseigner un fichier audio contenant une tonalité.
Il faut que cette tonalité soit continue sur toute la durée du fichier audio.

Pour initialiser le moteur audio, avec le fichier "chemin":
```
var morseAudio = new MorseSender(chemin);
```
Le moteur audio ne peut envoyer que les messages déjà convertis.
Pour envoyer ".... ..", utilisez :
```
var morseAudio = new MorseSender("beep.mp3");
morseAudio.sendMessage(".... ..");
```
