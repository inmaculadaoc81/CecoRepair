CECOTECREPAIR ONE PAGE

Dominio:
https://robotsaspiradores.com.es/

SERVICIO:
Reparación de robot aspirador Cecotec.

DIAGNÓSTICO:
20 € + IVA.
NO indicar diagnóstico gratuito.

CONTACTO — REGLA ESPECIAL PARA ESTA WEB:
- Únicamente mediante formulario.
- NO mostrar teléfono en la web.
- NO botón de llamada.
- NO WhatsApp.
- NO chatbot.
- NO Cal.com.
- NO correo visible.
- El teléfono pedido dentro del formulario es solo para que el usuario deje sus datos de contacto.

Google Business:
https://maps.app.goo.gl/CQWPNmpVFKEa4rwU9

YouTube:
https://www.youtube.com/channel/UCaxAqLD9Mk5gvzqoDedlWSA

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo de soporte no aparece en el HTML. Solo se utiliza en /api/contacto.

Google Analytics:
G-FBFCK85BDS

HISTORIAL: el repositorio era multipágina (19 páginas /modelos/ de
series Conga, más varias páginas /servicios/) y se convirtió a
one-page; esas páginas fueron eliminadas en commits anteriores. Como
ya no existen en el sitemap actual, se ha añadido middleware.mjs para
redirigir (301) cualquier URL antigua a la home, evitando 404 en
enlaces indexados o backlinks antiguos. Excluye /api/* y cualquier
ruta con extensión de archivo. Se añadió "@vercel/functions": "^2.0.3"
a package.json como dependencia de esta función.

REVISIÓN (fixes aplicados):
- Schema.org: ya existía (LocalBusiness JSON-LD); no se ha tocado.
- Sin teléfono, WhatsApp ni chatbot: esto es intencional (ver regla
  especial arriba), así que NO se ha añadido botón de llamada, chat ni
  borde blanco de chat — no aplican a esta web.
- Sección SEO en la home: no existía. Añadida sección "Guía" (id="guia",
  enlazada en el menú) con contenido propio sobre las series Conga,
  averías habituales y el proceso de diagnóstico.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar /
  Política de privacidad → https://kelatos.com/privacy-policy/), con
  diseño apilado a ancho completo en móvil.
- H1 de portada reescrito, corto y directo (estilo Isra Bravo, frase
  totalmente afirmativa, sin interrogación ni palabras condicionales
  como "si"/"conviene", incluye la marca): "Tu Cecotec no aspira bien.
  Aquí lo resolvemos, podemos repararlo." Tamaño del H1 aumentado:
  clamp(38-58px) → clamp(46-74px) en escritorio, 40px → 48px en móvil.
- api/contacto.js ya usaba SMTP + nodemailer (CommonJS, coherente con
  el package.json sin "type":"module"); no requería conversión.
