# Laboratorio-2-CVDS
## Patterns - Factory
## La herramienta Maven

1. **Ingresar a la página de la herramienta y entender:**
    * **Cuál es su mayor utilidad** : Es una herramienta que ahora se puede usar para construir y administrar cualquier proyecto basado en Java.
    * **Fases de maven :
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
## Crear un proyecto con Maven
1. Buscar cómo se crea un proyecto maven con ayuda de los arquetipos (archetypes).
2. Busque cómo ejecutar desde línea de comandos el objetivo "generate" del plugin "archetype", con los siguientes parámetros:
    * Grupo: edu.eci.cvds
    * Id del Artefacto: Patterns
    * Paquete: edu.eci.cvds.patterns
    * archetypeArtifactId: maven-archetype-quickstart
