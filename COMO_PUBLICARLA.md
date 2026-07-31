# EIRA · Seguimiento — cómo publicarla

Sin programar, sin servidor y sin costo. Unos 15 minutos la primera vez.

## Qué hay en esta carpeta

| Archivo | Para qué |
|---|---|
| `index.html` | La app. Es lo que usa la paciente. |
| `enlaces.html` | **Uso interno tuyo.** Genera el enlace personalizado de cada paciente. No se lo mandes a nadie. |
| `manifest.webmanifest` | Hace que se pueda instalar como app. |
| `sw.js` | Hace que funcione sin internet. |
| `logo_eira.png`, `icon-192.png`, `icon-512.png` | Marca e iconos. |

Sube **todos** los archivos. Si falta uno, la app deja de instalarse o pierde el logo.

## Publicarla en GitHub Pages

1. Entra a github.com y crea un repositorio nuevo. Nómbralo `eira.seguimiento` y márcalo **Public**.
2. En el repositorio: `Add file` → `Upload files`. Arrastra los siete archivos de esta carpeta. `Commit changes`.
3. Ve a `Settings` → `Pages` (menú de la izquierda).
4. En *Source* elige `Deploy from a branch`. En *Branch* elige `main` y la carpeta `/ (root)`. `Save`.
5. Espera dos o tres minutos y recarga. Arriba aparece la dirección:
   `https://TUUSUARIO.github.io/eira.seguimiento/`

Esa es la dirección base.

> **Ojo con lo público.** El repositorio tiene que ser público para que Pages funcione gratis. Eso
> expone el *código* de la app, no los datos: ningún dato de paciente viaja ni se guarda ahí. Los
> registros viven únicamente en el teléfono de cada paciente.

## Personalizar por paciente

1. Abre `enlaces.html` en tu computador (doble clic, o desde la misma dirección de Pages).
2. Pega tu dirección base en el primer campo, reemplazando `USUARIO` por tu usuario de GitHub.
3. Llena nombre, fecha de inicio y las metas de esa paciente.
4. Copia el mensaje ya redactado y mándalo por WhatsApp.

Cuando ella abra el enlace, la app guarda sus metas en su teléfono. De ahí en adelante puede
entrar desde el icono, sin el enlace.

Si cambias una meta en un control, genera el enlace nuevo y pídele que lo abra una vez.

## Cómo la instala la paciente

- **iPhone:** abrir el enlace en Safari → botón de compartir → *Agregar a inicio*.
- **Android:** abrir en Chrome → menú de tres puntos → *Instalar aplicación*.

Instalada funciona sin internet y se ve como una app normal.

## Cómo te llegan los datos

El domingo la paciente toca **ENVIAR REPORTE POR WHATSAPP**. Se le abre WhatsApp con el reporte de
los siete campos ya escrito, dirigido a tu número. Tú lo recibes listo para leer y pasar al Excel
maestro.

## Actualizar la app más adelante

Sube el archivo nuevo al repositorio reemplazando el anterior. En `sw.js`, cambia
`eira-seguimiento-v1` por `v2` (o el número que siga): eso obliga a que a las pacientes les llegue
la versión nueva en vez de la guardada en su teléfono.

## Antes de mandarla a la primera paciente

- [ ] Los siete archivos están subidos y la dirección abre bien desde el celular.
- [ ] Tu número de WhatsApp quedó correcto en el generador de enlaces.
- [ ] La autorización de tratamiento de datos menciona el registro digital en dispositivo del paciente.
- [ ] Le explicaste que debe descargar un respaldo de vez en cuando desde la pestaña METAS.
