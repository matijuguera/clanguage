## Guia 01 - Guia Prolog

### Ejercicio 1 - Dada la siguiente base de conocimiento:

palabra(abalone,a,b,a,l,o,n,e).
palabra(abandon,a,b,a,n,d,o,n).
palabra(enhance,e,n,h,a,n,c,e).
palabra(anagram,a,n,a,g,r,a,m).
palabra(connect,c,o,n,n,e,c,t).
palabra(elegant,e,l,e,g,a,n,t).

Se busca resolver el siguiente problema: Colocar las palabras de modo tal que se puedan ubicarlas en el siguiente tablero.

|----+---+----+---+----+---+----|
|    |   | V1 |   | V2 |   | V3 |
|----+---+----+---+----+---+----|
| H1 |   |    |   |    |   |    |
|----+---+----+---+----+---+----|
|    |   |    |   |    |   |    |
|----+---+----+---+----+---+----|
| H2 |   |    |   |    |   |    |
|----+---+----+---+----+---+----|
|    |   |    |   |    |   |    |
|----+---+----+---+----+---+----|
| H3 |   |    |   |    |   |    |
|----+---+----+---+----+---+----|

* Ejercicio extraido desde "Learn Prolog Now! By: Patrick Blackburn, Johan Bos and Kristian Striegnitz"

### Ejercicio 2 - Apellidos

Dada la siguiente base de datos de conocimentos:

padre(guillermo, rossi, walter).
madre(beatriz, capusotto, walter).
padre(guillermo, rossi, lucia).
madre(beatriz, capusotto, lucia).

Responder (true):
apellido(guillermo, rossi)?
apellido(beatriz, capusotto)?
apellido(walter, rossi)?
apellido(lucia, rossi)?


### Ejercicio 3 - Hernamos

**NOTA**: Dos personas son hermanos si tienen un padre o madre en común
Dada la siguiente base de datos de conocimentos:

padre(guillermo, rossi, walter).
padre(guillermo, rossi, lucia).
padre(guillermo, rossi, camilla).

madre(beatriz, capusotto, lucia).
madre(beatriz, capusotto, walter).
madre(beatriz, capusotto, rodolfo).
madre(jimena, kaplan, camilla).

Responder:
hermanos(walter, lucia)? (*true*)
hermanos(camilla, lucia)? (*true*)
hermanos(rodolfo, camila)? (*false*)



### Ejercicio 4 - Viajeros

Dada la siguiente base de datos de conocimentos:

enAuto(auckland,hamilton).
enAuto(hamilton,raglan).
enAuto(valmont,saarbruecken).
enAuto(valmont,metz).

enTren(metz,frankfurt).
enTren(saarbruecken,frankfurt).
enTren(metz,paris).
enTren(saarbruecken,paris).

enAvion(frankfurt,bangkok).
enAvion(frankfurt,singapore).
enAvion(paris,losAngeles).
enAvion(bangkok,auckland).
enAvion(singapore,auckland).
enAvion(losAngeles,auckland).

Se necesita: Construir una regla llamada viajar/2 (recibe desde hasta) que responda si es posible llegar desde un lugar hacia otro, cualquiera sea el método de trasporte que utilicemos. Considerar combinaciones.

Responder:
viajar(valmont, auckland)? (*true*)
viajar(auckland, raglan)? (*true*)
viajar(valmont, metz)? (*true*)
viajar(valmont, bsas)? (*false*)


* Ejercicio extraido desde [swi-prolog](http://lpn.swi-prolog.org/lpnpage.php?pagetype=html&pageid=lpn-htmlse12)

### Ejercicio 5 - Miembro de Listas

Construir un predicado que devuelva *true* cuando un elemento está dentro de la lista.

### Ejercicio 6 - Reverso de lista

Construir un predicado que devuelva el reverso de la lista. [1,2,3] -> [3,2,1].
