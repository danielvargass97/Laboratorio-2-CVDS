# Laboratorio-2-CVDS
## Patterns - Factory
## La herramienta Maven

1. **Ingresar a la página de la herramienta y entender:**
    * **Cuál es su mayor utilidad** : Es una herramienta que ahora se puede usar para construir y administrar cualquier proyecto basado en Java.
    * **Fases de maven** :
      * validar : validar que el proyecto es correcto y toda la información necesaria está disponible
      * compilar : compila el código fuente del proyecto
      * prueba : prueba el código fuente compilado usando un marco de prueba de unidad adecuado. Estas pruebas no deberían requerir que el código se empaquete o implemente
      * paquete : tome el código compilado y empaquételo en su formato distribuible, como un JAR.
      * prueba de integración : procese e implemente el paquete si es necesario en un entorno donde se puedan ejecutar pruebas de integración
      * verificar : ejecutar cualquier verificación para verificar que el paquete sea válido y cumpla con los criterios de calidad
      * instalar : instala el paquete en el repositorio local, para usarlo como dependencia en otros proyectos localmente
      * despliegue : hecho en un entorno de integración o lanzamiento, copia el paquete final en el repositorio remoto para compartirlo con otros desarrolladores y proyectos.
      * clean : limpia los artefactos creados por compilaciones anteriores
      * sitio : genera documentación del sitio para este proyecto 
    * **Ciclo de vida de la construcción** : Hay tres ciclos de vida de compilación integrados: predeterminado, limpio y de sitio. El defaultciclo de vida maneja la implementación del proyecto, el cleanciclo de vida maneja la limpieza del proyecto, mientras que el siteciclo de vida maneja la creación de la documentación del sitio de su proyecto.
    * **Para qué sirven los plugins** : Maven es, en esencia, un marco de ejecución de plugins; Todo el trabajo se realiza mediante plugins. Los plugins de compilación se ejecutarán durante la compilación y deben configurarse en el <build/> elemento desde el POM.
Los plugins de informe se ejecutarán durante la generación del sitio y deben configurarse en el <reporting/>elemento desde el POM. Debido a que el resultado de un plugin de informe es parte del sitio generado, los plugin de informes deben ser tanto internacionalizados como localizados.
    * **Qué es y para qué sirve el repositorio central de maven** : El repositorio central de Maven es un sitio web donde se guardan todos los archivos Java. Puede buscar los jars que necesita allí. Cuando busque los archivos jar necesarios, puede incluir los archivos jar usando pom.xml o descargar directamente los archivos jar y agregarlos a su proyecto java.
## Ejercicio de las Figuras
## Compilar y Ejecutar
* Busque cuál es el objetivo del parámetro "package" y qué otros parámetros se podrían enviar al comando mvn: mvn package:  empaqueta el proyecto (si es un proyecto java simple, genera un jar, si es un proyecto web, un war, etc…)
* Busque cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass". Tip: https://www.mojohaus.org/exec-maven-plugin/usage.html:  mvn exec:java -Dexec.mainClass="com.example.Main" [-Dexec.args="argument1"] ...
## Hacer el esqueleto de la aplicacion
* Ejecute múltiples veces la clase ShapeMain, usando el plugin exec de maven con los siguientes parámetros y verifique la salida en consola para cada una:

   * Sin parámetros
   * Parámetro: qwerty
   * Parámetro: pentagon
   * Parámetro Hexagon
* ¿Cuál(es) de las anteriores instrucciones se ejecutan y funcionan correctamente y por qué?
   * Sin parámetros: Muestra la excepcion declarada en el main, que se debe ingresar siempre un parametro.
   * Parámetro: qwerty: Parameter 'qwerty' is not a valid RegularShapeType
   * Parámetro: pentagon :Parameter 'pentagon' is not a valid RegularShapeType ---- 
   * Parámetro: Pentangon :Successfully created a Pentagon with 5 sides.
   * Parámetro Hexagon :Successfully created a Hexagon with 6 sides.
## Entregar
   * Investigue para qué sirve "gitignore" y cómo se usa. Para futuras entregas, debe estar configurado. : Sirve para decirle a Git qué archivos o directorios completos debe ignorar y no subir al repositorio de código.

Su implementación es muy sencilla, por lo que no hay motivo para no usarlo en cualquier proyecto y para cualquier nivel de conocimientos de Git que tenga el desarrollador. Únicamente se necesita crear un archivo especificando qué elementos se deben ignorar y, a partir de entonces, realizar el resto del proceso para trabajo con Git de manera habitual.
