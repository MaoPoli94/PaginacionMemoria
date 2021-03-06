===================================
CONSTRUIR DESCRIPCIÓN DE LA SALIDA
===================================

Cuando crea un proyecto de aplicación Java que tiene una clase principal, el IDE
copia automáticamente todo el JAR
archivos en la ruta de clase del proyecto a la carpeta dist / lib de su proyecto. El IDE
también agrega cada uno de los archivos JAR al elemento Class-Path en la aplicación
Archivo de manifiesto de archivos JAR (MANIFEST.MF).

Para ejecutar el proyecto desde la línea de comando, vaya a la carpeta dist y
escriba lo siguiente:

java -jar "MetroOS.jar"

Para distribuir este proyecto, comprima la carpeta dist (incluida la carpeta lib)
y distribuir el archivo ZIP.

Notas:

* Si dos archivos JAR en la ruta de clases del proyecto tienen el mismo nombre, solo el primero
El archivo JAR se copia en la carpeta lib.
* Solo los archivos JAR se copian en la carpeta lib.
Si la ruta de clases contiene otros tipos de archivos o carpetas, estos archivos (carpetas)
no se copian.
* Si una biblioteca en el classpath del proyecto también tiene un elemento Class-Path
especificado en el manifiesto, el contenido del elemento Class-Path debe estar en
la ruta del tiempo de ejecución de los proyectos.
* Para establecer una clase principal en un proyecto estándar de Java, haga clic con el botón derecho en el nodo del proyecto
en la ventana Proyectos y elija Propiedades. Luego haga clic en Ejecutar e ingrese el
nombre de clase en el campo Clase principal. Alternativamente, puede escribir manualmente el
nombre de clase en el elemento Main-Class del manifiesto.