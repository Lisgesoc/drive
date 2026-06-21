# ***SISTEMAS INTELIGENTES***

## **Indice**

### Tema 1: Intro
* 1.1 Agentes
* 1.2 Tipos de IA

### Tema 2: Agentes
* 2.1 Entorno (REAS y Propiedades)
* 2.2 Tipos de Agentes Según su Control
* 2.3 Sistemas Multi-Agente

### Tema 3: Busqueda y Planificación
* 3.1 Representación de un Problema
* 3.2 Búsqueda No informada
* 3.3 Búsqueda Heuristica (Algoritmo A*)
* 3.4 Búsqueda Local y Optimización
* 3.5 Búsqueda con Adversarios (Juegos de Suma Cero)

### Tema 4: Sistemas Bio-inspirados
* 4.1 Algoritmos Genéticos (AG)
* 4.2 Estrategias Evolutivas (EE)
* 4.3 Sistemas Emergentes (Hormigas y Enjambres)
* 4.4 Clasificación de la Computación Evolutiva como Agente

---


## **Tema 1: Intro**
- **Definición de Inteligencia**: Conjunto de procesos de pensamiento humano; toma de decisiones, resolucion de problemas, aprendizaje.
- **Inteligencia Artificial**: Disciplina de resoluciond e problemas al borde de lo computable.
- **Sistemas cognitivos**: Sistemas que exhiben inteligencia de tipo humana a través de procesos como el aprendizaje, razonamiento y memoria.
### 1.1 Agentes (Avanzar T2)
- **Def**: Es cualquier cosa capaz de percibir su medioambiente (sensores) y actuar en ese medio (actuadores)
- **Agente Racional**: Es aquel que ejecuta siempre la accion que maximice su **Medida de Rendimiento**
#### Factores racionalidad
- Medida de rendimiento que define el exito
- El conocimiento acumulado del medio
- Las acciones posibles
- La secuencia de percepciones
### 1.2 Tipos de IA
_____
#### Simbólica (Solo contempla la logica programada)
- Basado en **Conocimiento**
- Enfoque deductivo
- Busqueda heurística
- Top-Down
#### Subsimbólica (De los datos saca la lógica)
- Basado en **Datos**
- Machin learning
- Enfoque inductivo
- Bottom-Up
_____
#### General vs Narrow
- IA que puede resolver cualquier tarea vs IA capaz de resolver una
____
#### Fuerte vs Débil
- IA consciente de si misma vs IA que simula ser inteligente

## **Tema 2: Agentes**
- **Def**: Es cualquier cosa capaz de percibir su medioambiente (sensores) y actuar en ese medio (actuadores)
    - Proceso computacional autonomo
    - Percibe e interactua con el entorno
    - Puede comunicarse con otros agentes
    - Conjunto finito de tareas
- **Reactivos**: acciones directas
- **Objetivos**: planifican a largo plazo

#### Función Sobreyectiva f : P - A
- Todas las acciones al menos una percepción desencadenante
- Todas las percepciones desencadenan una unica acción
- **Agente Racional**: Es aquel que ejecuta siempre la accion que maximice su **Medida de Rendimiento**
#### Factores racionalidad
- Medida de rendimiento que define el exito
- El conocimiento acumulado del medio
- Las acciones posibles
- La secuencia de percepciones
____
### 2.1 Entorno
#### **REAS**: Rendimiento Entorno Actuadores Sensores
- **Rendimiento**: Definir una medida (Ej. roomba - mas superficie limpia)
- **Entorno**: Descripción formalización
- **Acciones**: Descripción de como se puede modificar el entorno
- **Sensores**: Descripción de como percibe el entorno 

