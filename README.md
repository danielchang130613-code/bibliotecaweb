📚 Biblioteca Digital
Aplicación web de una sola página (SPA) para gestionar el catálogo de una biblioteca: libros, préstamos, devoluciones e historial. Construida con HTML, CSS y JavaScript puros, sin frameworks ni librerías externas.

📋 Descripción
Biblioteca Digital permite:

📖 Explorar un catálogo de libros con búsqueda, filtros y ordenamiento.

🔖 Prestar libros a personas (máximo 3 préstamos activos) y registrar devoluciones.

📊 Consultar un resumen estadístico de la biblioteca.

🌗 Cambiar entre tema claro y oscuro.

💾 Persistir todos los datos en el navegador (localStorage).

La aplicación arranca con 8 libros iniciales (2 de colección) y 4 préstamos (2 activos —uno vencido— y 2 devueltos —uno con retraso—) para que el historial no empiece vacío.

🚀 Demo
Una vez publicado con GitHub Pages, la URL será algo como:
https://tu-usuario.github.io/biblioteca/

🛠️ Tecnologías utilizadas
Tecnología	Uso
HTML5	Estructura semántica (<header>, <nav>, <main>, <section>, <article>)
CSS3	Variables, Flexbox, Grid, transiciones, animaciones, temas claro/oscuro, responsive mobile-first
JavaScript (ES6+)	Manipulación del DOM, eventos, localStorage, lógica de negocio separada de la UI
Google Fonts	Tipografía Inter
Sin dependencias externas. Sin frameworks. Sin librerías.

📁 Estructura del proyecto
text
biblioteca/
├── index.html      ← Estructura HTML (4 vistas + 2 modales)
├── styles.css      ← Estilos, temas y responsive
├── script.js       ← Toda la lógica (datos, negocio, UI, eventos)
└── README.md       ← Este archivo
Organización interna de script.js
El archivo está dividido en 4 secciones bien comentadas:

DATOS — Inicialización, localStorage, funciones de fecha.

LÓGICA DE NEGOCIO — Reglas del modelo (prestar, devolver, validar, filtrar, ordenar, resumir). No toca el DOM.

UI — Renderizado del catálogo, préstamos, historial y resumen.

MAIN — Conexión de eventos, navegación entre vistas y arranque.

🎯 Funcionalidades
Vista 1 — Catálogo
Tarjetas generadas dinámicamente con título, autor, año, género y estado.

Búsqueda por título o autor (ignora tildes y mayúsculas).

Filtros por estado: Todos / Disponibles / Prestados.

Filtro por género y ordenamiento por título, autor o año (asc/desc).

Contador "Mostrando X de Y libros".

Botones Prestar / Devolver / Editar / Eliminar según el estado del libro.

Modal propio para prestar (validación de nombre: 2–40 caracteres).

Modal propio para confirmar eliminación.

Vista 2 — Mis préstamos
Lista de préstamos activos ordenados por fecha límite (más próxima primero).

Etiqueta de vencido con días de retraso.

Botón para devolver desde la lista.

Historial de devoluciones con indicador de "a tiempo" o "con retraso".

Contador de préstamos activos en el menú.

Vista 3 — Agregar / Editar libro
Formulario con validación campo por campo (mensajes bajo cada campo).

Contador de caracteres restantes del comentario (máx. 120).

Detección de duplicados (mismo título + autor).

Al editar, el mismo libro no cuenta como duplicado de sí mismo.

El foco pasa automáticamente al primer campo con error.

La tecla Escape limpia el formulario y cancela la edición.

Vista 4 — Resumen y ajustes
Total de libros, disponibles, prestados y vencidos.

Cantidad de libros por género.

Botón para cambiar entre tema claro y oscuro (persistente).

Campo para el nombre del usuario (aparece en el menú y al prestar).

Botón para restablecer la biblioteca a los datos iniciales.
