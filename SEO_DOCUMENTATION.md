# Documentación de Implementación SEO - Se Tú

Esta documentación detalla las mejoras de SEO (Search Engine Optimization) implementadas en el proyecto "Se Tú" siguiendo las directrices de la [Guía de SEO para principiantes de Google](https://developers.google.com/search/docs/fundamentals/seo-starter-guide?hl=es).

## 1. Títulos y Meta Descripciones
Se han optimizado los elementos `<title>` y `<meta name="description">` para que sean únicos y descriptivos.

*   **Implementación:** Localizado en `src/layouts/Layout.astro`.
*   **Mejora:** El título incluye la marca y la propuesta de valor ("Se Tú - Tu esencia. Tu propósito."). La descripción resume brevemente el contenido del podcast y su enfoque cristiano.

## 2. Jerarquía de Encabezados (Headings)
Se ha corregido la estructura de encabezados para ayudar a los motores de búsqueda a entender la importancia del contenido.

*   **Implementación:** Cambios en `src/pages/index.astro`.
*   **Mejora:**
    *   Se añadió un elemento `<h1>` principal con el nombre del proyecto ("Se Tú"). Anteriormente faltaba un `<h1>` en el cuerpo del documento.
    *   Se organizaron los temas secundarios bajo etiquetas `<h2>` ("Descubre Quién Dice Dios Que Soy", "Sobre Se Tú").
    *   Se eliminaron etiquetas `<h2>` redundantes que no aportaban estructura semántica adicional.

## 3. Optimización de Imágenes
Todas las imágenes ahora cuentan con atributos descriptivos para mejorar la accesibilidad y el SEO de imágenes.

*   **Implementación:** Cambios en `src/components/Header.astro` y revisión de `src/components/YouTubeEmbed.astro`.
*   **Mejora:**
    *   Se actualizó el `alt` del logo de "Company Logo" a "Logo oficial de Se Tú - Podcast sobre identidad en Cristo y propósito divino".
    *   Se verificó que los placeholders de video utilicen el título del video como texto alternativo.

## 4. Datos Estructurados (Schema.org)
Se han incluido fragmentos de código JSON-LD para ayudar a Google a entender mejor la organización y el sitio web.

*   **Implementación:** Localizado en `src/layouts/Layout.astro`.
*   **Mejora:** Se definieron tipos `Organization` y `WebSite` con sus respectivas propiedades (nombre, URL, logo, descripción).

## 5. Accesibilidad y Semántica HTML
*   Uso de etiquetas semánticas como `<main>`, `<header>`, `<section>` y `<nav>`.
*   Atributos `aria-label` en elementos interactivos como secciones de video y botones de reproducción.
*   Definición del idioma del sitio mediante `lang="es"` en la etiqueta `<html>`.

## 6. Archivos de Control de Rastreo
*   **robots.txt:** Configurado para permitir el rastreo de Googlebot y otros buscadores importantes, indicando la ubicación del sitemap.
*   **sitemap.xml:** Incluye la URL principal del sitio con su fecha de última modificación y prioridad.

---
*Implementado siguiendo las recomendaciones de Google Search Central.*