#### Propiedades del Entorno
- **Totalmente vs Parcialmente Observable**: Si tenemos toda la info relevante
- **Determinista vs Estocástico**: Si el siguiente estado del entorno = entorno actual + acción propia
- **Episódico vs Secuencial**: Si se planifica solo una acción o una posible secuencia futura
- **Estático vs Dinámico**: Si el entorno puede cambiar mientras el agente calcula su acción
- **Discreto vs Contínuo**: Si el Nº de estados del entorno es finito o infinito
- **Individual vs Multiagente**: Si en el sistema opera mas de 1 agente (Tambien pueden ser personas)
- **Competitivo vs Colaborativo**: Siendo multiagente si compiten o colaboran
____
### 2.2 Tipos de Agentes **Segun su Control**
####  Agente reactivo **Simple**
- Decisiones en base a la percepción actual, sin histórico
- Formalismos: Tabla, if-else, Interprete de reglas básicas
- Respuestas rápidas a eventos simples
- Propenso a bucles infinitos
____
#### Agente reacivo basado en **Modelo**
- Máquina de estados finita, pila de estados, arbol de comportamiento
- Mantiene un estado interno que depende de la historia de la percepción
- El estado debe actualizarse a cada variación de percepción
- La meta del agente es intrinseca y no cambia

##### Arbol de comportamiento
- Un arbol de comportamiento tiene nodos intermedios como decisiones y nodos hojas como acciones (son los unicos nodos finales)
- Los nodos decision se comportan como booleanos para cambiar al siguiente nodo
- La ejecucion puede ser:
    -Secuencial: seguir mientras succes
    -Selector: seguir mientras failure
    -Parallel: ejecuta nodos sin ves su terminación
    -ETC: se pueden definir nodos como queramos 
____
#### Agentes basados en **Objetivos**
- Las metas pueden cambiar esto implica replanificación
- Al haber mas de una meta una acción correcta depende de la meta
- Formalismos: Busqueda, Planificación
____
#### Agentes basados en **Utilidad**
- Elige mejor entre opciones 
- Decide entre objetivos contradictorios (Llegar rápido/Llegar seguro)
- Formalismos: Función de utilidad
____
#### Agentes que **Aprenden**
- Permite moverse en entornos Desconocidos
- Versatil
- Un actuador es cualquiera de los agentes anteriores
- El aprendizaje formula nuevas reglas y mejora la actuación
- Formalismos: Aprendizaje por refuerzo, supervisado o no
____
#### Agentes **Deliberativos** basados en **Objetivos**
- Varias implementaciones:
    - Usando reglas de inferencia
    - Usando busqueda y planificación
    - Sistema intencionales usando arquitectura BDI
##### - Arquitectura BDI (Creencias, Deseos, Intenciones)
- BRF: Funcion que revisa las creencias
- Funcion generadora de opciones
- Filtrado de opciones para quedarse con la Intención
#### Agentes vs Objetos (Diapos 38)
____
### 2.3 Sistemas **Multi-Agente**
- Conjunto de agentes autónomos, heterogeneos(Distintos), que trabajan para resolver el mismo problema
#### Ventajas
- Aumenta la potencia del sist.
- Robustez y tolerancia a fallos
- No es necesario que cada agente conozca toda la info
- Mejores en entornos dinamicos
#### Interacción entre agentes
##### Tipos de colaboración
| Tipo | Objetivos | Recursos | Habilidad |
| :--- | :--- | :--- | :--- |
| **Independencia** | Compatibles | Suficientes | Suficientes |
| **Colaboración simple** | Compatibles | Suficientes | Insuficientes |
| **Obstrucción** | Compatibles | Insuficientes | Suficientes |
| **Colaboración coordinada** | Compatibles | Insuficientes | Insuficientes |
| **Competición individual** | Incompatibles | Suficientes | Suficientes |
| **Competición por equipos** | Incompatibles | Suficientes | Insuficientes |
| **Conflicto individual** | Incompatibles | Insuficientes | Suficientes |
| **Conflicto colectivo** | Incompatibles | Insuficientes | Insuficientes |
____
#### Organización (Pueden ser estatica o dinámica)
- Definida por el programado
- Resultado de interacciones
- Jerárquica
- Igualitaria
#### Tipos de relación
- Conocimiento: A conoce a B y puede comunicarse con B.
- Comunicación: Existe un canal de comunicación entre A y B.
- Subordinación: B realiza una tarea que A le pide.
    - Estática (Maestro / Esclavo): El agente subordinado no se puede negar.
    - Dinámica: El agente subordinado se puede negar o negociar la tarea.
