# Documentación Técnica: Tarjeta de Presentación Digital

Este documento describe las decisiones de desarrollo y la arquitectura semántica aplicada en el proyecto `proyecto_final_clase.html`, bajo los estándares de **HTML5**.

---

## 1. Decisiones Semánticas (Justificación)

En lugar de utilizar etiquetas genéricas de presentación, se han seleccionado etiquetas con **valor significativo** para mejorar la accesibilidad (lectores de pantalla) y el posicionamiento (SEO).

* **`<header>`**: Se eligió para agrupar el nombre y el eslogan, estableciendo la identidad del documento desde el inicio.
* **`<main>`**: Define el contenido central de la página. Indica al navegador que este es el bloque de información principal, excluyendo encabezados o pies de página repetitivos.
* **`<section>`**: Utilizada para dividir el contenido de `main` en unidades temáticas lógicas: "Sobre mí" y "Habilidades/Pasatiempos".
* **`<time>`**: Se aplicó con el atributo `datetime` para que la fecha sea legible tanto para humanos como para algoritmos de búsqueda.
* **`<strong>` y `<em>`**: Se usaron para dar énfasis real. `<strong>` para conceptos de importancia técnica y `<em>` para el tono personal del eslogan.
* **`<address>`**: Es la forma semántica correcta de encerrar la información de contacto, indicando que los datos allí expuestos pertenecen al autor del documento.

---

## 2. Árbol DOM (Estructura Jerárquica)

A continuación, se representa visualmente la jerarquía de los elementos en el documento:



```text
Document (HTML)
└── head (Metadatos y Estilos)
└── body
    ├── header
    │   ├── h1 (Nombre)
    │   └── p > em (Eslogan)
    ├── main
    │   ├── section (Sobre mí)
    │   │   ├── h2
    │   │   └── p (incluye strong y time)
    │   └── section (Habilidades y Pasatiempos)
    │       ├── h2
    │       ├── h3
    │       ├── ul > li (Lista de habilidades)
    │       └── p (Pasatiempos con strong)
    └── footer
        └── address (Email y Ubicación)
            └── small (Copyright)