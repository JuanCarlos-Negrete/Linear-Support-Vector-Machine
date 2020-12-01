# Linear Support Vector Machine

## Equipo #6:
- 16210975 Luna Fuentes Fernando
- 16212354 Hernández Negrete Salma Fabel
- 15211900 Jiménez Diaz de Sandi René

### Descripción

También son conocidas con el acrónimo SVM por sus siglas en inglés (Support Vector Machines). Se pueden usar tanto para regresión como para clasificación.

Son un conjunto de algoritmos de aprendizaje supervisado desarrollados por Vladimir Vapnik y su equipo en los laboratorios AT&T.

Un SVM construye un hiperplano o conjunto de hiperplanos en un espacio de dimensionalidad muy alta (o incluso infinita) que puede ser utilizado en problemas de clasificación o regresión. Una buena separación entre las clases permitirá una correcta clasificación.

#### Idea básica

Dado un conjunto de puntos, subconjunto de un conjunto mayor (espacio), en el que cada uno de ellos pertenece a una de dos posibles categorías, un algoritmo basado en SVM construye un modelo capaz de predecir si un punto nuevo (cuya categoría desconocemos) pertenece a una categoría o a la otra.

Como en la mayoría de los métodos de clasificación supervisada, los datos de entrada (los puntos) son vistos como un vector p-dimensional (una lista ordenada de p números).

La SVM busca un hiperplano que separe de forma óptima a los puntos de una clase de la de otra, que eventualmente han podido ser previamente proyectados a un espacio de dimensionalidad superior.

En ese concepto de "separación óptima" es donde reside la característica fundamental de las SVM: este tipo de algoritmos buscan el hiperplano que tenga la máxima distancia (margen) con los puntos que estén más cerca de él mismo. Por eso también a veces se les conoce a las SVM como clasificadores de margen máximo. De esta forma, los puntos del vector que son etiquetados con una categoría estarán a un lado del hiperplano y los casos que se encuentren en la otra categoría estarán al otro lado

#### ¿Por qué se llaman Máquinas de Vectores de Soporte?

Se llama «máquina» en español por la parte de «machine» learning. Los vectores de soporte son los puntos que definen el margen máximo de separación del hiperplano que separa las clases. Se llaman vectores, en lugar de puntos, porque estos «puntos» tienen tantos elementos como dimensiones tenga nuestro espacio de entrada. Es decir, estos puntos multidimensionales se representan con con vector de n dimensiones.