- Operativa: A depende de que B realice antes otra tarea para poder proceder.
- De información: A cree la información que le proporciona B.
- Conflicto: Varios agentes necesitan o compiten por los mismos recursos finitos.
- Competición: Agentes operando con metas u objetivos incompatibles entre sí.
____
#### Cooperación
- **Def**: Mecanismo útil para mejorar de forma directa el rendimiento del grupo y resolver conflictos.
##### Formas de cooperar
- Cooperación intencional: Los agentes son plenamente conscientes de que deben colaborar.
- Desde el punto de vista del observador: Los agentes cooperan de forma efectiva pero no son conscientes de ello.
##### Tipos de cooperación comunes
- Agrupamiento de agentes (mecanismo inspirado en la biología).
- Compartir información relevante.
- Especialización de tareas específicas entre los agentes.
- Compartir recursos limitados del medio.
- Resolución guiada de conflictos mediante arbitraje externo.
____
#### La comunicación
- **Def**: Es la base fundamental de la colaboración y la coordinación; permite solicitar tareas, recursos, proponer información, compartir creencias o coordinarse.
##### Según el canal de transmisión
- Señal: Modificación directa del entorno físico o virtual que no cuenta con un destinatario fijo.
- Mensaje: El agente emisor envía la información directamente a otro agente con un destinatario explícito.
##### Según la sincronización temporal
- Síncronos: El emisor se bloquea y se queda a la espera de que el receptor conteste de forma inmediata.
- Asíncrono: El emisor no espera la recepción del mensaje ni la contestación, continuando con sus tareas.
____
#### Tipos de colaboración y contratos
##### Mecanismos de reparto de tareas
- Distribuida: Cada agente se encarga de gestionar de forma autónoma sus propios recursos y servicios.
- Centralizada: Un agente coordinador específico se encarga por completo del reparto global.
- Emergente: El reparto formal de tareas surge de forma natural a raíz de las interacciones.
##### Gestión mediante contratos
- Contrato: Acuerdo donde el proveedor se compromete a realizar la tarea y el cliente a no encargársela a ningún otro.
- Fases del ciclo de vida de un contrato: Asignado - Cerrado - Hecho - Roto.
- Smart contracts: Contratos automatizados ejecutados por agentes software con validez real que se apoyan en tecnología blockchain.
____
#### Red de contratos (Contract Net Protocol)
##### Fases consecutivas del protocolo
1. Anuncio: El cliente publica de forma abierta una tarea vacante en la red.
2. Oferta: Los contratistas evalúan la tarea y envían sus ofertas al cliente mediante su red de conocidos, un registro o memoria.
3. Evaluación: El cliente estudia de forma analítica las ofertas y se queda con la que más le interesa.
4. Formalización: Se cierra y formaliza el contrato definitivo entre ambas partes.
##### Especificaciones críticas a detallar en un contrato
- Calidad mínima requerida del trabajo para ser aceptado.
- Metodología o métricas bajo las cuales se evaluará el resultado.
- Fecha límite de realización o entrega de la tarea (Deadline).


## **Tema 3: Busqueda y Planificación**

### 3.1 Representación de un Problema
- **Espacio de estados**: conjuto de todos los estados que resuelven
- **Espacio de búsqueda**: arbol o grafo que sólo contiene nodos de busqueda

- **Definición de un Problema**
  - Estado inicial
  - Función sucesor: conjunto de pares(acción, estado sucesor)
  - Test de objetivo
  - Función de coste del camino

### 3.2 Búsqueda No informada
**Def**: No necesitan info adicional del dominio
##### Anchura
- Se explora el espacio de busqueda en anchura
- Es completo:asegura llegar a la solución
- Si los operadores tienen el mismo coste obtendra solución óptima
- O(r^p); r:sucesores p:profundidad media de la solu
##### Busqueda con costes
- Si el coste no siempre es el mismo expande nodos con menor coste
- Si el coste de sus hijos es positivo y no hay ciclos entre ellos seguirá siendo completo y optimo
##### Profundidad
- Se explora el espacio en profundidad
- No completo
- No óptimo

