# **DOCUMENTACIÓN DEL CURSO GIT - GITHUB**
##### ¿Qué y para quién es esta documentación?
##### Esta es una guía práctica y **básica** para que cualquier individuo interesado en aprender git y git-hub tenga una herramienta de aprendizaje y consulta útil a la mano. 
## ÍNDICE
1. INTRODUCCIÓN 
2. CLASE UNO
    - Conceptos básicos
    - Instalación de git
    - Primeros pasos con repositorios
    - Comandos básicos
      - git init
      - git add
      - git commit
      - git log
3. CLASE DOS
    - Comandos varios
      - git branch
      - git branch ""
      - git checkout ""
      - git merge ""
      - git config
        - user name
        - email
        - varios
    - File explorer y las ramas
    - Conlfictos
4. CLASE TRES
    - Ramas
    - Comandos **git merge**
    - git pull-request
5. CLASE CUATRO
    - Introducción a GitHub
    - Comandos relevantes
      - git clone
      - git pull, etc.
6. CLASE CINCO
    - Flujo de trabajo en equipos
      - Basic Workflow
      - Future Branch Workflow
      - Gitflow Workflow
      - Forking Workflow


___

## CONCEPTOS BÁSICOS
Cuando trabajamos en proyectos existe la necesidad de mantener un orden, registro y respaldo, ya que trabajar sin estos componentes sería un riesgo enorme para el éxito de cualquier proyecto que abordemos, es entonces cuando entran los sistemas de control de versiones.

El control de versiones es un sistema que registra los cambios en un proyecto, facilitando la gestión, colaboración y seguimiento de su evolución.
 Hay dos tipos principales: **centralizados** y **distribuidos**. 
 
 **Sistemas de control de versiones centralizados**
Almacenan un único repositorio central donde se guardan todas las versiones del proyecto.
Los usuarios trabajan en copias locales del repositorio y, posteriormente, deben sincronizar sus cambios con el repositorio central.
Ejemplos: Subversion, CVS, Mercurial.

**Sistemas de control de versiones distribuidos**
Cada usuario tiene una copia completa del repositorio en su computadora.
No existe un repositorio central único.
Los cambios se sincronizan entre los repositorios de los diferentes usuarios mediante un proceso de "push" y "pull".
Ejemplos: Git, Mercurial (en modo distribuido), DVCS.

Es aquí donde entra git.
**Entonces, ¿Qué es Git?**
Git es un sistema de control de versiones distribuido que te permite realizar un seguimiento de los cambios en tus proyectos de software y colaborar con otros desarrolladores.

