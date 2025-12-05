**a) Descripción del problema que estás modelando**

Mi ejercicio se centra en la conexion de amistad y comunicación de un grupo de amigos. Donde la conexión (arista) entre dos personas indica que son amigos cercanos 

y se que se comunican frecuentemente (por ejemplo, al menos una vez a la semana). 

La ausencia de una arista indica que la relación es menos cercana o que la comunicación es poco frecuente.


**b) Qué representa cada vértice**

Cada vértice (o nodo) representa a una persona dentro del grupo de amigos.

V1: Miguel (Yo)

V2: Juan

V3: Ana

V4: Rafa

V5: José

V6: Mia


**c) Qué representa cada arista**

Cada arista (o enlace) representa una relación de amistad cercana y comunicación frecuente bidireccional entre dos personas. Al ser una relación de amistad, el 
grafo no será dirigido.

E1: Miguel - Juan

E2: Miguel - Ana

E3: Miguel - Rafa

E4: Juan - Ana

E5: Juan - José

E6: Ana - Mia

E7: Rafa - José

E8: José - Mia


**e) Análisis: grados, conexidad, ciclos si existen**

Como es un grafo no dirigido, las aristas representan una comunicación bidireccional, entonces los grados de entrada y salida son iguales.

deg(Miguel) = 3 (Conectado con Juan, Ana, Rafa)

deg(Juan) = 3 (Conectado con Miguel, Ana, José)

deg(Ana) = 3 (Conectado con Miguel, Juan, Mia)

deg(Rafa}) = 2 (Conectado con Miguel, José)

deg(José) = 3 (Conectado con Juan, Rafa, Mia)

deg(Mia) = 2 (Conectado con Ana, José)

*Suma de grados: $3+3+3+2+3+2 = 16*

*Aristas: 8 x 2 = 16. (Significa la verificacion de los grados)*

El grafo es Conexo. Esto significa que existe un camino desde cualquier vértice hacia cualquier otro. No hay personas aisladas o grupos completamente separados.

Ciclo 1: Miguel -> Juan -> Ana -> Miguel

Ciclo 2: Juan -> José -> Rafa -> Miguel -> Juan (otra ruta del ciclo 1)

Ciclo 3: Juan -> José -> Mia -> Ana -> Juan


**f) Una pregunta interesante que puedas responder con tu grafo**

Pregunta: *Si Juan quiere enviarle una invitación de su fiesta a Rafa pero solo pudo usar a sus amigos cercanos, ¿cuál es el camino más corto que puede enviar el mensaje?*

R = Es la ruta con el menor número de aristas entre Juan y Rafa:

Ruta 1 (2 pasos): Juan -> Miguel -> Rafa

Ruta 2 (2 pasos): Juan -> José -> Rafa

Ambas rutas tienen una longitud de 2, así que el mensaje tiene que pasar por solo una persona para llegar a la indicada a entregar.
