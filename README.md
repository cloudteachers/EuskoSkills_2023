<img src="https://raw.githubusercontent.com/cloudteachers/EuskoSkills_2023/main/euskoskills_logo.jpg" alt="EuskoSkills logo"/>

# EuskoSkills 2023
En este repositorio se puede encontrar la documentación realizada para la categoría **53 - Cloud Computing** utilizada en EuskoSkills 2023, competición celebrada en Irún entre el 9 y el 11 de Mayo del 2023.

## Competición
La competición en esta categoría estuvo formada por un total de 4 pruebas, realizadas de la siguiente manera:
 * **Prueba 1**: 1,5 horas de duración realizada la tarde del 9 de mayo. 
 * **Prueba 2**: 3 horas de duración realizada la mañana del 10 de mayo.
 * **AWS Jam Session**: 3 horas de duración realizada la tarde del 10 de mayo. Esta Jam fue realizada por AWS, y por tanto se auto-corregía.
 * **Prueba 3**: 3 horas de duración realizada la mañana del 11 de mayo.

Las tres pruebas realizadas están en este repositorio en formato PDF (y dentro del directorio [documentos](./documentos) en formato editable). Estas pruebas fueron realizadas por:

* **Rubén Gómez Olivencia**: CIFP Elorrieta-Errekamari LHII. Tutor y coordinador de esta categoría.
* **Ainara Montoya**: CIFP Ciudad Jardín LHII. Tutora.
* **Iñigo Aramendi Inchauspe**: IES Xabier Zubiri Manteo BHI. Tutor.

## Documentos
En el directorio [documentos](./documentos) se puede encontrar lo siguiente:
* Pruebas realizadas en formato **.odt** editables en LibreOffice.
* Imagen **pruebas.png** con la infraestructura utilizada para cada una de las pruebas.
* Fichero **pruebas.drawio** que es la imagen pruebas.png editable a través de [Draw.io](https://draw.io/)
* Rúbrica de corrección utilizada para las distintas pruebas.


### Rúbrica
La rúbrica realizada para la corrección está dividida por pruebas y dentro de cada una de ellas por "secciones".

Cada sección cuenta con un conjunto de apartados con su puntuación correspondiente, y al inicio de cada sección el total de puntos que suman los apartados. Cada una de estas secciones han sido añadidas a los documentos para que los participantes tuviesen la información de cómo iban a ser corregidas las distintas pruebas.

Los puntos de las pruebas hacían un total de 80 puntos, y la **AWS Jam** constaba de 400 puntos, que en la rúbrica fue dividida entre 20 para hacer un total de 100 puntos.

Para realizar la corrección de cada apartado a cada alumno es suficiente con ponerle en la celda correspondiente un "1" para indicar que lo ha realizado correctamente o "0" para indicar que no. Con ello se realizará la suma en cada sección teniendo en cuenta la puntuación de cada apartado.

Esta rúbrica ha sido diseñada en modo "binario", o el apartado está bien o está mal, por lo tanto se suma la totalidad de puntos del apartado o nada.

Al final de la rúbrica hay un apartado para calcular los tiempos. En la sección correspondiente se ha de añadir la hora de inicio de la prueba, y para cada estudiante se indicará la hora de finalización de cada prueba. De esta manera se obtendrá el tiempo total utilizado para todas las pruebas, que sería utilizado en caso de empate en la puntuación (ganando el que menos tiempo haya utilizado).

## Aspectos a mejorar
Al ser la primera vez que se realizaban este tipo de pruebas y la competición, y a pesar de haber tratado de no cometer errores, durante la competición ha habido distintas situaciones que deberían ser tenidas en cuenta para futuras ediciones. A continuación se indican varios de estos aspectos:

### Pruebas 
Las pruebas fueron realizadas pensando en ser heterogéneas y que cubriésen distintos apartados del mundo Cloud. Quizá para futuras ediciones se pueden modificar ciertos aspectos como:
* **Prueba 1**: Es una prueba sencilla que después es utilizada en la prueba 2. Quizá sería conveniente realizar una prueba más compleja dentro del apartado VPC, y que luego no sea utilizada en pruebas posteriores.
* **PHP y acceso a base de datos**: En dos pruebas se ha exigido crear código PHP que acceda a una base de datos para obtener y mostrar los datos. Aunque en esta competición sólo un competidor consiguió realizar este apartado en la prueba 3 (a pesar de que se creía que era uno de los apartados más sencillos a realizar), sería recomendable no repetir apartados en pruebas distintas, ya que puede favorecer/penalizar a los participantes.
* **Importar dumps de bases de datos**: Similar al caso anterior, este aspecto se repite en dos apartados. Aparte, durante la competición el segundo dump tenía un _charset_ distinto al que tiene por defecto en MariaDB, lo que daba error. En este caso, habría que pensar si es el competidor el que debe arreglar dichos fallos o no.

### Rúbrica
A pesar de haber tratado de hacer una rúbrica lo más objetiva y estricta posible, durante las correcciones hubo ciertos aspectos que generaron dudas, y que por tanto se tuvo que llegar a un consenso. Algunos de estos fueron:
* **Security Groups**: En la rúbrica se especifica en varios apartados "Tiene un security group propio llamado 'xxx' que sólo permite YYY". Esto da lugar a confusión durante la correción en los casos en los que existen más security groups que permiten más opciones que las especificadas. Debería modificarse por algo del estilo "Sólo tiene un security group llamado 'xxx' que sólo permite YYY".
* **Definir "funciona"**: Existe un apartado de la rúbrica donde se indica "La aplicación exigida está instalada y funciona correctamente" que puede dar lugar a confusión. En el caso de la competición se realizó la instalación de Wordpress, y en algunos casos los participantes no terminaron el asistente de instalación (en un caso no tenía la base de datos desplegada, y en otro sí). Por lo tanto, en este caso habría que modificar este apartado por algo del estilo "La aplicación exigida está instalada, desplegada y con la configuración realizada para que un **usuario no administrador** pueda visualizarla y utilizarla".
* **Dobles penalizaciones**: A pesar de haber tratado de evitar las dobles/múltiples penalizaciones, existe alguna. En la prueba 3, en el apartado del balanceador existe la posibilidad de hacer doble penalizaciones.

## Para futuras ediciones
Con todo lo dicho en el apartado anterior, para futuras ediciones se podrían tener en cuenta añadir lo siguiente en distintas pruebas:

* **Autoescalado en balanceador**: Mejorar la "Prueba 3" añadiendo que el balanceador autoescale el número de instancias que hay detrás de él cuando el uso medio de las CPUs supere un porcentaje.
* **Elastic Beanstalk**: Despliegue utilizando esta herramienta de AWS.
* **ECS/ECR/EKS**: Crear contenedores y levantarlos a través de los servicios propios de AWS en lugar de utilizar Docker en la instancia.
* **Uso de Alta Disponibilidad de RDS**: Hacer uso de las posibilidades de crear clústers en RDS.
* **Monitorización con CloudWatch**: Uso de las distintas posibilidades que ofrece CloudWatch para crear alertas de monitorización o para crear paneles para visualizar métricas de las instancias/servicios.
* **Exigir el uso del CLI**: Durante las pruebas realizadas se pidió hacer uso de un backup a S3, por lo que era necesario hacer uso del CLI. Quizá sería conveniente añadir alguna prueba más del estilo.
* **Despliegue automatizado**: Sería buena idea hacer algún apartado que use de alguna herramienta de despliegue automatizado como **Terraform**.
