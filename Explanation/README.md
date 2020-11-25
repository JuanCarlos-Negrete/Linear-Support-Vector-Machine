# Linear Support Vector Machine

## TODO: Hoja de presentacion

### Descripción [SALMA]
También son conocidas con el acrónimo SVM por sus siglas en inglés (Support Vector Machines). Se pueden usar tanto para regresión como para clasificación.

Son un conjunto de algoritmos de aprendizaje supervisado desarrollados por Vladimir Vapnik y su equipo en los laboratorios AT&T.

Se puede usar para:
- Clasificación binaria (aplicación original)
- Clasificación multiclase
- Regresión
- Selección de variables
- Identificacion de casos anóomalos (outliers)
- Clustering

### Datos de ejemplo - Regularizacion [FERNANDO]
> TODO: Tema

### Truco del Kernel en SVM - Algunas aplicaciones
El propocito principal del SVM es el formar el hiperplano que maximiza el margen de separación entre clases, sin embargo hay veces en las que no hay forma 
de encontrar una hiperplano que permita separar dos clases. En estos casos decimos que las clases no son linealmente separables. Para resolver este problema 
podemos usar el truco del kernel.

El truco del kernel consiste en inventar una dimensión nueva en la que podamos encontrar un hiperplano para separar las clases.

Algunas aplicaciones de las máquinas de vectores de soporte
Las máquinas de vectores de soporte eran muy utilizadas antes de la era del aprendizaje profundo. Para muchas aplicaciones se prefería el uso de SVM en lugar 
de redes neuronales. La razón era que las matemáticas de los SVM se entiende muy bien y la propiedad de obtener el margen de separación máximo era muy atractivo. 

Algunos casos de éxito de las máquinas de vectores de soporte son:

-Reconocimiento óptico de caracteres
    -El OCR(Reconocimiento optico de caracteres) es una tecnología transversal, aplicable en distintos ámbitos y sectores para la digitalización de formularios, 
     documentos administrativos, informes, etc., ya que las ventajas que ofrece son comunes para todos ellos.
     En el sector de la cultura, por ejemplo en el ámbito de la preservación del patrimonio, el OCR se aplica principalmente en los procesos de digitalización 
     de documentos históricos, en soporte papel o microformas.
-Detección de caras para que las cámaras digitales enfoquen correctamente
-Filtros de spam para correo electrónico
-Reconocimiento de imágenes a bordo de satélites 
    -Ayuda a saber qué partes de una imagen tienen nubes, tierra, agua, hielo, etc.

Actualmente, las redes neuronales profundas tienen una mayor capacidad de aprendizaje y generalización que los SVM.

### Ventajas y desventajas. [MANUEL]
> TODO: Tema

### Resumen [RENE]
> TODO: Tema


### Fuentes de Información

>https://ccc.inaoep.mx/~emorales/Cursos/NvoAprend/Acetatos/svm2017.pdf
>https://www.iartificial.net/maquinas-de-vectores-de-soporte-svm/
>https://es.wikipedia.org/wiki/M%C3%A1quinas_de_vectores_de_soporte
