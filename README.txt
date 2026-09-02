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

REVISIÓN ADICIONAL (a petición del cliente, regla general de la familia):
- Quitada la pestaña/etiqueta rotada del hero (.hero-chip o
  .hero-tag) que sobresalía y se solapaba visualmente con la caja de
  información en anchos de tablet/escritorio medio (detectado con
  captura en vivo en AcerTech). Regla para toda la familia: no volver
  a añadir este tipo de elemento decorativo. (La regla CSS .hero-chip
  se deja intacta, sin uso, según práctica habitual de la familia.)

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "Tu X no Y. Aquí Z." usada en varios repos
  ("Tu Cecotec no aspira bien. Aquí lo resolvemos, podemos
  repararlo."). Reescrito en formato imperativo, sin mencionar
  diagnóstico gratuito (aquí el diagnóstico tiene coste, 20 € + IVA,
  según la regla especial de esta web): "Repara tu robot aspirador
  Cecotec en Madrid." (7 palabras).
- BUG REAL — dos textos decorativos gigantes sin ninguna reducción de
  tamaño en tablet/móvil: ".problems::after" ("CECOTEC", 175px) y
  ".care-art::before" ("LIMPIEZA", 86px), mismo patrón ya corregido en
  KoboldTech. Añadida reducción en tablet (100px/56px) y móvil
  (56px/40px). El ticker ".hero::after" ya se ocultaba correctamente
  en móvil, no se ha tocado.
- La casilla de política de privacidad existía pero el texto no
  enlazaba a ningún sitio. Añadido el enlace estándar de la familia a
  https://kelatos.com/privacy-policy/, resaltado en azul.
- Añadida franja de aviso de servicio técnico independiente debajo del
  menú (no existía). Verificado antes que .header no usa
  display:flex directamente.
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- No aplica la regla de paridad de iconos en los CTA: esta web solo
  tiene un botón de acción ("Cuéntanos qué le ocurre", enlaza al
  formulario), sin teléfono ni WhatsApp, según la regla especial de
  contacto exclusivo por formulario. Verificado: schema.org
  correctamente sin campo "telephone" (coherente con esa misma
  regla); formulario conectado a /api/contacto.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente — repo 32/48):
- No aplica: enlace de Cal.com, mensaje de WhatsApp y botón de
  teléfono — esta web usa la regla especial de contacto exclusivo por
  formulario (sin teléfono, sin WhatsApp, sin Cal.com, sin chatbot),
  ya documentada arriba.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- Verificado: el menú móvil ya se cerraba correctamente al pulsar un
  enlace.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- Verificado: el H1 en móvil ya está en 48px.
- Verificado: el único CTA del hero (.hero-cta) ya tenía
  border-radius:999px y un estado hover que oscurece el fondo; no
  requería cambios.
- Verificado: este repo no usa el patrón de franja de insignias bajo
  el H1 (familia Dyson); no aplica la reubicación.

REVISIÓN ADICIONAL (nueva regla de menú móvil, a petición del cliente):
- BUG REAL — la franja de aviso de independencia estaba dentro de
  <header>. Movida fuera de <header>, como hermana justo después de
  él y antes del hero: sigue siendo la misma franja amarilla de ancho
  completo.
- Verificado: el header (.header{position:sticky;top:0}) ya se
  mantenía fijo/pegado arriba al hacer scroll; no requería cambios.
- Verificado de nuevo: el resto del checklist ya estaba correcto (esta
  web usa la regla especial de contacto exclusivo por formulario, sin
  teléfono/WhatsApp/Cal.com); no requería cambios.
