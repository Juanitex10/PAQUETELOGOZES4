# PA Q TE LO GOZES · Carruseles separados y modelos refinados

Abre `index.html` en un navegador moderno con WebGL. No requiere instalación, framework ni compilador. El archivo único incorpora fotografías, etiquetas y modelos. Necesita Internet para Three.js, Google Fonts y el mapa. El ZIP incluye ese HTML y estas instrucciones.

## Inicio y carta

Foto real del local restaurada y optimizada en WebP: **1792 × 2400 píxeles**, superior a la imagen original. No es una fotografía nativa 4K; no se inventó otro local ni se infló su tamaño con reescalado artificial. El fondo conserva las luces y ambiente neón. La carta sigue integrada debajo de Inicio, sin emergente.

Se retiró el bloque de granizados/sodas de esa carta, **no la pestaña Granizados y sodas**, que conserva el granizado recolorable, tamaños y dos sodas. Botón «Cócteles» sin 3D. Retirados los cuadros de licores y Trident; vínculo discreto «Ver licores y bebidas» dirige a la pestaña interna. Hay enlaces individuales para las diez referencias de alcohol y las tres bebidas: al pulsar abre la botella exacta.

## Licores y bebidas

Dos carruseles simultáneos e independientes en la misma pestaña: **licores a la izquierda, bebidas a la derecha** en PC; se apilan en teléfono para mantener buena legibilidad. Cada uno tiene botella anterior a la izquierda, activa en el centro y siguiente a la derecha, con profundidad. Pulsa cualquiera de las laterales para traerla al centro. La fila inferior de flechas y puntos se retiró; puedes navegar por las botellas, flechas del teclado al enfocar el panel y catálogo. Las transiciones usan giro de 720°, arco ligero y curva suave como Cócteles.

Cristal, Gatorade y Bretaña tienen modelos GLB propios de sus referencias. Bretaña incorpora la silueta entallada, tapa y relieve de vidrio sin etiqueta de papel ficticia. Las diez referencias de alcohol tienen modelos paramétricos volumétricos con hombros, cuello, tapa, base y etiquetas tomadas de la carta restaurada. Las cuatro medias botellas tienen exactamente la mitad de altura del equivalente completo en la misma posición; forma, etiquetas y precios se conservan. No son paneles fotográficos. La nitidez de texto trasero está limitada por las fuentes originales.

## Cócteles y controles

Once modelos 3D. Se reconstruyeron El Ferxxo, Demencia tropical, Piña colada y Cabeza de Jabalí con referencias llenas, contornos completos y mapas PBR detallados. Se conservaron texturas hasta 2048 px al optimizar. Son reconstrucciones desde fotografías, no escaneos físicos perfectos; los detalles traseros y vidrio pueden diferir del producto real.

Mantén clic izquierdo o toque sobre un producto y arrastra para girarlo sobre su centro. Al soltar vuelve a su orientación sin trasladarse. Clic derecho/central no deslizan. Clic breve al producto lateral o posterior lo trae delante. Los carruseles de alcohol y bebidas cambian independientemente. Cócteles conserva sus controles propios. Un único contexto y canvas WebGL sirve las dos escenas, sin pasar automáticamente a 2D. Piezas de botellas con mismo material se agrupan para reducir llamadas de dibujo; los paneles fuera de pantalla en móvil no se renderizan.

Retirada la sombra rectangular del plano de reflexión. Los cócteles conservan sus transiciones, textos/precios y colores de fondo; las instrucciones flotantes y frutas decorativas siguen eliminadas. Resolución adaptativa reduce carga en GPU lenta; movimiento reducido aplica cambios inmediatos. No se garantiza una tasa fija de FPS en todo dispositivo.

## Reservas

Solo se oculta el botón duplicado «Reserva tu mesa» dentro de Reservas; la navegación permanece. **Fecha de nacimiento** y **Fecha de reserva** son campos distintos: admite cumpleaños reales de cualquier adulto de al menos 18 años, no futuros; reserva hoy o futura en calendario válido usando fecha actual de Bogotá. No requiere ni almacena documentos de identidad.

