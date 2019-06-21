# Drone-Cat-and-Mouse
Practica 2 de la asignatura de Robótica

El juego consiste en un dron negro (gato) que persigue a otro dron de color rojo (ratón) sin llegar a colisionar.
El ratón es independiente mientras que el gato está programado por nosotros.

Primero:
Mediante un filtro del color rojo de las imágenes proporcionadas por las cámaras del gato, sólo se verá al ratón que es lo que nos interesa y el resto estará todo en negro.

Segundo:
Perseguiremos al gato mediante un controlador PID, el cual se calcula con un error de desviación que es la diferencia entre el punto central de la imagen tomadas por las cámaras y el centro de masas del ratón.

Para la velocidad lineal usaremos los pixeles filtrados (será inversamente proporcional al área filtrado) y para la angular el controlor PID anteriormente citado.

En caso de no tener área filtrado (se ha perdido al ratón), se para al gato y se le pone a girar sobre sí mismo para buscar al ratón.

Las constantes del controlador se ha hecho de forma experimental.

[Video Del Algoritmo Funcionando](https://www.youtube.com/watch?v=PtCbkIPXzW4&feature=youtu.be)
