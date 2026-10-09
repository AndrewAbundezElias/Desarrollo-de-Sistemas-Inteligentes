Actividad 3.1
Algoritmos de búsqueda

1. Problemas de búsqueda: 
Desafíos computacionales en los que un agente debe encontrar una secuencia de acciones que lo lleve desde una situación inicial hasta un objetivo determinado en un entorno definido.
2. Espacios de estado:
Conjunto de todos los estados posibles en los que se puede encontrar el problema o sistema durante el proceso de búsqueda.
3. Estado inicial:
Configuración o punto de partida desde el cual el agente comienza el proceso de solución.
4. Acciones:
Operaciones o movimientos válidos que el agente puede realizar para pasar de un estado a otro dentro del espacio de estados.
5. Modelo de transición:
Función matemática o lógica que describe cuál será el estado resultante al aplicar una acción específica en un estado dado.
6. Prueba de meta:
Función que evalúa un estado actual para determinar si satisface todas las condiciones requeridas para ser considerado un estado objetivo o solución.
7. Costo del camino:
Valor numérico asignado a una trayectoria de acciones, calculado normalmente como la suma de los costos individuales de cada paso dentro del camino.
8. Solución:
Secuencia ordenada de acciones que transforma el estado inicial en un estado que satisface la prueba de meta.
9. Frontera:
Estructura de datos que almacena todos los nodos que han sido generados pero que aún no han sido explorados o expandidos.
10. Nodo:
Estructura de datos que representa un punto en el árbol o grafo de búsqueda, la cual contiene el estado correspondiente, el nodo padre, la acción aplicada y el costo acumulado.
11. Agente de resolución de problemas:
Tipo de agente inteligente orientado a metas que planifica secuencias de acciones en entornos deterministas, estáticos y conocidos.
------------------------------------------------------------------------
Sistemas de búsqueda(ciega)

------------------------------------------------------------------------
- Búsqueda no informada(ciega):
Conjunto de algoritmos que exploran el espacio de estados utilizando únicamente la definición del problema, sin heurísticas o información adicional sobre la cercanía a la meta.
- Búsqueda en amplitud:
Estrategia que explora el árbol de búsqueda nivel por nivel, evaluando primero todos los nodos a una profundidad determinada antes de pasar a la siguiente.
- Búsqueda en profundidad:
Estrategia que explora la rama más profunda del árbol de búsqueda hasta alcanzar un nodo hoja o un límite antes de realizar _backtracking_.
- Búsqueda de costo uniforme:
Algoritmo que expande siempre el nodo de la frontera que tenga el menor costo acumulado g(n), garantizando encontrar la ruta de menor costo en grafos ponderados.
- Cola:
Estructura de datos lineal donde el primer elemento en ingresar es el primero en salir, utilizada típicamente para implementar la frontera en BFS.
- Pila:
- Estructura de datos lineal donde el último elemento en ingresar es el primero en salir, utilizada típicamente para implementar la frontera en DFS.
- Completitud:
Propiedad que garantiza que el algoritmo siempre encontrará una solución en caso de que exista una dentro del espacio de estados.
- Optimalidad:
Propiedad que asegura que el algoritmo devolverá la solución con el menor costo posible entre todas las soluciones válidas.
- Complejidad en tiempo:
Medida del número de nodos generados o explorados por el algoritmo antes de hallar una solución, expresada en función del factor de ramificación (b) y la profundidad (d).
- Complejidad en espacio:
Cantidad de memoria requerida por el algoritmo durante la ejecución, determinada principalmente por el número máximo de nodos almacenados simultáneamente en la frontera.
![[Pasted image 20261008181637.png]]
![[Pasted image 20261008181241.png]]
![[Pasted image 20261008181410.png]]
![[Pasted image 20261008181523.png]]![[Pasted image 20261008181523 1.png]]
Es lo mismo porque el costo es lo mismo si el costo cambiara seria diferente 