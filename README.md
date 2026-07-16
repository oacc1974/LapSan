# Importadora LAP SAN – Landing Page y Plan SEO

Este proyecto contiene la landing page corporativa de **Importadora LAP SAN** (Guayaquil – Ecuador), enfocada en soluciones para el hogar en **control de plagas** e **inciensos aromáticos**.

## Tecnologías utilizadas

- **HTML5**: estructura semántica clara (header, main, sections, footer).
- **CSS3**: estilos modernos y responsive, listos para utilizar variables CSS si se requiere.
- **JavaScript (vanilla)**: funcionalidad básica (menú móvil, año dinámico en el footer) sin dependencias externas.
- **Font Awesome 6.4** (opcional): para usar iconos profesionales en caso de que se integren en el futuro.

## 1. Objetivo SEO

Posicionar la landing para búsquedas relacionadas con:

- Importadora y distribuidora de inciensos y productos para el control de plagas en Ecuador.
- Inciensos espirales mata mosquitos (marca **ZENDEN**) y trampas engomadas **LEÓN**.
- Búsquedas locales relacionadas con Guayaquil y el mercado ecuatoriano.

## 2. Palabras clave sugeridas

Ejemplos de keywords y variantes a utilizar de forma natural en los textos:

- **Marca + servicio**
  - `importadora lap san`
  - `importadora de inciensos en ecuador`
  - `importadora de productos para control de plagas`

- **Producto + país/ciudad**
  - `incienso mata mosquitos ecuador`
  - `incienso espiral mata mosquitos zenden`
  - `trampas engomadas leon ecuador`
  - `incienso aromatico clove`

- **Intención local**
  - `control de plagas en guayaquil`
  - `proveedor de productos para el hogar en guayaquil`
  - `distribuidor de inciensos y control de plagas en ecuador`

Las palabras clave deben aparecer de forma natural en:

- Título principal (`<h1>`).
- Subtítulos (`<h2>`, `h3`).
- Primeros párrafos de texto.
- Descripciones de productos.

## 3. SEO on-page implementado

En `index.html` se han aplicado las siguientes prácticas:

- **Title SEO optimizado**:
  - `Importadora LAP SAN | Control de plagas e inciensos aromáticos para el hogar`
- **Meta description descriptiva y local**:
  - Menciona Guayaquil, Ecuador, control de plagas, inciensos aromáticos y experiencia de 20+ años.
- **Meta robots**:
  - `<meta name="robots" content="index,follow" />`
- **Canonical**:
  - `<link rel="canonical" href="/" />` (actualizar con el dominio definitivo cuando esté disponible).
- **Open Graph (OG)** para redes sociales y bots:
  - `og:title`, `og:description`, `og:type`, `og:url`, `og:site_name`, `og:image`.
- **Twitter Card**:
  - `summary_large_image` con título, descripción e imagen del logo.
- **Estructura de encabezados clara**:
  - `h1` único para el título principal.
  - `h2` para secciones: Quiénes somos, Liderazgo en el mercado, Portafolio de productos, Beneficios, Contáctenos.
- **Contenido relevante**:
  - Textos que explican experiencia, productos, liderazgo de la marca ZENDEN y beneficios para el cliente.

### Recomendaciones on-page adicionales

- Ajustar ligeramente el `h1` y subtítulos para incluir variaciones como:
  - "inciensos mata mosquitos en Ecuador", "control de plagas para el hogar", etc.
- Revisar que los textos se mantengan naturales y sin sobrecarga de palabras clave.
- Revisar y optimizar **atributos `alt` de las imágenes** para que sean descriptivos (tipo de producto, marca y contexto), por ejemplo:
  - `alt="Incienso espiral mata mosquitos marca ZENDEN en empaque"`.

## 4. SEO técnico

Archivos creados en la raíz del proyecto `Lap`:

### 4.1. `robots.txt`

```txt
User-agent: *
Disallow:

Sitemap: /sitemap.xml
```

- Permite el rastreo completo (`index, follow`).
- Indica a los bots la ubicación del sitemap.

Se pueden añadir reglas de bloqueo en el futuro si hay secciones restringidas.

### 4.2. `sitemap.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>/</loc>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>/index.html</loc>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
</urlset>
```

- Cuando existan otras páginas (ej. servicios, blog, etc.), se deben agregar nuevos nodos `<url>`.
- Al publicar en un dominio real, actualizar `loc` con la URL completa, por ejemplo:
  - `https://imlapsan.com/`

### 4.3. `404.html`

- Página de error personalizada con:
  - Título: `404 - Página no encontrada`.
  - Estilo reutilizando `styles.css`.
  - Botón para volver a `/index.html`.
  - Meta `robots` configurado como `noindex,follow`.
- El servidor (Apache, Nginx, hosting) debe configurarse para utilizar este `404.html` como página de error.

### 4.4. Seguridad (recomendado en `.htaccess` o configuración del servidor)

- Configurar **headers de seguridad**:
  - `Content-Security-Policy` (CSP) adecuada al proyecto.
  - `X-Content-Type-Options: nosniff`.
  - `X-Frame-Options: SAMEORIGIN` (prevención de **clickjacking**).
  - `X-XSS-Protection: 1; mode=block` (protección básica contra **XSS** en navegadores que lo soporten).
- Obligar uso de **HTTPS**:
  - Redirección permanente `http → https`.
  - Redirección `dominio.com/index.html → dominio.com/` para evitar contenido duplicado.
