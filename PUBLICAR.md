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

## La dirección anterior (adep-encuesta.web.app)

Antes la encuesta se publicaba en Firebase Hosting (proyecto `adep-encuesta`, cuenta de Gmail de ADEP).

- Esa dirección **sigue funcionando** con la última versión que se publicó ahí, y las respuestas que lleguen
  por ella también se guardan en la misma hoja. No recibe cambios nuevos.
- Reparta la dirección nueva. Cuando ya nadie use la vieja, se puede apagar en la consola de Firebase:
  **Hosting → … → Desactivar sitio**. Para entrar a Firebase, Google exige verificación en dos pasos
  en la cuenta desde el 6 de noviembre de 2026.

### Antes de entregar

- [ ] **Sitio viejo en Firebase (`adep-encuesta`): desactivado o entregado.** Una de las dos:
  - **Desactivado:** en <https://console.firebase.google.com/project/adep-encuesta/hosting/sites>,
    en el sitio `adep-encuesta` → **⋮ → Desactivar sitio**. La dirección `adep-encuesta.web.app` deja de abrir;
    las respuestas ya guardadas en la hoja de Google no se tocan.
  - **Entregado:** en **⚙ Configuración del proyecto → Usuarios y permisos → Agregar miembro**, dar el rol
    **Propietario** a la persona que recibe (o confirmar que ella tiene la cuenta de Gmail de ADEP,
    con la verificación en dos pasos a su nombre). Después, quitar el acceso propio.
