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
- [ ] **Envío por Microsoft 365 (si se activó): quién tiene el secreto.** Vea [ENVIAR-CON-MICROSOFT.md](ENVIAR-CON-MICROSOFT.md).
  - **¿Se activó?** En la hoja **Encuesta de Servicio ADEP → Extensiones → Apps Script → ⚙️ Configuración
    del proyecto → Propiedades de la secuencia de comandos**. Si no existe `MS_SECRET`, el correo sale por Gmail
    y no hay nada que entregar: marque esta casilla como *no se activó*.
  - **Si existe:** el secreto está guardado en dos lugares, y ninguno depende de una persona:
    la propiedad `MS_SECRET` (la ve quien tenga la cuenta de Gmail de ADEP) y la aplicación **Encuesta ADEP**
    en Microsoft Entra (ahí ya no se puede volver a ver; solo crear uno nuevo). Anote en la entrega,
    **sin copiar el secreto**:
    - quién administra Microsoft 365 en ADEP (puede crear un secreto nuevo);
    - la **fecha de vencimiento** del secreto (Entra → Encuesta ADEP → Certificados y secretos) y quién lo renueva;
    - el correo que envía (`MS_REMITENTE`).
  - Si alguien guardó el valor del secreto aparte (papel, chat, nota), bórrelo: no hace falta tenerlo fuera de
    Apps Script. Si se compartió por un medio inseguro, pida a TI un secreto nuevo y borre el viejo en Entra.
