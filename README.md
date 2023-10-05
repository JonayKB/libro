# Libro
Repositorio dedicado para la realización de test con git
# Git Avanzado - Jonay Contreras

1. [Clonado](#clonado)
2. [Ejercicio 1](#ejercicio-1)
3. [Ejercicio 2](#ejercicio-2)

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
```

- git commit -m "Añadido capítulo 2"
    - salida

        ```code
        
        ```