«El plan» tiene selector de estilo oscuro redondeado con Un buen parche, Cumpleaños, Evento especial y **Otro**. Al elegir Otro se pide «Especifica tu evento», obligatorio y no vacío. Esa descripción se incluye en el mensaje preparado para WhatsApp. El cumpleaños no se envía en ese mensaje. El formulario conserva valores al navegar y no envía ni confirma reservas automáticamente.

Mapa y contacto siguen debajo del formulario. Instagram rosa, teléfono azul y Gmail multicolor. El visitante debe enviar la solicitud y el equipo confirmar disponibilidad: WhatsApp +57 320 845 5447.

## Alcance

Esta vista previa y copia descargable no modifican https://paquetelogozes4.vercel.app/. Sustituir la web original requiere acceso al editor o hosting Webador. Los cambios permanecen en el proyecto del rediseño.

## Refinamiento de esta versión

Demencia tropical se reconstruyó con contorno de copa continuo y superficie roja más lisa, sin los pliegues exagerados de la malla anterior. Piña colada se reconstruyó con líquido cremoso lleno hasta justo debajo del borde, copa continua y rodaja de piña conservada. Las tres reconstrucciones nuevas (estas dos copas y Bretaña) usan mapas PBR y texturas optimizadas hasta 2048 px, con aproximadamente 47–49 mil caras cada una. El vidrio y los detalles internos siguen siendo aproximaciones de fotografías; no son escaneos ópticos perfectos del producto físico.

## Optimización, SEO y analítica (última revisión)

- Imágenes convertidas a WebP/JPEG y redimensionadas a su tamaño real de uso; texturas de los 16 modelos 3D limitadas a 1024 px (JPEG). El fondo de Inicio ya no se duplica (variable CSS `--hero-img`).
- Todas las `<img>` tienen `alt` descriptivo con enfoque SEO.
- `404.html`: página de error con la identidad del sitio (`noindex`). Debe configurarse como página de error en el hosting.
- Validación interactiva del formulario de reservas (errores en rojo bajo cada campo; bloquea el envío si hay errores). Script al final de `index.html`.
- GA4 en el `<head>` con marcador `G-XXXXXXXXXX`; reemplázalo por tu ID de medición en `index.html` y `404.html`.

## Legal, cookies y SEO (última revisión)

- `privacidad.html` y `terminos.html`: textos legales (Colombia, Ley 1581 de 2012) con el diseño del sitio; estilos en `assets/legal.css`. Enlazados en el pie de `index.html`.
- Banner de cookies al final de `index.html` (antes de `</body>`). Guarda la elección en `localStorage` (`paq_cookie_consent`, 12 meses) y controla el consentimiento de GA4 (Consent Mode). El enlace «Preferencias de cookies» del pie lo reabre.
- SEO en el `<head>`: title, descripción (≤150), canonical y Open Graph/Twitter con `assets/og-image.jpg` (1200×630). Favicon: `assets/favicon.png` (32×32).
- `sitemap.xml` y `robots.txt` en la raíz. Sube también la carpeta `assets/`.

## Optimización (SEO, imágenes y modelos 3D)

- SEO y Open Graph orientados a «los mejores granizados y cócteles de Bogotá»; datos estructurados `BarOrPub` (JSON-LD). Si el dominio final no es `https://paquetelogozes4.vercel.app/`, cámbialo en el `<head>` de `index.html` (og:url, og:image, twitter:image), en `privacidad.html`, `terminos.html`, `sitemap.xml` y `robots.txt`.
- Imágenes de producto y fondo en `assets/img/*.webp` (todas ≤ 150 KB) con `alt` descriptivo. `assets/logo.webp` para el logo.
- `assets/og-image.jpg` se mantiene en JPG a propósito: WhatsApp y Facebook no muestran bien las vistas previas en WebP. `assets/favicon.png` también se mantiene en PNG por compatibilidad.
- Modelos 3D (`assets/models/*.glb`) comprimidos con Meshopt + cuantización + texturas WebP (23,7 MB → 7,4 MB, sin cambio visual). El cargador usa `MeshoptDecoder`; las normales vienen ya suavizadas en el archivo, por eso no se recalculan.
