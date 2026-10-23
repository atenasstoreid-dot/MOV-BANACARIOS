# Lucid Bot – Mensajes iniciales por modelo (propuesta v2)

Objetivo: que el primer mensaje, cuando el cliente pregunta por el modelo del
anuncio, sea **dinámico, informativo y persuasivo**, y que termine con una
**pregunta fácil** que lleve a dar la talla y cerrar el pedido.

## Estructura (3 burbujas + multimedia)

1. **Saludo + modelo + foto/video** (el del anuncio, en uso).
2. **Por qué este modelo** (3 viñetas máximo, solo lo que de verdad pesa en la
   decisión).
3. **Precio + envío gratis + contraentrega + pregunta de cierre.**

Reglas de redacción:

- Solo información que ayude a decidir; nada de relleno.
- No prometer tiempos de entrega (varían mucho por municipio).
- Siempre nombrar el **modelo exacto** del anuncio.
- El diferencial va siempre: **suela ultraliviana e inyectada (no pintada)**.
- Quitar el miedo a comprar por internet: **envío gratis + pagas al recibir**.
- Terminar **siempre con una pregunta** (talla o color), nunca con "quedo
  atento".
- Escasez/urgencia solo si es real (stock bajo o promo con fecha).

Variables (ajustar a la sintaxis de Lucid Bot): `{{NOMBRE}}`, `{{MODELO}}`,
`{{PRECIO}}`, `{{COLORES}}`, `{{TALLAS}}`.

---

## Plantilla A – Botas ultralivianas

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 👋 La **{{MODELO}}** es de las botas más pedidas de Atenas
> Store 🔥 Mírala puesta 👇
> *(foto/video)*

**Burbuja 2**
> ✅ **Suela ultraliviana**: la usas todo el día sin cansarte.
> ✅ **Suela inyectada, no pintada**: no se despega ni se pela.
> ✅ Colores: {{COLORES}} · Tallas: {{TALLAS}}.

**Burbuja 3**
> 💰 **{{PRECIO}}** con **envío gratis** a toda Colombia.
> 💵 **Pagas cuando la recibes**, o con Addi / Sistecrédito a cuotas.
>
> ¿Qué **talla** usas? 👟

---

## Plantilla B – Deportivos

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 🙌 El **{{MODELO}}** es el deportivo que más se está
> llevando 🔥
> *(foto/video)*

**Burbuja 2**
> ⚡ **Ultraliviano**: sientes que no llevas nada puesto.
> 💪 **Suela inyectada (no pintada)**: dura más y agarra mejor.
> 🎨 Colores: {{COLORES}} · Tallas: {{TALLAS}}.

**Burbuja 3**
> 💰 **{{PRECIO}}** · **Envío gratis** y **pagas al recibir** 📦
>
> ¿En qué **color** y qué **talla**? 😉

---

## Plantilla C – Clásico / todo negro (trabajo, uniforme)

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 👋 El **{{MODELO}}** es ideal si necesitas un calzado negro
> que aguante el día a día y se vea bien 👌
> *(foto)*

**Burbuja 2**
> ✔️ Sirve para trabajo, uniforme o salir.
> ✔️ **Suela ultraliviana e inyectada**: menos cansancio y no se pela.
> ✔️ Tallas: {{TALLAS}}.

**Burbuja 3**
> 💰 **{{PRECIO}}** · **Envío gratis** y pagas al recibir 🚚
>
> ¿Qué **talla** te separo? 🖤

---

## Mensajes de apoyo

**Seguimiento (10–15 min sin respuesta)**
> {{NOMBRE}}, ¿viste las fotos? 👀 Dime tu talla y te confirmo disponibilidad
> 👟

**"¿Y si no me queda?"**
> Tranquilo 🙌 Si la talla no te queda, te hacemos el **cambio**. Y como pagas
> al recibir, no arriesgas nada. ¿Qué talla usas en tenis?

**"¿Es confiable?"**
> Claro 😊 Somos **Atenas Store S.A.S.**, empresa registrada en Cúcuta. El
> envío es gratis y **pagas cuando recibes**. Mira lo que dicen nuestros
> clientes 👇 *(reseñas/videos)*

**"Está caro"**
> Te entiendo 🙏 La diferencia es la **suela inyectada y ultraliviana**: no se
> despega como las pintadas y dura mucho más. Y puedes pagarlo a cuotas con
> **Addi o Sistecrédito**.

---

## Cómo medir si funciona

A/B (versión actual vs. nueva) 1–2 semanas con el mismo anuncio:

- % que responde al primer mensaje.
- % de conversaciones que terminan en pedido.
- % de pedidos entregados vs. devueltos.
