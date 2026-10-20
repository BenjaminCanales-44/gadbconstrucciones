# GADB Construcciones — Sitio web corporativo

🔗 **Sitio en producción:** [www.gadbconstrucciones.cl](https://www.gadbconstrucciones.cl)

Sitio web para una empresa constructora de la Región de Coquimbo (casas, quinchos, ampliaciones, remodelaciones, piscinas y terrazas). Presenta los servicios y proyectos realizados, y permite a los clientes cotizar directamente por WhatsApp. La empresa actualiza servicios, proyectos y testimonios desde un panel web, sin tocar código.

> Proyecto desarrollado en equipo por **Benjamin Canales** y **[Bryan Piña](https://github.com/Bemol69)** para un cliente real.

## ✨ Funcionalidades

- **Catálogo de servicios** y **portafolio de proyectos** con filtros y galería de fotos.
- **Formulario de cotización** que arma automáticamente el mensaje de WhatsApp.
- **Proceso de trabajo, testimonios y contadores** animados.
- **Zonas de cobertura y horario** de atención configurables.
- **Panel de administración (/admin)** con Sveltia CMS: cada cambio genera un commit en GitHub y se publica automáticamente.
- Diseño responsive con animaciones que respetan `prefers-reduced-motion`.

## 🏗️ Arquitectura

- **Build propio en Node.js** (`scripts/build.mjs`): lee la configuración del sitio y los datos en JSON editados desde /admin, y genera el sitio final en `dist/`.
- **Optimización de imágenes** a WebP para una carga rápida.
- **SEO técnico**: contenido renderizado en el HTML, canonical, Open Graph, datos estructurados (Schema.org `GeneralContractor`), `sitemap.xml` y `robots.txt`.
- **Publicación continua en Vercel** con dominio propio.

## 🛠️ Tecnologías

JavaScript (vanilla) · HTML5 · CSS3 · Node.js · Sveltia CMS · GitHub · Vercel

## 🚀 Ejecutar localmente

```bash
npm install
node scripts/build.mjs
npx serve dist
```
