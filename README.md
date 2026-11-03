# Invitación de boda · Jessica & Ricardo

Invitación interactiva para la boda del 19 de marzo de 2027 en Hermosillo, Sonora.
Sitio estático publicado en GitHub Pages: https://ricardoyjessica.com/

## Archivos

- `index.html` — la invitación (formato DC, usa `support.js`).
- `recomendaciones.html` — lugares para comer, con enlaces a Google Maps.
- `generador.html` — genera los enlaces y códigos QR personalizados de cada invitado.
- `assets/` — fotos, flores, iconos y la imagen de vista previa (`og.jpg`).

## Enlaces personalizados

El parámetro `?i=` es un base64 con campos separados por `|`:

- Individual o pareja: `invitado1|invitado2|2 si lleva +1|ID`
- Familia: `FAM|nombre|número de invitaciones|ID`

Cada invitado lleva un ID. Sin ID (o con datos incompletos) la confirmación se
muestra igual, pero **no se envía el correo**.

## Confirmación por correo

Se envía con EmailJS desde el navegador. El destinatario se configura en la
plantilla de EmailJS, no en el código.

## Probar en local

```bash
npx serve . -l 8082
```
