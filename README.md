# simkinaps-legal

Documentos legales públicos de las apps de Simkinaps, servidos con GitHub Pages.

**Este repo es público a propósito** y es el único que lo es. Apple y Google
exigen que la política de privacidad esté en una URL pública y accesible sin
login. Aquí no va nada del código de las apps: eso vive en `SimkinJenkins/Simkinaps`,
que es privado.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Política de privacidad de MoonGardening, EN + ES con selector de idioma. |
| `horometro/index.html` | Política de privacidad de Horometro. |
| `sumadora/index.html` | Soporte y política de privacidad de Sumadora, ES + EN. |

## Cómo se publica

Ajustes del repo → Pages → Source: `Deploy from a branch` → rama `main`, carpeta
`/ (root)`. La URL queda en:

```
https://simkinjenkins.github.io/simkinaps-legal/
```

Esa es la que se pega en App Store Connect (App Privacy → Privacy Policy URL) y,
cuando toque, en la ficha de Google Play.

## Estado

Los tres huecos ya están rellenos (2026-09-04) y el banner de borrador retirado:

- Fecha de publicación: 4 de septiembre de 2026.
- Desarrollador: Patricio Bravo Cisneros (cuenta de Apple **Individual**, así que
  Apple publica el nombre legal como vendedor; los dos deben coincidir).
- Contacto: simkin.developer@gmail.com.

Si alguna vez cambia el nombre de vendedor en App Store Connect, hay que cambiarlo
aquí el mismo día: una ficha y una política que se contradicen es motivo de rechazo.

## Mantenerla veraz

La política afirma cosas concretas sobre la app, y esas afirmaciones se
verificaron contra el código el 2026-09-04:

- Sin cuentas ni login, sin StoreKit, sin IDFA/ATT, sin push remoto, sin
  `URLSession`. Notificaciones locales. Firebase Analytics presente en iOS.
- **Android no tiene Firebase**: su `AnalyticsLogger` solo escribe en logcat y
  nada sale del dispositivo. Si se publica en Play antes de enchufar Firebase,
  la sección de analítica no describe la versión Android.

Si cambia cualquiera de esos hechos —se añade un paywall, ads, o sync en la
nube— hay que actualizar **esta política, la App Privacy label de Apple y el
formulario de Data Safety de Google** antes de que la feature se publique.