### 3.3 Búsqueda Heuristica
- Para problemas muy grandes se quedara sin tiempo y/o sin memoria antes de encontrar la solución
- **Heurística**: Solución rápida de un problema cuando se tiene una info parcial
- El coste de la función heuristica debe ser menor o igual al de recorrer el cammino pero lo mas proximo posible
- **Dist. Euclídea**: En linea recta desde un nodo a la solu
- **Dist. Manhattan**: No cuenta diagonales
#### Búsqueda Voraz
- Se exploran los hijos empezando por el mas prometedor
- Se implementa sobre una cola de prio
- No es completa ni admisible
#### **A\***
- Minimiza el coste total de la solución
- Abandona un camino ya explorado si detecta que no es el mas prometedor
- f(n)=g(n)+h(n)
- Si f admisible => completo y optimo

### 3.4 Búsqueda Local y Optimización
Ideales cuando el espacio de búsqueda es gigantesco y sacrificamos completitud/optimalidad para obtener una solución subóptima aceptable en un tiempo razonable. Se mueven de forma incremental en el espacio de soluciones candidatas.

##### - Escalada (*Hill-Climbing*)
- Parte de una solución inicial aleatoria y evalúa sus vecinas, moviéndose únicamente hacia aquella que mejore el desempeño actual.
- Extremadamente rápido, pero sufre el problema de quedar atrapado en **mínimos/máximos locales** o el *efecto meseta*.
- *Versión Estocástica*: Para mitigar los mínimos locales, si el algoritmo se congela, ejecuta un salto completamente aleatorio hacia otra región del mapa manteniendo guardado el mejor resultado global.

##### - Enfriamiento Simulado (*Simulated Annealing*)
- Inspirado en el proceso metalúrgico de calentar y enfriar lentamente un material para estabilizar sus propiedades físicas.
- En cada iteración evalúa un vecino de forma probabilística. La gran diferencia con la escalada es que **acepta soluciones peores** en función de la "temperatura" actual del sistema.
- Al inicio (alta temperatura) acepta casi cualquier cambio errático para explorar el mapa; conforme el tiempo avanza (enfriamiento), se vuelve más estricto hasta estabilizarse.

### 3.5 Búsqueda con Adversarios (Juegos de Suma Cero)
Estrategias aplicadas a sistemas multiagente competitivos donde las acciones de un jugador perjudican de forma directa al rival y viceversa.

##### - Algoritmo Minimax
- Modela un árbol de juego con dos roles intercalados por turnos: **MAX** (el agente, intenta maximizar su puntuación) y **MIN** (el oponente, intenta minimizar el beneficio de MAX).
- El valor de un nodo se calcula de forma recursiva hacia arriba
- Limitación: Es de coste exponencial en tiempo. En la práctica se requiere establecer un **límite estricto de profundidad** y evaluar los estados hojas con una heurística de juego en lugar de la utilidad real final.

##### - Poda Alfa-Beta
- Optimización directa que permite descartar ramas completas del árbol Minimax sin necesidad de examinarlas, reduciendo drásticamente el exponente temporal.
- Utiliza dos variables de control actualizadas dinámicamente:
- Criterio de poda: Si en cualquier punto de la exploración el valor de un nodo en una rama es peor que el rango determinado por $[\alpha, \beta]$, esa sub-rama se corta (*poda*) porque un jugador racional nunca elegirá ese camino.

## **Tema 4 Sistemas Bio-inspirados**
- **Definición**: Rama de la IA que resuelve problemas complejos de optimización. Inspirada en la evolucion biologica
- **Gen**: la unidad minima de transferencia genetica
- **Genotipo**:  conjunto de genes de un individuo
- **Fenotipo**: Implementacion de genotipo

### 4.1 Algoritmos Genéticos (AG)
Pretenden resolver problemas combinatorios y de optimización representando soluciones discretas en forma de vectores o matrices de genes.
- **Individuo**: Vector de genes que representa una solución única candidata.
- **Población**: Conjunto de individuos en una generación concreta (la población inicial suele generarse de forma aleatoria).
- **Convergencia Prematura**: Riesgo de que el algoritmo quede atrapado en un mínimo local debido a la pérdida de variabilidad genética por un exceso de peso del operador de cruce.

