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
7. CLASE SEIS
8. CLASE SIETE

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
