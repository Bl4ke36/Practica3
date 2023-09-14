Mario Eduardo Pérez Villalobos

Edad: 17

**Foto**: ![a](Yo.jpeg)

[practica5](./Practica-5.md)

**creando la versión 1.0.0 de este repositorio**

---

- ¿Cómo se inicializa un repositorio en Git?

    Lo primero a hacer es configurar el repositorio siguiendo una secuencia de comandos y finalmente inicializarlo con el respectivo comando

    Secuencia de comandos:
    ```bash
    git config --global user.name "Jonathan MirCha"
    git config --global user.email jonmircha@gmail.com
    git config --global user.ui true
    git config --global init.defaultBranch main
    git config --list
    git config --global core.editor "code --wait"
    git config --global -e
    # para windows
    git config --global core.autocrlf true
    # para linux/mac
    git config --global core.autocrlf input 
    git config -h
    # luego de esto sigue el comando para inicializar
    git init
    ```
- ¿Cómo creas un repositorio en GitHub?

    Accedes a GitHub desde tu navegador y en la parte superior del panel de la izquierda hay un boton azúl, al presionarlo abre el panel de creacion de un repositorio
- ¿Cómo vinculas un repositorio local de Git con uno remoto en GitHub?
    
    Esto se hace por medio del enlace que de da el mismo repositorio de GitHub generando la ruta por medio del codigo
    ```bash
    git remote add origin https://github.com/usuario/repositorio.git
    ```
- ¿Cuál es el flujo básico de trabajo en Git y GitHub?

    El flujo basico se maneja por 4 etapas: **modified, staged, commited y remote** cada una tiene un respectivo comando para pasar a la siguiente, la de **modified** que es trabajar directamente en el archivo de la computadora pasa al **staged** que es el registro de cambios, luego este registro pasa a **commited** que es cuando ya se han aplicado los cambios en el repositorio local y finalmente el **remote** cuando estod cambios son guardados en GitHub o servicios similares.
    
    La secuencia de codigo en terminal para hacer esto seria:
    ```bash
    git add .
    git commit -m "mensaje descriptivo"
    #este es usado unicamente cuando se guarda por primera vez en dicha rama del repositorio remoto
    git push -u origin nombre-de-la-rama 
    #una vez hecho el primer push con el comando anterior se usa este comando
    git push 
    ```