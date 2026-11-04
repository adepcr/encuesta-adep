# Publicar la encuesta (GitHub Pages)

La encuesta se publica con **GitHub Pages**, desde este repositorio de la organización de ADEP.
No necesita llaves, contraseñas ni Firebase.

- Encuesta: **https://adepcr.github.io/encuesta-adep/**
- Resultados (solo organizadores, con clave): **https://adepcr.github.io/encuesta-adep/resultados.html**

Las respuestas no dependen de la página: siguen llegando a la hoja de Google de la cuenta de Gmail de ADEP
(vea [INSTALAR-BACKEND.md](INSTALAR-BACKEND.md)).

## Activar la página (una sola vez)

1. Abra <https://github.com/adepcr/encuesta-adep/settings/pages>.
2. **Source:** *Deploy from a branch*. **Branch:** `main` y carpeta `/ (root)`. Presione **Save**.
3. En uno o dos minutos la encuesta queda en la dirección de arriba.

Desde entonces, cada cambio que se sube a `main` se publica solo (tarda uno o dos minutos).

## La dirección anterior (adep-encuesta.web.app): desactivada

Antes la encuesta se publicaba en Firebase Hosting (proyecto `adep-encuesta`, cuenta de Gmail de ADEP).

- El **4 de noviembre de 2026** se desactivó el sitio: `adep-encuesta.web.app` ya no abre la encuesta.
  La única dirección es la de GitHub Pages (arriba). Las respuestas guardadas en la hoja de Google no se tocaron.
- El proyecto de Firebase sigue existiendo en la cuenta de Gmail de ADEP, sin sitio publicado y sin costo (plan Spark).
  Para entrar a Firebase, Google exige verificación en dos pasos en esa cuenta desde el 6 de noviembre de 2026.
- Se desactivó desde una terminal con:
  ```
  npx firebase-tools login
  npx firebase-tools hosting:disable --project adep-encuesta
  ```
  (La consola web nueva no muestra un botón para desactivar.) Para volver a encenderlo habría que publicar
  de nuevo con `firebase deploy`, pero no hace falta: la encuesta vive en GitHub Pages.

### Antes de entregar

- [x] **Sitio viejo en Firebase (`adep-encuesta`): desactivado** el 4 de noviembre de 2026.