##### Operadores Genéticos Canónicos:
- **Selección**: Escoge a los mejores individuos para reproducirse en base a su calidad.
    - Ruleta: Elección aleatoria con mayor probabilidad propocional al fitness.
    - Jerárquica: Ordena la población por fitness y selecciona segun la probabilidad dependiendo de la posición.
    - Torneo: Elige K elementos al azar y se queda estrictamente con el de mejor fitness (K regula la presión selectiva).
- **Cruce**: Se cruzan individuos de 2 en 2.
- **Mutación**: Se modifican de forma aleaoria (Probabilidad) los genes de individuos recien cruzados.
- **Inversión**: se invierten algunos genes.

- **Def Fitness**: Funcion que evalua las soluciones y encuentra la mas apta
##### Elitismo
- Estrategia para algoritmos que permite promocionar a los N mjores individuos de la anterior a la siguiente generacion. (N baja mejor)
##### Gestión de Individuos No Válidos:
- Penalizar drásticamente el fitness del individuo para impedir que sea seleccionado en la ruleta.
- Descartar la solución inválida y repetir inmediatamente el proceso de reproducción.
- Modificar el cruce y la mutación para impedir Invalidos o adaptar al individuo valido mas cercano.

### 4.2 Estrategias Evolutivas (EE)
Estrategia similar a la genética pero con valores continuos.
- **Representación**: Cada individuo {vector de codificación (x sub i), vector de varianzas (var sub i)}.
- **Notación estrategia**: (u/p,a) u:tam pob; p:nº padres seleccionados; a:nº descendientes
#### Algo (1+1)EE
- *Solo un individuo*
- **Notación indiv**: P=x,var
- Se genera pob intermedia  mutando al individuo
- Si mejor se reemplaza
- Sin cruce
#### Multiples indv
- Misma idea pero con cruce
- x'=(x1+x2)/2
- var'=sqrt(var1+var2)
#### Evolutiva como Agente
- Agente basado en objetivos que resuelve problema de optimización
- Cambio en la función fitness pues cada individuo puede ser solucion y esto varia la condición de parada del algo
- Se adaptan muy bien a entornos cambiantes si mantenemos la diversidad genética

### 4.3 Sistemas Emergentes
Sistemas complejos compuestos por multitud de agentes con reglas de comportamiento individuales que en comportamiento conjuto son inteligentes.

##### - Colonias de Hormigas
- Metaheurística inspirada en la busqueda de alimentos de una hormiga.
- **Mecanismo de Feromona**: los agentes se mueven de forma aleatoria en el espacio de solu, y dejan rastro de feromonas.
- **Disipación/Evaporación**: La feromona decrece con el tiempo en las rutas menos transitadas. Esto elimina de forma natural las soluciones subóptimas.

### 4.4 Clasificación de la Computación Evolutiva como Agente
- **Tipo de control**: Agentes resuelve-problemas de optimización (basados en objetivos). La ruta o secuencia de acciones carece de valor; el éxito radica únicamente en la calidad del estado de configuración final alcanzado.
- **Evolución**: Agentes que aprenden (aprendizaje no supervisado). El algoritmo refina y descubre de manera autónoma las reglas óptimas del espacio de soluciones guiándose exclusivamente por la función de fitness.
- **Interacción**: Sistemas multiagente de colaboración coordinada (en hormigas y enjambres) donde la comunicación es indirecta y se realiza por señales mediante la alteración del medio (rastros de feromonas).

## **Tema 5 Aprendizaje Automatico (Machine Learning)**

### 5.1 Intro y Aprendizaje supervisado
- **Aprendizaje**: Proceso de adquirir conocimiento o aptitudes.
- **Automatico**: Mecanismo o aparato que funciona total o parcialmente por si solo.
- **ML Agente**: Son agentes que aprenden y se adaptan a entornos dinamicos. El ML los permite predecir el comportamiento de un sistema a futuro.
Como en el aprendizaje animal(Humano) ML requiere capacidad de abstraccion de pequeños detalles y memoria. Aunque la abstracción incluya sesgos, estos son necesarios para poder ser utiles en ejemplos no entrenados.
- **Sesgo**: Modelo de simplificacion de un problema introduciendo un "posible" error.
- **Varianza**: No introduce sesgos en el modelo. Realmente no nos beneficia la Sobre Adaptacion.
- **Tipos de Aprendizaje(Entrenamiento)**
    - Supervisado: Los ejemplos deben contener la solucion.
    - No Supervisado: Ejemplos sin info del resultado esperado.
    - Por Refuerzo: Retroalimentacion del entorno. Prueba y error. 

