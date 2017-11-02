# TF_Complejidad

## Enemigos:
	- **Tipo 1:** recorre todos los casilleros, excepto los que son de pared irrompible.
	- **Tipo 2:** solo recorre por aquellos casilleros que est�n libres.
	- Aparece uno de cada tipo por nivel. El enemigo tipo 1 en el extremo opuesto al jugador (m-1, n-1), y el enemigo tipo 2 lo m�s cerca a la posici�n de la puerta de salida.
	- Si el enemigo llega a una posici�n en donde ya no tiene casilleros sin visitar para moverse, entonces debera "teletransportarse" al �ltimo casillero donde ten�a posiciones siguientes sin visitar (BFS)

## Jugador:
	- En cada turno, calcula la ruta m�s corta para llegar a la salida, evitando los casilleros de pared irrompible, y a los enemigos.
	- Avanza al siguiente casillero en la ruta calculada y coloca una bomba, luego retorna al casillero diagonal libre mas cercano, si no est� disponible, retorna 2 casilleros en linea opuesta a la bomba.
	- Una vez que explota la bomba, y desaparece la explosi�n, el jugador avanza a la �ltima posici�n visitada (donde coloc� la bomba) y vuelve a ejecutar el algoritmo.