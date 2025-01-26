### 1. Crear repositorio local y subir a GITHUB

1. Crea una carpeta llamada `UT2.2.a`.
2. Inicializa un repositorio local en la carpeta `UT2.2.a`. ¿Qué comando/s utilizas?
   ```text
    git ini

    ``` 
3. Revisa qué rama se ha creado por defecto. ¿Qué comando/s utilizas?
    ```text
    git branch
    
    ``` 
4. Renombrar la rama por defecto a `main` en caso de que tenga otro nombre. ¿Qué comando/s utilizas?
   ```text
    git branch -M nombrerama main
    
    ``` 
5. Agrega un fichero `README.md`.

   ```markdown
   # UT2.2.a

   ![alt text](image.png)
   ```

6. Agrega el fichero `README.md` al stage area. ¿Qué comando/s utilizas?
   ```text
    git add README.md
    
    
    ``` 

7. Realiza un commit con el mensaje "Add README". ¿Qué comando/s utilizas?
   ```text
   git commit -m "Add README"
    
    ``` 
8. Agrega otro fichero `01.xml` con siguiente texto.

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <libreria>
       <libro>
           <titulo>El Quijote</titulo>
           <autor>Miguel de Cervantes</autor>
           <editorial>Editorial Castalia</editorial>
           <fecha>1605</fecha>
           <genero>Novela</genero>
           <precio>20</precio>
       </libro>
   </libreria>
   ```

9.  Agrega el fichero `01.xml` al stage area y realiza el commit "Add file 01.xml" ¿Qué comando/s utilizas?
    ```text
    git add 01.xml     
    git commit -m "Add file 01.xml"
    ``` 
10. Agrega una nueva rama llamada y posicionate directamente en ella con el mismo comando `fea/wac01`. ¿Qué comando/s utilizas? (busca en internet si no lo recuerdas)
    ```text
    git checkout -b fea/wac01
    
    ``` 
11. En qué rama estas ahora mismo? ¿Qué comando/s utilizas?
    ```text
    git branch
    
    ``` 
12. Estando en la rama `fea/wac01` agrega un fichero `02.xml, y agrega al área de stage y realiza commit "Add file 02".

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>
    ```
    ```text
    git add 02.xml
    git commit -m "Add file 02"
    ``` 

13. Muestra el log utilizando solo una línea por commit con opciones gráficas. ¿Qué comando/s utilizas?
    ```text
   git log --oneline --graph
    
    ``` 
14. Posicionate de nuevo en la rama `main`, y crea otra rama `fea/wac02`, posicionandote directamente en ella. Agrega un fichero `03.xml`, agrega al área de stage y realiza commit "Add file 03".

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```
        ```text
   git checkout main
    git checkout -b fea/wac02
    git add 03.xml
    git commit -m "Add file 03"
    ``` 

15. Posicionate en la rama `main` y muestra los ficheros que hay en el directorio. ¿Qué comando/s utilizas?
    ```text
    git checkout main
    ls
    
    ``` 
16. Realizar un merge de la rama `fea/wac01` en la rama `main`. (Indica los comandos utilizados y explica cada uno de ellos).
    ```text
    git checkout main: Cambia a la rama main para prepararla para el merge.
    git merge fea/wac01: Fusiona los cambios de la rama fea/wac01 en la rama actual (main). Git integrará los commits de fea/wac01 en main. Si no hay conflictos, el merge se realizará de forma automática.
    
    ``` 
17. Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen/gif visualizando los comandos) `adjunta la imagen`
    
![alt text](img/ej17.1.png)
![alt text](img/ej17.2.png)
![alt text](img/ej17.3.png)
19. Elimina la rama `fea/wac01` sin posibilidad de recuperación. ¿Qué comando/s utilizas?
    ```text
    git branch -D fea/wac01
    
    ``` 
20. Realiza un merge de la rama `fea/wac02` en la rama `main`.
    ```text
    git checkout main
    git merge fea/wac02
    ``` 
21. Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen) `adjunta la imagen`

![alt text](img/ej18.1.png)

21. Vuelve a la rama `fea/wac02` y modifica el fichero `03.xml` añadiendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```
  ```text
    git checkout fea/wac02
    git commit -m "Añadir nuevo libro en 03.xml"
    ``` 
    Agrega al área de stage y realiza commit "Update 03 file. Add book El Silmarillion".

22. Posicionate en la rama `main`, muestra el estado y muestra el contenido del fichero `cat 03.xml`. (Imagen visualizando comandos) `adjunta la imagen`
![alt text](img/ej22.png)

23. Realiza un merge de la rama `fea/wac02` en la rama `main`. ¿Qué comando/s utilizas?
    ```text
    git checkout main
    git merge fea/wac02
    ``` 
24. Muestra el estado del repositorio, y muestra el contenido del fichero `03.xml`. (Imagen visualizando comandos) `adjunta la imagen`
![alt text](img/ej24.png)

25. Ahora, en la rama `main` modifica el fichero `03.xml` incluyendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>
    ```

    Agrega al área de stage y realiza commit "Update 03 file. Add book El Hobbit".

    ```text
     git add 03.xml
    git commit -m "Update 03 file. Add book El Hobbit"
    "He modificado el segundo libro aqui porque me he dado cuenta que el segundo libro agregue el mismo que el primero". // Respuesta
    
    ``` 