- **Tipos de Problemas**
    - Clasificacion: Categorizar un elemento. Salida discreta.
    - Regresion: Estimar la salida con la mayor accuaricy posible. Salida continua.
    - Agrupamiento: Intentar conocer el numero y el tipo de clases.
    - Reduccion de Dimensiones: Extraer caracteristicas relevantes.
    - Asociacion: Establecer relaciones entre variables.
    - Generraciond e Contenido: Genera en base a datos del entrenamiento.

#### Aprendizaje Supervisado
- Pretende deducir una **funcion** que dada la entrada se obtenga la solucion deseada.
- Cada instancia de entrenamiento debe ser un vector de entrada y su salida esperada.
- La entrada **matriz** n*m. N: numero de instancias, M: Numero de atributos.
- Los atributos pueden ser cuantitativos (Numericos) o cualitativos (Categoricos).
- **Correcta Representacion de Datos**
    - Evitar ruido (datos erroneos o atributos inutiles)
    - Suficientes ejemplos
    - Misma escala para todas las entradas de cada atributo
    - Discretizacion de atrb num
    - Categoricos a binarrio tantos atributos como categorias y marcando el positivo. **One-Hot Encoding** (Codigo en Anexo II).
- **Testing**
    - Dividir el conjunto de datos en **Entrenamiento y Prueba**.
    - Posible conjunto de Validacion (Durante el entrenamiento para mantener capacidad de generalizacion)

#### Tecnicas de Aprendizaje Supervisado
- Posibles modelos e implementaciones (Ver en **Tema 5.1.3**)

### 5.2 Redes Neuronales



## **Anexo I: Índice de Consulta Rápida para el Examen**

* **Clasificar la relación o el tipo de colaboración entre robots, países o agentes** ==> Consultar 2.3
* **Definir el REAS o las 6 propiedades básicas del entorno de un puzle o robot** ==> Consultar 2.1
* **Elegir el tipo de control o arquitectura de software interna de un agente** ==> Consultar 2.2
* **Formalizar las 4 constantes de un puzle (Estado Inicial, Objetivo, Operadores, Coste)** ==> Consultar 3.1
* **Diseñar, proponer o demostrar si una función heurística para A\* es admisible** ==> Consultar 3.3
* **Resolver un problema combinatorio o de asignación gigante (ej: libros en estantes)** ==> Consultar 4.1 y 3.4
* **Controlar o corregir la generación de individuos no válidos que rompen las reglas** ==> Consultar 4.1
* **Optimizar un problema físico o matemático basado en valores continuos o reales** ==> Consultar 4.2
* **Modelar interacciones simples basadas en feromonas u olvido de rutas subóptimas** ==> Consultar 4.3
* **Adaptar un puzle ante un rival por turnos (Suma cero / Minimax / Poda Alfa-Beta)** ==> Consultar 3.5
* **Justificar la elección de IA Simbólica (Top-Down) vs IA Subsimbólica (Bottom-Up)** ==> Consultar 1.2
* **Clasificar un algoritmo genético, evolutivo o bio-inspirado como tipo de agente** ==> Consultar 4.4

## **Anexo II: Codificar**

* **One-Hot Encoding**
```python
from sklearn.preprocessing import OneHotEncoder
oneHotEncoder = OneHotEncoder(drop='first')
oneHotEncoderFit = oneHotEncoder.fit(provincias.reshape(-1,1))
oneHotEncoderFit.transform(provincias.reshape(-1,1)).toarray()
```
* **Tratamiento valores perdidos o nulos**
```python
from sklearn.impute import SimpleImputer
```
* **Division conjunto de datos**
```python
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(data, y, train_size = 0.8, random_state = 1234)
```