## INSTALACIÓN DE GIT
[Este es el link del sitio oficial para descargar](https://git-scm.com/downloads"Página oficial")

![Imagen del sitio oficial de git]("C:\Users\DELL\Pictures\Screenshots\Captura de pantalla 2024-05-07 164358.png")

# 1 INTRODUCCIÓN

Git es un sistema de control de versiones distribuido diseñado para facilitar el seguimiento de los cambios en los archivos de un proyecto a lo largo del tiempo. Permite a los desarrolladores colaborar en proyectos de software de manera eficiente y controlar las diferentes versiones de su código.

En Git, los desarrolladores trabajan en un repositorio, que es un directorio que contiene todos los archivos de un proyecto y su historial de cambios. Cada vez que se realiza una modificación en los archivos del proyecto, Git registra esos cambios en un "commit", que es una instantánea del estado de los archivos en ese momento. Esto permite a los desarrolladores revisar el historial de cambios, volver a versiones anteriores del código y colaborar en equipo de manera efectiva.

Git también facilita la colaboración entre desarrolladores a través de repositorios remotos, como GitHub o GitLab. Estos repositorios remotos actúan como copias centrales del proyecto, donde los desarrolladores pueden compartir su trabajo, colaborar en equipo y realizar un seguimiento de los cambios realizados por otros colaboradores.

# 2. CLASE UNO

## Comandos básicos
**git init**: Este comando se utiliza para crear un nuevo repositorio Git en un directorio local. Cuando ejecutamos git init, se crea un nuevo subdirectorio .git en el directorio actual, que contiene todos los archivos necesarios para el repositorio Git.

**git add**: Git utiliza un área de preparación (también conocida como "staging area") para preparar los cambios que se incluirán en el próximo commit. git add se utiliza para agregar archivos al área de preparación. Puedes agregar archivos específicos o todos los archivos modificados.

**git commit**: Después de agregar los archivos al área de preparación con git add, el comando git commit se utiliza para crear un nuevo commit que registre los cambios. Cada commit en Git tiene un mensaje asociado que describe los cambios realizados en ese commit. Se suele usar el flag -m para añadir un mensaje directamente desde la línea de comandos (git commit -m "mensaje del commit").

**git log**: Este comando muestra un historial de commits en la rama actual. Proporciona información detallada sobre cada commit, como el autor, la fecha y hora, y el mensaje del commit. git log muestra los commits más recientes.

# 3. CLASE DOS
**git branch**: En Git, una rama (branch) es esencialmente una línea de desarrollo independiente. 
Cada rama representa una versión separada del código base de un proyecto.
 Al crear una rama, puedes trabajar en nuevas características, arreglar errores o realizar cambios sin afectar directamente la rama principal del proyecto (generalmente llamada "master" o "main").
 Esto es útil para trabajar en paralelo con otros desarrolladores o para experimentar sin comprometer el código principal.

**git branch <nombre_rama>**: Este comando se utiliza para crear una nueva rama con el nombre especificado a partir de la ubicación actual del repositorio.

**git checkout <nombre_rama>**: Desplaza el repositorio a la rama especificada, lo que significa que todos los cambios posteriores que realices se aplicarán a esa rama.

**git merge <nombre_rama>**: Combina los cambios de la rama especificada en la rama actual.
Esto suele utilizarse para fusionar una rama de desarrollo de vuelta a la rama principal (como "master" o "main") después de completar una función o arreglo de errores en la rama de desarrollo.

**git config**: Git config se utiliza para configurar opciones específicas de Git en tu sistema. Estas opciones pueden ser globales (para todos los repositorios) o específicas de un repositorio. Algunas de las configuraciones comunes incluyen nombre de usuario, dirección de correo electrónico, editor predeterminado, etc.

# 4. CLASE TRES

**Ramas**: Como se mencionó anteriormente, las ramas en Git son líneas de desarrollo independientes que permiten trabajar en diferentes aspectos del proyecto sin afectar directamente la rama principal (generalmente "master" o "main").
Cada rama puede contener cambios, commits y archivos diferentes, lo que facilita la colaboración en equipos y el desarrollo de nuevas funciones de manera aislada.

**Comandos git merge**: Los comandos git merge se utilizan para combinar cambios de una rama a otra.
Cuando ejecutas git merge, estás integrando los cambios de una rama (llamada rama fuente) en otra rama (llamada rama de destino).
Esto suele hacerse después de completar el trabajo en una rama de función o una rama de desarrollo y deseas incorporar esos cambios en la rama principal del proyecto.

**git merge <nombre_rama>**: Este comando fusiona los cambios de la rama especificada en la rama actual.
Por ejemplo, si estás en la rama "main" y deseas fusionar los cambios de una rama llamada "nueva-caracteristica", ejecutarías git merge nueva-caracteristica.
git pull-request: Un "pull request" es una característica de plataformas de alojamiento de repositorios como GitHub, GitLab o Bitbucket, que permite a los desarrolladores colaborar en el proceso de revisión de código. Un pull request es una solicitud para que los cambios realizados en una rama de un repositorio (generalmente una rama de función) se incorporen a otra rama (generalmente la rama principal).

Los pasos típicos para crear un pull request incluyen:
Crear una nueva rama para tu trabajo.
Realizar los cambios necesarios en esa rama.
Hacer push de la rama a tu repositorio remoto.
En la plataforma de alojamiento (por ejemplo, GitHub), ir al repositorio y crear un pull request seleccionando la rama de la que deseas fusionar los cambios y la rama a la que deseas fusionarlos.
Los colaboradores del proyecto pueden revisar tus cambios, hacer comentarios y sugerencias, y finalmente aprobar o rechazar el pull request.
Una vez aprobado, los cambios se fusionan en la rama de destino.

# 5. CLASE CUATRO
## Introducción a GitHub:
GitHub es una plataforma de desarrollo colaborativo basada en Git que permite a los equipos trabajar juntos en proyectos de software.
Proporciona herramientas para gestionar repositorios de código, realizar seguimiento de problemas, revisar código, alojar documentación y mucho más.
Es ampliamente utilizado por desarrolladores de software de todo el mundo y es especialmente popular en proyectos de código abierto.

**Comandos relevantes:**

**git clone**: Este comando se utiliza para clonar un repositorio remoto en tu máquina local. La sintaxis básica es git clone <URL_del_repositorio>, donde <URL_del_repositorio> es la dirección URL del repositorio que deseas clonar.

Ejemplo: git clone https://github.com/ejemplo/repo.git

**git pull**: El comando git pull se utiliza para recuperar los cambios desde un repositorio remoto y fusionarlos con tu rama local. 
Es útil cuando quieres asegurarte de tener la última versión del código en tu máquina.

Ejemplo: git pull origin master

**git push**: Este comando se utiliza para enviar tus cambios locales al repositorio remoto.
Es necesario después de realizar cambios y commits en tu repositorio local y quieres que esos cambios estén disponibles para otros colaboradores del proyecto.

Ejemplo: git push origin master

**git add**: Antes de confirmar (commit) tus cambios en Git, necesitas agregar los archivos modificados o nuevos al área de preparación (staging area) utilizando el comando git add.

Ejemplo: git add archivo_modificado.txt

git commit: El comando git commit toma todos los cambios agregados al área de preparación y los guarda permanentemente en la historia del proyecto como un nuevo commit.
Es importante incluir un mensaje descriptivo que explique los cambios realizados en el commit.

Ejemplo: git commit -m "Agrega nuevas funcionalidades"

**git branch**: Como se explicó anteriormente, git branch se utiliza para crear, listar y gestionar ramas en tu repositorio Git.

# 6. CLASE CINCO
## Basic Workflow:

Este flujo de trabajo es bastante simple y suele ser adecuado para proyectos pequeños o equipos que están comenzando a usar Git.

El flujo básico implica trabajar directamente sobre la rama principal (como "master" o "main").
Los desarrolladores crean ramas locales para trabajar en nuevas características o correcciones de errores.
Después de completar el trabajo en una rama, se fusiona de vuelta a la rama principal.
No hay ramificaciones permanentes para características específicas, y todas las actualizaciones se realizan en la rama principal.

## Feature Branch Workflow:

En este flujo de trabajo, cada nueva característica o tarea se desarrolla en su propia rama independiente.
Los desarrolladores crean una nueva rama para cada característica que están trabajando.
Después de completar la característica, se fusiona de vuelta a la rama principal (generalmente "master" o "main").
Esto permite un desarrollo paralelo de características y facilita la colaboración en equipos grandes.

## Gitflow Workflow:

El flujo de trabajo Gitflow es un modelo más avanzado que se adapta bien a proyectos grandes y complejos.
Define dos ramas principales: master y develop.
Las nuevas características se desarrollan en ramas de características que se ramifican desde develop.
Una vez que una característica está completa, se fusiona nuevamente en develop.
Regularmente, se crea una rama de "release" a partir de develop para preparar versiones estables.
Después de la prueba y la corrección de errores en la rama de "release", se fusiona en master y develop.
Las correcciones de errores se realizan en ramas separadas y se fusionan nuevamente tanto en master como en develop.

## Forking Workflow:

Este flujo de trabajo es común en proyectos de código abierto con múltiples colaboradores.
Cada colaborador crea un "fork" (copia) del repositorio original en su propia cuenta de GitHub.
Luego, realizan cambios en sus propios forks y envían "pull requests" al repositorio original para que los cambios sean considerados.
Los mantenedores del proyecto revisan y aceptan los pull requests, incorporando los cambios al proyecto principal.
