# C++ Video Catalog Management System

Este es un proyecto de gestión de catálogo de videos desarrollado en C++. El sistema permite a los usuarios interactuar con una colección de películas y series, incluyendo la visualización, calificación y filtrado de contenido.

El proyecto está diseñado para demostrar la aplicación de **Principios de Programación Orientada a Objetos (POO)** como **herencia** y **polimorfismo**, así como el manejo de **memoria dinámica** y **lectura de archivos**.

## Funcionalidades Principales

* **Cargar Catálogo**: Lee y procesa un catálogo de videos desde un archivo de texto (`videos.txt`). El sistema distingue entre películas y series/episodios.
* **Mostrar Catálogo**: Permite a los usuarios ver el listado completo de videos disponibles.
* **Calificar Videos**: Los usuarios pueden asignar una calificación de 1 a 5 a cualquier video. El sistema calcula y muestra el promedio de las calificaciones.
* **Filtrar por Calificación**: Muestra videos que superan una calificación promedio mínima especificada por el usuario.
* **Filtrar por Género**: Muestra videos de un género específico que el usuario puede buscar.

## Estructura del Proyecto

El proyecto está organizado en múltiples archivos, cada uno con una responsabilidad específica:

* **`main.cpp`**: Contiene el menú principal y la lógica de la interfaz de usuario. Llama a las funciones para cargar, mostrar, calificar y filtrar videos.
* **`Video.h` y `Video.cpp`**: Define la clase base abstracta `Video`. Esta clase maneja las propiedades comunes a todas las piezas de contenido, como ID, nombre, duración y calificaciones.
* **`Pelicula.h` y `Pelicula.cpp`**: Define la clase `Pelicula`, que hereda de `Video`.
* **`Capitulo.h` y `Capitulo.cpp`**: Define la clase `Capitulo`, que hereda de `Video`.
* **`Serie.h` y `Serie.cpp`**: Define la clase `Serie`, que gestiona una colección de objetos `Capitulo`.
* **`videos.txt`**: Un archivo de texto que sirve como base de datos para cargar los datos del catálogo.

## Tecnologías y Conceptos Clave

* **C++11/14**: El proyecto utiliza características modernas de C++.
* **Programación Orientada a Objetos (POO)**: Utiliza **herencia** para modelar la relación entre `Video`, `Pelicula` y `Capitulo`. El **polimorfismo** se utiliza para manejar diferentes tipos de videos a través de punteros a la clase base.
* **Manejo de Memoria Dinámica**: El programa hace uso de **punteros** y `new`/`delete` para crear objetos dinámicamente y gestionar la memoria, con especial atención a la prevención de fugas de memoria.
* **Manejo de Archivos (File I/O)**: Utiliza librerías como `fstream` y `sstream` para leer y parsear los datos del archivo `videos.txt`.
* **`dynamic_cast`**: Emplea `dynamic_cast` para realizar conversiones de tipo seguras en tiempo de ejecución, por ejemplo, al filtrar por tipo de video.

## Cómo Compilar y Ejecutar

1.  Asegúrate de tener un compilador de C++ (como g++) instalado.
2.  Navega al directorio del proyecto en tu terminal.
3.  Compila el proyecto con el siguiente comando:
    ```bash
    g++ -o proyecto ProyectoEmi.cpp Capitulo.cpp Pelicula.cpp Video.cpp Serie.cpp
    ```
4.  Ejecuta el programa compilado:
    ```bash
    ./proyecto
    ```

## Contribuciones
Las sugerencias y pull requests son bienvenidas.

---