- Opcional: cabeceras de privacidad/cookies si se añaden herramientas de analítica.
- Seguir aplicando buenas prácticas de rendimiento:
  - Comprimir imágenes (idealmente < 200 KB cada una).
  - Minificar CSS/JS en modo producción si es necesario.
- Verificar experiencia móvil y métricas core web vitals con herramientas como **PageSpeed Insights** o **Lighthouse**.

## 5. Datos estructurados (schema.org)

Se recomienda añadir datos estructurados (JSON-LD) para que los buscadores entiendan mejor la empresa.

### 5.1. Tipo recomendado

- `Organization` o `LocalBusiness`.

### 5.2. Campos sugeridos

- `@type`: `Organization` / `LocalBusiness`.
- `name`: `Importadora LAP SAN`.
- `address`: dirección en Guayaquil – Ecuador.
- `email`: `ventas@imlapsan.com`.
- `url`: URL del sitio (cuando exista dominio definido).
- `logo`: URL absoluta del logo.
- `telephone`: teléfono comercial.
- `sameAs`: enlaces a redes sociales (si aplica).

> Nota: El JSON-LD debe agregarse dentro del `<head>` de `index.html` en un bloque `<script type="application/ld+json">`.

## 6. SEO local

Importante para posicionarse en Guayaquil y Ecuador:

- Crear y optimizar **Google Business Profile (Google Mi Negocio)**:
  - Nombre: Importadora LAP SAN.
  - Categoría adecuada (importadora / distribuidor / control de plagas / productos para el hogar).
  - Dirección completa, teléfono, sitio web.
  - Horarios de atención.
  - Fotografías de productos, bodegas, oficinas.
  - Solicitar reseñas a clientes.

- Presencia en **directorios y cámaras locales**:
  - Cámaras de comercio, asociaciones del sector, directorios empresariales de Ecuador.

## 7. SEO off-page (enlaces y autoridad)

Acciones recomendadas:

- Conseguir **backlinks** desde:
  - Distribuidores, mayoristas, cadenas de tiendas que trabajen con LAP SAN.
  - Blogs o portales de hogar, control de plagas, estilo de vida.
  - Medios digitales con notas de prensa sobre la marca ZENDEN y la empresa.

- Enlaces desde sitios de **marcas asociadas** (si existen páginas oficiales de ZENDEN, LEÓN, CLOVE) mencionando a LAP SAN como representante en Ecuador.

## 8. Formularios y medición

### 8.1. Formulario de contacto con Formspree

El formulario de contacto en `index.html` está preparado para funcionar con **Formspree**:

```html
<form id="contactForm" class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

Pasos para activarlo:

1. Registrarse en [https://formspree.io](https://formspree.io).
2. Crear un **nuevo formulario** (proyecto) para el sitio de Importadora LAP SAN.
3. Copiar el **Form ID** que proporciona Formspree (formato similar a `/f/abcdwxyz`).
4. Reemplazar `YOUR_FORM_ID` en el atributo `action` por el ID real, por ejemplo:

```html
action="https://formspree.io/f/abcdwxyz"
```

> A partir de ese momento, cada envío del formulario se enviará al correo configurado en Formspree.

## 9. Medición y seguimiento

Una vez que el sitio esté publicado en su dominio final:

- **Google Search Console**:
  - Verificar la propiedad del dominio.
  - Enviar `sitemap.xml`.
  - Revisar cobertura (errores 404, problemas de indexación, etc.).
  - Revisar consultas de búsqueda y páginas con más impresiones/clics.

- **Google Analytics / GA4**:
  - Medir tráfico orgánico.
  - Configurar eventos para:
    - Clic en "Ver portafolio de productos".
    - Clic en "Contactar ventas".
    - Envíos del formulario de contacto.

### 9.1. Google Analytics (opcional)

Si se desea medir el comportamiento de los usuarios con **Google Analytics 4 (GA4)**:

1. Crear una **propiedad GA4** en la cuenta de Google Analytics.
2. En la sección *Flujos de datos* (Web), copiar el **Measurement ID** (formato `G-XXXXXXXXXX`).
3. Integrar la etiqueta de Google en el sitio, normalmente en el `<head>` de `index.html` o en un archivo JS central (por ejemplo, `main.js`).

Ejemplo de línea de configuración (una vez cargado `gtag.js`):

```js
gtag('config', 'G-XXXXXXXXXX'); // Reemplaza con tu Measurement ID real
```

> Importante: no subir a producción el ID genérico; siempre reemplazar `G-XXXXXXXXXX` por el ID de medición correcto de la propiedad.

## 9. Checklist rápido

- [ ] Definir dominio final y actualizar `canonical`, `og:url` y `sitemap.xml`.
- [ ] Revisar y optimizar `alt` de todas las imágenes.
- [ ] Afinar textos de `h1`, subtítulos y párrafos con palabras clave naturales.
- [ ] Configurar HTTPS y redirecciones en el servidor.
- [ ] Asegurar que el servidor use `404.html` como página de error.
- [ ] Añadir datos estructurados (JSON-LD) de `Organization` o `LocalBusiness`.
- [ ] Crear/optimizar Google Business Profile.
- [ ] Registrar el sitio en Google Search Console y enviar `sitemap.xml`.
- [ ] Configurar Google Analytics / GA4 y eventos principales.
