# ORVIO | Desarrollo de Plataforma E-commerce y Arquitectura Front-End

## 📝 Fundamentación y Enfoque del Proyecto
Este proyecto pre-entrega consiste en el diseño, maquetación y personalización integral de la interfaz de usuario (UI) para **ORVIO**, una tienda en línea orientada al nicho de wearables, telefonía móvil y dispositivos de audio avanzado. 

**Nota de Metodología de Desarrollo:** El sitio fue concebido como una solución de software real para dar soporte técnico e impulsar el canal comercial de un emprendimiento activo propiedad de **Scorso Rosana** (con punto de distribución en **José León Suárez, Provincia de Buenos Aires**). Para su ejecución, se tomó como base la estructura modelo provista por la cátedra, la cual fue modificada de manera exhaustiva a conveniencia del proyecto. Durante el proceso de desarrollo y reingeniería del código, se utilizó la **Inteligencia Artificial (Gemini AI) como entorno de asistencia y co-piloto de desarrollo**, permitiendo acelerar la resolución de problemas de maquetación, depuración de estilos y optimización del diseño líquido.

---

## 🛠️ Especificaciones Técnicas y Auditoría del Código

### 1. Estructura y Semántica Completa (HTML5)
La arquitectura de la información se distribuye de forma modular e independiente entre el nodo principal (`index.html`) y la subpágina transaccional (`pages/contacto.html`), utilizando de forma estricta etiquetas semánticas nativas:
* **`<header class="header">`**: Barra de navegación superior persistente (`position: sticky`). Aloja la identidad marcaria corporativa, los puntos de acceso al flujo del carrito y la lista de navegación principal (`.navbar`).
* **`<main>`**: Eje dinámico de contenidos estructurado secuencialmente mediante bloques independientes:
  * `.hero`: Banner de alto impacto comercial con alineación optimizada (`justify-content: flex-end`) para balancear la legibilidad tipográfica y el arte de fondo.
  * `.section-productos`: Contenedor modular encargado de la exposición del catálogo técnico de la tienda.
  * `.banner`: Sección intermedia configurada para llamados a la acción (CTA) e incentivos de conversión (`40% OFF`).
  * `.section-resenias`: Módulo de validación social mediante opiniones de usuarios estructuradas.
  * `.seccion-mapa`: Incorpora la integración multimedia requerida a través de un elemento `<iframe>` embebido para la geolocalización de la sede central.
  * `.newsletter`: Franja inferior de captura de datos orientada a estrategias de fidelización por correo.
* **`<footer>`**: Cierre adaptativo que organiza metadatos verídicos de localización, menús informativos de usuario y sellos de confianza para pasarelas de pago.

### 2. Capa de Presentación Avanzada y Hojas de Estilo (CSS3)
El ecosistema visual y las reglas de diseño se gobiernan centralizadamente en el archivo `styles.css` aplicando propiedades avanzadas de CSS nativo:
* **Maquetación Unidimensional (Flexbox):** Implementado en la grilla `.productos-container`. La combinación de `display: flex` y `flex-wrap: wrap` permite que los elementos hijos (`.producto`, calculados a un ancho del `23%`) se reordenen de manera líquida según el espacio disponible en el viewport, previniendo deformaciones mediante `object-fit: contain` en sus imágenes.
* **Maquetación Bidimensional (CSS Grid):** Utilizado en el bloque `.resenias-container` mediante `display: grid` y la regla `grid-template-columns: repeat(3, 1fr)`. Esto asegura una distribución geométrica perfecta en tres columnas proporcionales que responden dinámicamente al cursor (`transform: translateY(-4px)`).
* **Reset General y Tipografía:** Normalización del DOM utilizando el selector universal (`*`) asociado a `box-sizing: border-box`, unificando la estética general bajo la fuente tipográfica *Spartan* (Google Fonts).

### 3. Adaptabilidad Responsiva (Media Queries)
La hoja de estilos incluye una arquitectura responsiva parametrizada en múltiples puntos de quiebre (`1200px`, `992px`, `768px` y `576px`) para garantizar la visualización en dispositivos móviles:
* En viewports reducidos (inferiores a `799px`), la barra de navegación tradicional muta hacia un menú flotante lateral fuera de la pantalla (`position: fixed; right: -300px`).
* Los contenedores y selectores se encuentran estructurados y preparados para alternar su visibilidad hacia el plano activo (`right: 0px`) ante la inyección de la clase dinámica `.active`.

---

## ⚠️ Estado del Alcance de Interactividad (JavaScript)
*El proyecto se entrega con el ciclo de maquetación semántica (HTML5) y la ingeniería de estilos visuales responsivos (CSS3) completados al 100%. Las declaraciones de selectores, identificadores de control y clases de estado (`id="navbar"`, `id="bar"`, `id="close"`, `class="active"`) se encuentran correctamente integradas en el código fuente. Aquellos componentes lógicos que no sufrieron modificaciones funcionales avanzadas (correspondientes a la interactividad dinámica con JavaScript) se mantienen en su estado estructural base debido a que corresponden a los contenidos programáticos diferidos para los próximos módulos académicos del trayecto.*

---

* **Estudiante:** morillo Maria
* **Proyecto Comercial Real:** ORVIO E-commerce 
* **Curso / Trayecto:** Talento Tech — Desarrollo Web Inicial
