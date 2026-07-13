# Auditoría y mejora de SEO técnico — martinhersog.com

**Cliente:** María Martín Hersog ([martinhersog.com](https://martinhersog.com))
**Tipo de proyecto:** Auditoría y optimización de SEO técnico
**Alcance:** WordPress + RankMath SEO + Google Search Console

## Descripción corta

Auditoría y optimización de SEO técnico para el portfolio profesional de María Martín
Hersog (martinhersog.com): instalación y configuración de RankMath, verificación en
Google Search Console, corrección de estructura de encabezados, optimización de
metadatos y accesibilidad de imágenes. Puntuación de SEO on-page mejorada de **78 a
91/100**.

---

## Contexto

María Martín Hersog es diseñadora gráfica y web, con un portfolio en WordPress activo
desde 2021 pero sin ningún trabajo de SEO técnico realizado hasta la fecha. El sitio no
tenía plugin de SEO instalado, no estaba verificado en Google Search Console, y
presentaba varios problemas de estructura técnica que dificultaban tanto la indexación
como la interpretación del contenido por parte de los buscadores. Construido con
WordPress + tema Salient + WPBakery Page Builder.

## Objetivo

Establecer una base técnica de SEO sólida sobre la que poder construir, en el futuro,
una estrategia de contenido y visibilidad — dejando el sitio correctamente configurado,
medible y sin errores estructurales, aunque el impacto directo en tráfico de búsqueda
dependa de trabajo posterior (contenido, enlaces externos).

**Nota de acceso:** la propietaria ofreció acceso completo a la cuenta de hosting; por
seguridad, se optó por no usar ese acceso directo y trabajar en su lugar con un usuario
administrador propio y limitado dentro de WordPress.

## Trabajo realizado

### 1. Configuración de herramientas

- Instalación y configuración de **RankMath SEO** (no había ningún plugin de SEO antes).
- Creación de una propiedad en **Google Search Console** y verificación de la
  propiedad.
- **Problema encontrado:** la verificación por etiqueta HTML fallaba — el código
  publicado en el `<head>` del sitio no coincidía con el que RankMath insertaba, señal
  de que otra fuente tenía prioridad. Se descartó como causa el plugin RankMath, la
  caché, y otros plugins instalados (desactivándolos uno a uno). El origen exacto no
  se localizó (probablemente un meta tag antiguo hardcodeado en el tema padre), pero no
  bloqueó la solución.
- **Solución aplicada:** verificación por el método alternativo **"Archivo HTML"** de
  Search Console, que no compite con el `<head>` del sitio — funcionó a la primera.

### 2. Corrección de estructura técnica

- **H1 duplicado en la home:** el módulo de encabezado tenía 3 etiquetas `<h1>` en la
  misma página (debía haber exactamente 1). Causa: dos títulos adicionales estaban
  codificados manualmente como `<h1>` en el bloque de contenido en lugar de `<h2>`.
  Corregido cambiando el nivel de encabezado de esos dos elementos.
- **Sitemap de autores expuesto:** el sitemap nativo de WordPress incluía un
  sub-sitemap de usuarios (`users`), que exponía innecesariamente los nombres de
  usuario del sitio — sin valor SEO y un riesgo menor de seguridad. Resuelto
  automáticamente al activar RankMath, que tomó el control de los sitemaps y desactivó
  el nativo de WordPress.
- **Imágenes sin texto alternativo (ALT):** redacción de texto ALT descriptivo para
  más de 60 imágenes del portfolio, cubriendo tanto las señaladas por el analizador de
  RankMath como el resto del catálogo de proyectos — mejora de accesibilidad y de SEO
  de imágenes.

### 3. Optimización on-page

- Redacción de títulos SEO y meta descriptions para las 4 páginas principales del
  sitio (Inicio, Sobre mí, Portfolio, Contacto).
- Definición de palabra clave objetivo para las 4 páginas principales y las 14
  entradas del portfolio de proyectos.
- Ajuste de los títulos internos de página (WordPress) para alinearlos con las
  palabras clave — con el cuidado de que, en este sitio, el menú de navegación hereda
  automáticamente el título de página si no se ha personalizado a mano. Se fijó el
  texto de navegación manualmente en cada caso para no romper la coherencia visual del
  menú.

## Resultado: evolución de la puntuación de SEO on-page (RankMath)

| Momento | Puntuación | Detalle |
|---|---|---|
| Primer informe completo | 78/100 | 21 pruebas superadas / 1 aviso / 4 fallos |
| Tras H1, imágenes, títulos y keywords | 86/100 | 22 pruebas superadas / 1 aviso / 3 fallos |
| Tras keywords en portfolio y ajustes finales | **91/100** | 23 pruebas superadas / 0 avisos / 3 fallos |

Los fallos restantes al cierre de esta fase son de menor impacto y quedan como
pendientes documentados: 14 entradas de portfolio donde la keyword no aparece en el
título interno de WordPress (mismo ajuste ya aplicado a las 4 páginas principales),
etiquetas OpenGraph incompletas, y un fallo puntual de ejecución del test de velocidad
móvil (no del sitio en sí).

## Nota metodológica

Este trabajo corresponde a SEO técnico y on-page — higiene y estructura del sitio, no
promoción o generación de tráfico. Su valor es servir de base correctamente construida
para futuras acciones de contenido y visibilidad, que son las que determinarán el
impacto real en el posicionamiento en buscadores para términos competitivos.

## Pendientes para una futura fase

- Ampliar el contenido de las páginas principales (objetivo 600+ palabras) integrando
  la keyword de forma natural, para subir la puntuación real más allá de ajustes de
  metadatos.
- Ajustar el título interno de WordPress de las 14 entradas de portfolio.
- Completar las etiquetas OpenGraph para mejorar la vista previa al compartir en redes
  sociales.
- Instalar Google Analytics como segundo método de verificación de propiedad y para
  empezar a acumular datos de tráfico.
