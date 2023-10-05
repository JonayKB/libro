# Libro
Repositorio dedicado para la realización de test con git
# Git Avanzado - Jonay Contreras

1. [Clonado](#clonado)
2. [Ejercicio 1](#ejercicio-1)
3. [Ejercicio 2](#ejercicio-2)
4. [Ejercicio 3](#ejercicio-3)
5. [Ejercicio 4](#ejercicio-4)
6. [Ejercicio 5](#ejercicio-5)
6. [Ejercicio 6](#ejercicio-6)
7. [Ejercicio 7](#ejercicio-7)

## Clonado
```code
git clone https://github.com/jpexposito/libro.git
cd libro
ls -la
```
- ls -la
    - salida:

        ```code
            Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        d-----        05/10/2023      9:10                img
        d-----        05/10/2023      9:10                prueba2
        d-----        05/10/2023      9:10                test
        -a----        05/10/2023      9:12            480 README.md
        ```


## Ejercicio 1
- Mostrar el historial de cambios del repositorio.

- Crear la carpeta capítulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto.

```code
Git es un sistema de control de versiones ideado por Linus Torvalds.
```
- Añadir los cambios a la zona de intercambio temporal.

- Hacer un commit de los cambios con el mensaje Añadido capítulo 1.

- Volver a mostrar el historial de cambios del repositorio.

- __Solución:__

```code
git log
mkdir capitulos
nano capitlos/capitulo1.txt
Git es un sistema de control de versiones ideado por Linus Torvalds.
Ctrl + x
S
Enter
git add .
git commit -m "Añadido capítulo 1"
git log
```

- git log
    - salida:

        ```code
        commit bd404e8ec131d0dce131561bdd64bb963472ff4f
        Author: JonayKB <JonayKB@gmail.com>
        Date:   Wed Oct 4 16:15:21 2023 +0100

            Subido para casa

        commit 1016a8a4e53ee1167750094aaac7d2018063a264
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Wed Sep 27 15:50:15 2023 +0100

            se añade la segunda carpeta

        commit 3f26704336e8d586f91aca272c89218d96e61d98
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Wed Sep 27 15:21:53 2023 +0100

            mensaje

        commit 8a81c55462cc731099b5842f2cd38fbc47105d56
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Mon Oct 10 18:18:08 2022 +0100

            Se añade un título

        commit fbe91b280cfbc50352ee18627a4339d4aa7e91c4
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Mon Oct 10 18:14:01 2022 +0100

            closed #1

        commit 3ea9800cc58f6e37a0ff3e6878bf9cc99dd17ced
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Mon Oct 10 17:58:02 2022 +0100

            se crea la carpeta img #1

        commit 4dcb74b18a32f24061bc2e7c415f09f7aaff4971
        Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
        Date:   Mon Sep 27 11:57:59 2021 +0100
        Initial commit
        ```




- git commit -m "Añadimos capitulos y capitulo1"
    - salida:

        ```code
        [main d381bea] Añadimos capitulos y capitulo1
         2 files changed, 81 insertions(+), 1 deletion(-)
        create mode 100644 capitulos/capitulo1.txt
        ```



- git log
    - salida

        ```code
        commit d381beac569022efd95d3024f9293fbd3b9e3a2d (HEAD -> main)
        Author: jonaykb <jonaykb@gmail.com>
        Date:   Thu Oct 5 09:22:42 2023 +0100

        Añadido capítulo 1
        ```



## Ejercicio 2

- Crear el fichero capitulo2.txt en la carpeta capítulos con el siguiente texto.

```code
El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el 
repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.
```

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje Añadido capítulo 2.
- Mostrar las diferencias entre la última versión y dos versiones anteriores.
- __Solución:__

```code
nano capitulos/capitulo2.txt
El flujo de trabajo básico con Git consiste en: 
1- Hacer cambios en el repositorio. 
2- Añadir los cambios a la zona de intercambio temporal. 
3- Hacer un commit de los cambios.
Ctrl + X
S
Enter
git add .
git commit -m "Añadido capítulo 2"
git diff HEAD~2..HEAD
```

- git commit -m "Añadido capítulo 2"
    - salida

        ```code
        [main 87a952d] Añadido capítulo 2
         2 files changed, 70 insertions(+), 3 deletions(-)
        create mode 100644 capitulos/capitulo2.txt
        ```



- git diff HEAD~2..HEAD
    - salida:

        ```code
        diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
        new file mode 100644
        index 0000000..f4068a7
        --- /dev/null
        +++ b/capitulos/capitulo1.txt
        @@ -0,0 +1 @@

        +Git es un sistema de control de versiones ideado por Linus Torvalds.
        \ No newline at end of file

        diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
        new file mode 100644
        index 0000000..b18ed63
        --- /dev/null
        +++ b/capitulos/capitulo2.txt
        @@ -0,0 +1,4 @@

        +El flujo de trabajo básico con Git consiste en: 
        +1- Hacer cambios en el repositorio. 
        +2- Añadir los cambios a la zona de intercambio temporal. 
        +3- Hacer un commit de los cambios.
        \ No newline at end of file
        ```
## Ejercicio 3
- Crear el fichero capitulo3.txt en la carpeta capítulos con el siguiente texto.

```code
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
```

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje Añadido capítulo 3.
- Mostrar las diferencias entre la primera y la última versión del repositorio.
- __Solución:__

```code
nano capitulos/capitulo3.txt
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
Ctrl + X
S
Enter
git add .
git commit -m "Añadido capítulo 3"
git log
git diff
```


- git commit -m "Añadido capítulo 3"
    - salida:
        ```code
        [main 584ac18] Añadido capítulo 3
        2 files changed, 47 insertions(+), 2 deletions(-)
        create mode 100644 capitulos/capitulo3.txt
        ```
- git diff 4dcb74b18a32f24061bc2e7c415f09f7aaff4971..HEAD
    - salida:



        ```code
        diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
        +
        diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
        new file mode 100644
        index 0000000..f4068a7
        --- /dev/null
        +++ b/capitulos/capitulo1.txt
        @@ -0,0 +1 @@
        +Git es un sistema de control de versiones ideado por Linus Torvalds.
        \ No newline at end of file

        diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
        new file mode 100644
        index 0000000..b18ed63
        --- /dev/null
        +++ b/capitulos/capitulo2.txt
        @@ -0,0 +1,4 @@
        +El flujo de trabajo básico con Git consiste en: 
        +1- Hacer cambios en el repositorio. 
        +2- Añadir los cambios a la zona de intercambio temporal. 
        +3- Hacer un commit de los cambios.
        \ No newline at end of file

        diff --git a/capitulos/capitulo3.txt b/capitulos/capitulo3.txt
        new file mode 100644
        index 0000000..534b9a9
        --- /dev/null
        +++ b/capitulos/capitulo3.txt
        @@ -0,0 +1 @@
        +Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
        \ No newline at end of file

        diff --git a/img/README.md b/img/README.md
        diff --git a/img/README.md b/img/README.md
        diff --git a/img/README.md b/img/README.md
        new file mode 100644
        index 0000000..bfcf422
        --- /dev/null
        +++ b/img/README.md
        @@ -0,0 +1 @@
        +# Título 2
        diff --git a/prueba2/file2.clean b/prueba2/file2.clean
        new file mode 100644
        index 0000000..e69de29
        diff --git a/test/file.clean b/test/file.clean
        new file mode 100644
        index 0000000..e69de29
        ``````

## Ejercicio 4
- Crea el fichero índice.txt la siguiente línea:

```code
Indice de los cápitulos, con conceptos avanzados de git
```

- Añadir los cambios a la zona de intercambio temporal.


- Hacer un commit de los cambios con el mensaje "Indice de los cápitulos, con conceptos avanzados de git.

- Mostrar quién ha hecho cambios sobre el fichero indice.txt.

- __Solución:__

```code
nano indice.txt
Indice de los cápitulos, con conceptos avanzados de git
Ctrl + X
S
Enter
git commit -m "Indice de los cápitulos, con conceptos avanzados de git"
git annotate indice.txt
```
- git commit -m "Indice de los cápitulos, con conceptos avanzados de git"
    - salida:

        ```code
        [main 385db21] Indice de los cápitulos, con conceptos avanzados de git
        2 files changed, 108 insertions(+)
        create mode 100644 indice.txt
        ```

- git annotate indice.txt
    - salida:

        ```code
        385db218        (   jonaykb     2023-10-05 09:50:00 +0100       1)Indice de los cápitulos, con conceptos avanzados de git
        ```

## Ejercicio 5
- Crear una nueva rama bibliografía y mostrar las ramas del repositorio.
- __Solución:__

```code
git branch bibliografia
git branch
```

- git branch
    - salida:

    ```code
      bibliografia
    * main
    ```


## Ejercicio 6
- Crear el fichero capitulos/capitulo4.txt y añadir el texto siguiente:

```code
  En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
```

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit con el mensaje “Añadido capítulo 4.”
- Mostrar la historia del repositorio incluyendo todas las ramas.
- __Solución:__

```code
nano capitulos/capitulo4.txt
En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
Ctrl + X
S
Enter
git add .
git commit -m "Añadido capítulo 4"
git log --graph --all --oneline
```
- git commit -m "Añadido capítulo 4"
    - salida:

        ```code
        [main 49f8132] Añadido capítulo 4
        2 files changed, 57 insertions(+), 1 deletion(-)
        create mode 100644 capitulos/capitulo4.txt
        ```

- git log --graph --all --oneline
    - salida:

        ```code
        * 49f8132 (HEAD -> main) Añadido capítulo 4
        * 385db21 (bibliografia) Indice de los cápitulos, con conceptos avanzados de git
        * 584ac18 Añadido capítulo 3
        * 87a952d Añadido capítulo 2
        * d381bea Añadimos capitulos y capitulo1
        * 1016a8a se añade la segunda carpeta
        * 3f26704 mensaje
        * 8a81c55 Se añade un título
        * fbe91b2 closed #1
        * 3ea9800 se crea la carpeta img #1
        * 4dcb74b Initial commit
        ```

## Ejercicio 7
- Cambiar a la rama bibliografía.
- Crear el fichero bibliografia.txt y añadir la siguiente referencia:

```code
Chacon, S. and Straub, B. Pro Git. Apress.
```

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”
- Mostrar la historia del repositorio incluyendo todas las ramas.
- __Solución:__

```code
git checkout bibliografia
git nano bibliografia.txt
Chacon, S. and Straub, B. Pro Git. Apress.
Ctrl + X
S
Enter
git add .
git commit -m "Añadida primera referencia bibliográfica."
git log --graph --all --oneline
```