![ScreenShot](https://github.com/SalmaFabel/IMG/blob/main/IMAGEN%20Linear%20Support%20Vector%20Machine.PNG)

### Datos de ejemplo - Regularización [FERNANDO]
Imaginemos que tenemos dos clases de datos, la clase Azul y la clase Roja. Lo que deseamos hacer es trazar una línea que separe las 2 clases. De esta forma, cuando un punto nuevo llegue, podremos ver a cual de las 2 clases pertenece dependiendo de en qué lado de la línea se encuentre.

<img src="https://i.imgur.com/1itSHRR.png">

### Como no clasificar los datos.

<img src="https://i.imgur.com/AE6FJ2H.png">

<img src="https://i.imgur.com/lsPsIeF.png">

### Forma óptima de clasificar los datos.

Se busca maximizar el margen entre ambas clases, por lo que una línea que mejor distingue las 2 clases es preferible ya que las máquinas de vectores son técnicas de machine learning que encuentran la mejor separación posible entre las clases.

<img src="https://i.imgur.com/i47Tr3c.png">

### Regularización 
En veces los datos tienen ruido por qué no están bien clasificados o por el nivel de complejidad de algunos puntos. En estos casos, se le dice al SVM que generalice esos pocos casos del conjunto.

### Truco del Kernel en SVM - Algunas aplicaciones
El propósito  principal del SVM es el formar el hiperplano que maximiza el margen de separación entre clases, sin embargo, hay veces en las que no hay forma 
de encontrar un hiperplano que permita separar dos clases. En estos casos decimos que las clases no son linealmente separables. Para resolver este problema 
podemos usar el truco del kernel.

El truco del kernel consiste en inventar una dimensión nueva en la que podamos encontrar un hiperplano para separar las clases.

Algunas aplicaciones de las máquinas de vectores de soporte
Las máquinas de vectores de soporte eran muy utilizadas antes de la era del aprendizaje profundo. Para muchas aplicaciones se prefería el uso de SVM en lugar 
de redes neuronales. La razón era que las matemáticas de los SVM se entienden muy bien y la propiedad de obtener el margen de separación máximo era muy atractivo. 

Algunos casos de éxito de las máquinas de vectores de soporte son:

-Reconocimiento óptico de caracteres
    -El OCR(Reconocimiento óptico de caracteres) es una tecnología transversal, aplicable en distintos ámbitos y sectores para la digitalización de formularios, 
     documentos administrativos, informes, etc., ya que las ventajas que ofrece son comunes para todos ellos.
     En el sector de la cultura, por ejemplo, en el ámbito de la preservación del patrimonio, el OCR se aplica principalmente en los procesos de digitalización 
     de documentos históricos, en soporte papel o microformas.
-Detección de caras para que las cámaras digitales enfoquen correctamente
-Filtros de spam para correo electrónico
-Reconocimiento de imágenes a bordo de satélites 
    -Ayuda a saber qué partes de una imagen tienen nubes, tierra, agua, hielo, etc.

Actualmente, las redes neuronales profundas tienen una mayor capacidad de aprendizaje y generalización que los SVM.

<!-- START CRUZ -->
### Ventajas y desventajas de SVC. [CRUZ IBARRA]
### Ventajas 
> - Funciona muy bien con un claro margen de separación. 
> - Es eficaz en espacios de gran dimensión.
>- Es eficaz en los casos en que el número de dimensiones es mayor que el número de muestras.
> - Utiliza un subconjunto de puntos de entrenamiento en la función de decisión (llamados vectores de soporte), por lo que también es eficiente en la memoria.
> <img src="https://www.learnopencv.com/wp-content/uploads/2018/07/svm-linearly-separable-data.png">

### Desventajas
> - No funciona bien cuando tenemos un gran conjunto de datos porque el tiempo de entrenamiento requerido es mayor
> - Tampoco funciona muy bien cuando el conjunto de datos tiene más ruido, es decir, las clases de destino se superponen
<img src="https://1.bp.blogspot.com/-CD6nja2DNDY/VgTft5YhWiI/AAAAAAAADEo/W7eTpexZ0fI/s1600/svm-predicted-classification-3-ring-data-resized-600.png">

> - SVM no proporciona directamente estimaciones de probabilidad, sino que se calculan mediante una costosa validación cruzada cinco veces. Está incluido en el método SVC relacionado de la biblioteca scikit-learn de Python.
<img src="https://i.stack.imgur.com/1fXzJ.png">
<!-- END -->

### Resumen [RENE]
Finalmente, podemos decir que el objetivo principal es segregar el conjunto de datos de la mejor manera posible y que se tiene como objetivo seleccionar un hiperplano con el máximo margen posible entre vectores de soporte en el conjunto de datos dado, siendo los vectores que definen el margen de separación los vectores de soporte. En el caso de contar con clases no separables, se puede utilizar el truco del kernel para añadir una nueva dimensión que permita realizar dicha separación.

### Fuentes de Información

>Eduardo Morales, Jesús González, Hugo Jair Escalante. (2017). Máquinas de Soporte Vectorial. 26/11/2020, de INAOE Sitio web: https://ccc.inaoep.mx/~emorales/Cursos/NvoAprend/Acetatos/svm2017.pdf

>José Martínez Heras. (28/05/2019). Máquinas de Vectores de Soporte (SVM). 26/11/2020, de iartificial.net Sitio web: https://www.iartificial.net/maquinas-de-vectores-de-soporte-svm/

>---. (2020). Máquinas de vectores de soporte. 26/11/2020, de Wikipedia Sitio web: https://es.wikipedia.org/wiki/M%C3%A1quinas_de_vectores_de_soporte


