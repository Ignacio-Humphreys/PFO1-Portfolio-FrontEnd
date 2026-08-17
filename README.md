# Portfolio — Ignacio Tomás Humphreys (PFO1)

Resolución del "PFO1 | Landing de portafolio" de la materia Desarrollo de Sistemas Web · Front End del IFTS 29.

**Nombre y apellido:** Ignacio Tomás Humphreys
**GitHub:** https://github.com/Ignacio-Humphreys
**Demo en Vercel:** 

## Descripción

Landing de una sola página (`index.html`) con estructura semántica (`header`, `nav`, `main`, `footer`) que presenta:
- Sección principal (hero) con nombre y presentación.
- Sobre mí.
- Habilidades técnicas (grid de tarjetas).
- Sección personal: hobbies e intereses.
- Contacto: enlaces directos (email y GitHub) + formulario.

## Decisiones de diseño

- **Paleta negro/rojo, líneas angulares:** Se utiliza `clip-path` para cortar una esquina en diagonal, buscando una estética más industrial/técnica en los botones y las cards.
- **Tipografía:** `Oswald` (condensada, en mayúsculas) para títulos + `IBM Plex Mono` para cuerpo de texto, reforzando el perfil técnico del sitio. Ambas cargadas desde Google Fonts.
- **Layout:** Combino **Flexbox** para elementos de una sola fila con tamaño variable (header, footer) y **Grid** para colecciones de tarjetas que necesitan reacomodarse en filas y columnas según el ancho disponible (habilidades, hobbies, columnas de contacto). Se mezclan ambas por facilidad de uso en cada caso.
- **Variables CSS** Centralizan colores y tipografías para mantener coherencia visual y facilitar cambios futuros.
- **Animación:** Entrada con `fadeSlideUp` en el hero (fade + desplazamiento vertical), más transiciones de hover en tarjetas, links y botones. Se respeta `prefers-reduced-motion` para usuarios que prefieren minimizar animaciones (este último punto, detectado en un chequeo con la IA).
- **Responsive:** Layout fluido con `clamp()` para tipografía y `grid-template-columns: repeat(auto-fill, minmax(...))` para que las tarjetas se reacomoden solas sin depender de breakpoints fijos; un único media query cubre ajustes finos en mobile.
- **Accesibilidad:** `alt` descriptivo en la imagen, `aria-label` en la navegación y el formulario, foco visible por teclado (`:focus-visible`).

## Imágenes

El único elemento gráfico (`assets/avatar.svg`) es una ilustración abstracta simple armada directamente en código SVG (formas geométricas planas), no una foto ni una imagen generada por un modelo de IA de imágenes.

## Declaración de uso de IA

- **Herramienta:** Claude (Anthropic), plan de suscripción estándar (Claude.ai).
- **Para qué se usó:** Estoy creando a modo de práctica este mismo portfolio pero con elementos de backend (como node por ejemplo) y luego se añadirán mejoras para la escalabilidad del mismo. En este caso, la IA me ayudó a pasar ese proyecto complejo a un html estático con los puntos requeridos para las rúbricas, en una búsqueda de optimización de tiempos y para evitar procesos largos de depuración al migrar del proyecto inicial a éste.
- **Experiencia previa:** Utilizo Claude para el trabajo, donde tenemos una cuenta premium que ayuda a la operación diaria. Adicionalmente, a nivel educativo la utilizo siempre previo a los parciales para que me haga dos resúmenes: 1 con los puntos principales que se fueron viendo en las unidades y otro con los detalles adicionales, ejemplos y demás. A ambos resúmenes además les suma una autoevaluación para chequear mis conocimientos y sentirme más cómodo luego a la hora de hacer el parcial correspondiente.
- **Qué revisé/adapté con criterio propio:** Definí la paleta de colores, la tipografía, el contenido real (habilidades, hobbies, datos de contacto) y la estructura de secciones pedida por la consigna; revisé el HTML y CSS generado para confirmar que cumple los requisitos técnicos de la rúbrica (semántica, Flexbox/Grid, Google Fonts, responsive, animación, `alt`, formulario con `label`) antes de darlo por terminado.
