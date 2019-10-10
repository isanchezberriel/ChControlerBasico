# ChControlerBasico
Práctica básica de scripting en Unity. Descripción guiada de lo que el alumno debe implementar.

Sobre la escena que has trabajado ubica un cubo que represente un personaje que vas a mover. Se debe implementar un script que haga de CharacterController. Cuando el jugador pulse las teclas de flecha (o aswd) el jugador ser moverá en la dirección que estos ejes indican.

## Ejercicio 1: 
    Crear un script para el personaje que lo desplace por la pantalla, sin aplicar simulación física.
     - Agregar un campo público que permita graduar la velocidad del movimiento desde el inspector de objetos.
        Estar a la escucha de si el usuario ha utilizado los ejes virtuales. Elegir cuáles se va a permitir utilizar: flechas, awsd.

**Ayuda**: Utilizar la clase Input.
-El recorrido virtual realizado con los controladores (teclas) debe ser proporcional a lo que se desplaza el jugador:
 --Si sólo pulsa una vez, corresponderá a una unidad, Unity asigna +1 o -1 según la dirección del movimiento
 --Si se mantiene pulsado, el jugador debe avanzar en un movimiento continuo, así que Unity asigna un valor entre 0 y 1 ó 0 y -1
 - Una vez que tenemos la proporción del desplazamiento, este también debe ser proporcional a la velocidad que hemos establecido para el objeto. El objeto debe cumplir los siguientes requisitos en el movimiento:
 - Se debe mover exclusivamente en el plano XZ de su sistema de referencia (su suelo)
  - El avance se debe producir hacia adelante.

**Recuerda:** los parámetros que debas usar que sean vectores tienen que ser del tipo Vector3, por tanto, debes crear una referencia a un objeto de tipo Vector3. 
**Recuerda:** Vector3 dispone de la propiedad forward. 
**Ayuda**: la traslación la puedes calcular usando el sistema de referencia del objeto. 
**Ayuda**: Puede que necesites la función GetComponent 
- Elegir otros ejes virtuales para el giro y girar al jugador sobre el eje OY (up). 
- Cada vez que el cubo colisione con una esfera se debe disminuir el poder que tiene. 
- Crear una esfera con física, imprimir en la consola, el estado por el que pasan las colisiones cuando el cubo choca con ella. 
-Realizar un controlodaro para un objeto físico: 
**Recuerda:** En este no debemos mover el objeto actuando sobre su sistema de referencia. Debe ser el motor de física quien actualice sus posiciones, para ello se debe aplicar una fuerza proporcional a la velocidad y la intensidad con la que el jugador usa los ejes.