26. Agrega un nuevo fichero `04.xml` sobre libros ciencia-ficcion, en la rama `main`.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El fin de la eternidad</titulo>
            <autor>Isaac Asimov</autor>
            <editorial>Edhasa</editorial>
            <fecha>1955</fecha>
            <genero>Ciencia ficción</genero>
            <precio>20</precio>
        </libro>
    </liberia>
    ```

    Agrega al área de stage y realiza commit "Add 04 file. Add cienca-ficcion books".

    ```text
   git add 04.xml
    git commit -m "Add 04 file. Add ciencia-ficcion books"
    
    ``` 

27. Muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) `adjunta la imagen`
    ![alt text](img/ej27.png)
28. Vuelve un commit atrás, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) `adjunta la imagen`
    ![alt text](img/ej28.png)
29. Vuelve al commit anterior, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) `adjunta la imagen`
    ![alt text](img/ej29.png)
30. Posicionate de nuevo en el último commit, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) `adjunta la imagen`
![alt text](img/ej30.png)
### 2. Crear repositorio remoto y subir a GITHUB

1. Crea un repositorio remoto en GITHUB llamado `EEDD_{NombreApellido}_TE2.2` público, vacio, sin nada.
2. Agrega el repositorio remoto a tu repositorio local. ¿Qué comando/s utilizas?
   ```text
    // Respuesta
    
    ``` 
3. Muestra los repositorios remotos que tienes configurados. ¿Qué comando/s utilizas?
   ```text
    // Respuesta
    
    ``` 
4. Sube la rama `main` al repositorio remoto. ¿Qué comando/s utilizas?
   ```text
    // Respuesta
    
    ``` 
5. Muestra el log de la rama `main` con opciones gráficas. ¿Qué comando/s utilizas?
   ```text
    // Respuesta
    
    ``` 
6. Posicionate en la rama `fea/wac02` y sube la rama `fea/wac02` al repositorio remoto. ¿Qué comando/s utilizas?
   ```text
    // Respuesta
    
    ``` 

7. Ahora desde GITHUB (web) en la rama `fea\wac02`, modifica el fichero `03.xml` añadiendo un nuevo libro.

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <libreria>
       <libro>
           <titulo>El Señor de los Anillos</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1954</fecha>
           <genero>Fantasía</genero>
           <precio>25</precio>
       </libro>
       <libro>
           <titulo>El Silmarillion</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1977</fecha>
           <genero>Fantasía</genero>
           <precio>25</precio>
       </libro>
       <libro>
           <titulo>El Hobbit</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1937</fecha>
           <genero>Fantasía</genero>
           <precio>15</precio>
       </libro>
       <libro>
           <titulo>El hombre bicentenario</titulo>
           <autor>Isaac Asimov</autor>
           <editorial>Edhasa</editorial>
           <fecha>1976</fecha>
           <genero>Ciencia ficción</genero>
           <precio>20</precio>
   </libreria>
   ```

   Realiza un commit con el mensaje "Update 03 file. Add book El hombre bicentenario".
   (Muestra pantallazo de GITHUB con el commit realizado) `adjunta la imagen`

8. Ahora obten los cambios sin acualizar el repositorio local (`git fetch origin`).
9.  Muestra un log del repositorio local con opciones gráficas. (Incluye imagen) `adjunta la imagen`
    
10. Ahora actualiza el repositorio local con los cambios del repositorio remoto (`git pull origin fea/wac02`).
    
11. Muestra un log del repositorio local con opciones gráficas. (Incluye imagen) `adjunta la imagen`

12. Haz un merge de la rama `fea/wac02` en la rama `main`. Muestra estado, log, y el contenido fichero `03.xml` (Incluye imagen) `adjunta la imagen`
13. Sube la rama `main` al repositorio remoto. ¿Qué comando/s utilizas?
    ```text
    // Respuesta
    
    ``` 
14. Elimina la rama local `fea/wac02` sin posibilidad de recuperación. ¿Qué comando/s utilizas?
    ```text
    // Respuesta
    
    ``` 
15. Elimina la rama remota `fea/wac02` sin posibilidad de recuperación (git push origin --delete fea/wac02).
    ```text
    // Respuesta
    
    ```
16. Muestra desde GITHUB (navegador web) las ramas que tienes el en repositorio remoto. (Incluye imagen) `adjunta la imagen`
17. Para finalizar, muestra el log del repositorio local con opciones gráficas. (Incluye imagen) `adjunta la imagen`

### 3. Enlace repositorio remoto

1. Incluye el enlace al repositorio remoto en este punto para que el profesor pueda acceder a él.
   ```text
    // Enlace al repositorio remoto (en que aparece en la URL del navegador)
    
    ``` 
