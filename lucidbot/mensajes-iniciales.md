# Lucid Bot – Mensajes iniciales por modelo (propuesta v1)

Objetivo: que el primer mensaje, cuando el cliente pregunta por el modelo del
anuncio, sea **más dinámico, con más información y más persuasivo**, y que
termine siempre con una **pregunta fácil** que lleve a dar la talla y cerrar el
pedido.

## Estructura recomendada (3 burbujas + multimedia)

En vez de un solo bloque de texto largo, enviar en secuencia (1–2 s entre cada
una), así se siente como una conversación real:

1. **Saludo + gancho + foto/video del modelo** (el del anuncio, en uso).
2. **Beneficios** (máximo 4 viñetas, lo que gana el cliente, no solo
   características).
3. **Precio + formas de pago + garantía + pregunta de cierre** ("¿Qué talla
   usas?").

Reglas de redacción:

- Tutear, tono cercano y seguro. Frases cortas. 3–5 emojis por mensaje, no más.
- Siempre nombrar el **modelo exacto** del anuncio (`{{MODELO}}`).
- Repetir el diferencial: **suela ultraliviana e inyectada (no pintada)**.
- Reducir el miedo a comprar por internet: **pago contraentrega**, garantía,
  cambios de talla.
- Terminar **siempre con una pregunta** (talla o color), nunca con "quedo
  atento".
- Escasez/urgencia solo si es real (stock bajo o promo con fecha).

Variables a reemplazar (ajustar a la sintaxis de variables de Lucid Bot):
`{{NOMBRE}}`, `{{MODELO}}`, `{{PRECIO}}`, `{{PRECIO_ANTES}}`, `{{COLORES}}`,
`{{TALLAS}}`, `{{TIEMPO_ENTREGA}}`.

> ⚠️ Confirmar antes de publicar: si el envío es gratis para todos los
> pedidos, el tiempo de entrega real, los términos de la garantía y si hay
> descuento vigente. Si algo no aplica, quitar esa línea.

---

## Plantilla A – Botas ultralivianas

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 👋 Qué buena elección: la **{{MODELO}}** es una de las
> botas más pedidas de Atenas Store 🔥
> Mira cómo se ve puesta 👇
> *(foto/video del modelo)*

**Burbuja 2**
> Lo que más les gusta a nuestros clientes:
> ✅ **Suela ultraliviana**: pesa casi nada, la usas todo el día sin cansarte.
> ✅ **Suela inyectada, no pintada**: no se despega ni se pela con el uso.
> ✅ Diseño robusto que combina con jean, para trabajo o salir.
> ✅ Disponible en {{COLORES}}, tallas {{TALLAS}}.

**Burbuja 3**
> 💰 Precio hoy: **{{PRECIO}}** ~~{{PRECIO_ANTES}}~~
> 🚚 Envío a toda Colombia, llega en {{TIEMPO_ENTREGA}}.
> 💵 **Pagas cuando la recibes (contraentrega)**, o con Wompi, Addi o
> Sistecrédito.
> 🛡️ Garantía y cambio de talla si no te queda.
>
> Para separarte la tuya, **¿qué talla usas normalmente?** 👟

---

## Plantilla B – Deportivos

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 🙌 Te cuento del **{{MODELO}}**, el deportivo que está
> rompiendo en ventas este mes 🔥
> *(foto/video del modelo)*

**Burbuja 2**
> ¿Por qué lo eligen?
> ⚡ **Ultraliviano**: sientes que no llevas nada puesto.
> 🦶 Cómodo desde el primer día, ideal para caminar largas jornadas.
> 💪 **Suela inyectada (no pintada)**: más duración y mejor agarre.
> 🎨 Colores: {{COLORES}} · Tallas: {{TALLAS}}.

**Burbuja 3**
> Precio: **{{PRECIO}}** 💥
> 📦 Te llega a la puerta de tu casa en {{TIEMPO_ENTREGA}}, y **pagas al
> recibir**. También aceptamos Wompi, Addi y Sistecrédito.
>
> ¿En qué **color** lo quieres y qué **talla** usas? 😉

---

## Plantilla C – Clásico / todo negro (trabajo, uniforme)

**Burbuja 1**
> ¡Hola {{NOMBRE}}! 👋 El **{{MODELO}}** es perfecto si necesitas un calzado
> negro que aguante el día a día y se vea bien 👌
> *(foto del modelo)*

**Burbuja 2**
> ✔️ Todo negro, sirve para trabajo, uniforme o salir.
> ✔️ **Suela ultraliviana**: menos cansancio en jornadas largas.
> ✔️ **Suela inyectada**: no se pela ni se despega.
> ✔️ Tallas {{TALLAS}}.

**Burbuja 3**
> Precio: **{{PRECIO}}** · Contraentrega a toda Colombia 🚚
> ¿Qué **talla** te separo? 🖤

---

## Mensajes de apoyo (si el cliente no responde o duda)

**Seguimiento (10–15 min sin respuesta)**
> {{NOMBRE}}, ¿pudiste ver las fotos? 👀 Si me dices tu talla te confirmo de
> una vez si hay disponible en {{COLORES}} 👟

**Objeción: "¿Y si no me queda?"**
> ¡Tranquilo! 🙌 Si la talla no te queda, te hacemos el **cambio**. Y como
> pagas contraentrega, no arriesgas nada por adelantado. ¿Qué talla usas en
> tenis normalmente?

**Objeción: "¿Es confiable?"**
> Claro que sí 😊 Somos **Atenas Store S.A.S.**, empresa registrada en Cúcuta y
> enviamos a toda Colombia. Puedes pagar **cuando recibas** tu pedido. Mira lo
> que dicen nuestros clientes 👇 *(reseñas/videos de clientes)*

**Objeción: "Está caro"**
> Te entiendo 🙏 La diferencia está en la **suela inyectada y ultraliviana**:
> no se despega como las pintadas y te dura mucho más. Además puedes pagarlo a
> cuotas con **Addi o Sistecrédito**. ¿Te muestro cómo?

---

## Cómo medir si funciona

Probar A/B (versión actual vs. nueva) por 1–2 semanas con el mismo anuncio y
comparar:

- % de clientes que responden al primer mensaje.
- % de conversaciones que terminan en pedido.
- % de pedidos entregados vs. devueltos (que la promesa no genere devoluciones).
