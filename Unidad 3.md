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
Es lo mismo porque el costo es el mismo, si el costo cambiara seria diferente dijkstra

Actividad 3.2
Compara en la pagina dos algoritmos (A*) y uno ciego. Contestar las siguientes preguntas:
![[Pasted image 20261014155518.png]]
![[Pasted image 20261014155636.png]]
![[Pasted image 20261014155721.png]]
¿Que longitud tiene cada algoritmo?
Manhattan:30
Breadth-first-search:24.73
¿Cuanto tiempo se tardo cada algoritmo?
Manhattan:1.0000ms
Breadth-first-search:2.0000ms
¿Que diferencia observas?
Que uno es mas rapido que el otro ya que permite las diagonales y asi puede cortar el paso 
y asi seria la ruta mas optima 

Actividad 3.3

1.⁠ ⁠Tipos de aprendizaje automático
Aprendizaje supervisado: Los algoritmos aprenden a partir de datos que ya están etiquetados (es decir, tienen la respuesta correcta conocida). Su objetivo es predecir o clasificar nuevos datos basándose en ese entrenamiento previo.
Aprendizaje sin supervisión: El modelo analiza datos que no tienen etiquetas ni respuestas previas. Su propósito es explorar la información, agruparla y descubrir patrones o relaciones ocultas por sí mismo.
Aprendizaje de refuerzo: Un agente aprende a tomar decisiones interactuando directamente con un entorno. Lo hace a través de un sistema de prueba y error, recibiendo recompensas o castigos para descubrir cuál es la acción óptima y lograr un objetivo específico.
2.⁠ ⁠Tarea (T) y Experiencia (E) en Conducción Automática
Tarea (T): Controlar la dirección, aceleración y frenado del vehículo en tiempo real para navegar de forma segura por la carretera sin intervención humana.
Experiencia (E): El conjunto masivo de datos recopilados por los sensores del vehículo (cámaras, radares, LiDAR) y la retroalimentación continua de situaciones de tráfico reales pasadas que el sistema procesa para aprender a reaccionar ante obstáculos, peatones y señales.
3.⁠ ⁠Cuándo usar ML vs. Reglas tradicionales
¿Cuándo conviene usar ML? Cuando se manejan volúmenes masivos de datos estadísticos complejos, dinámicos o no estructurados donde las reglas lógicas tradicionales ("si pasa X, haz Y") se vuelven imposibles de programar o mantener porque los patrones cambian constantemente.
Ejemplo donde NO convendría: El cálculo de impuestos fijos o la aplicación de una fórmula matemática exacta y estática (como calcular el área de un rectángulo o una simple conversión de unidades). Usar ML aquí sería innecesario, costoso y propenso a errores que un código determinista resuelve al 100%.
4.⁠ ⁠Detección de fraudes y anomalías con enfoques no supervisados
Por qué tiene sentido el enfoque no supervisado: Los fraudes graves suelen ser completamente nuevos, extraños y atípicos (por lo que no hay suficientes ejemplos históricos etiquetados como "fraude"). Un modelo no supervisado simplemente busca desviaciones o comportamientos anómalos frente a lo que considera el patrón habitual, sin necesidad de saber de antemano qué forma tendrá el fraude.
El problema del modelo supervisado: Requeriría un volumen enorme de ejemplos previos de fraude exacto para aprender a reconocerlos. Si surge una nueva modalidad de fraude que el modelo no vio durante su entrenamiento (lo cual es muy común), el sistema no lo detectará y pasará desapercibido como un falso negativo.
5.⁠ ⁠Análisis en el sector de la salud (Diagnóstico médico)
¿Qué error es peor? El falso negativo (es decir, que el modelo indique que un paciente está sano cuando en realidad tiene una enfermedad grave, como cáncer o insuficiencia cardíaca).
Por qué: Un falso positivo genera una falsa alarma que se puede corregir con exámenes médicos adicionales (molesto, pero seguro). En cambio, un falso negativo retrasa o evita el tratamiento médico crucial, lo que puede poner en riesgo la vida del paciente al no detectarse la enfermedad a tiempo.
6.⁠ ⁠Análisis de caso: Amazon
Datos que utiliza el sistema: Historial de navegación, compras previas, artículos añadidos a la cesta, búsquedas realizadas, tiempo de permanencia en las páginas de producto y el comportamiento de compra de millones de usuarios similares (filtrado colaborativo).
Quién se beneficia:
La empresa (Amazon): Incrementa sus ventas, retiene a los usuarios y optimiza su inventario.
El usuario: Encuentra productos relevantes de manera rápida y sin esfuerzo.
Quién podría salir perjudicado: El usuario, debido a la privacidad. Sus hábitos de consumo son rastreados y analizados constantemente, lo que puede vulnerar su intimidad digital o manipular sus decisiones de compra mediante sesgos comerciales (publicidad invasiva o compras impulsivas).
7.⁠ ⁠Lectura crítica del artículo
Dos elementos que generan dudas sobre la información son:
Incongruencia numérica en el título: El título promete "12 aplicaciones y ejemplos exitosos de aprendizaje automático", pero a lo largo del texto solo se listan o desarrollan de forma general 11 industrias/aplicaciones principales antes de pasar a los casos comerciales propios.
Promoción comercial sesgada: El artículo es un texto de marketing redactado por la propia empresa desarrolladora (Helpware Tech), por lo que las cifras de éxito presentadas (como "6X CTR" o "mejor precisión de pronóstico (80%)") son autorreferenciales y carecen de una auditoría externa o metodología transparente que explique cómo se midieron.
Qué se le pediría al autor para confiar más:
Metodologías detalladas y métricas de validación independientes (como matrices de confusión o pruebas en entornos de control reales) que respalden los porcentajes de mejora anunciados.
Casos de estudio documentados con la participación o el testimonio directo de los clientes reales que contrataron el servicio, en lugar de descripciones generales comerciales.

Actividad 3.4
