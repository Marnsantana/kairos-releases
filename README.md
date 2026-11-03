# KAIROS — descargas oficiales

**KAIROS** es una aplicación de escritorio para Windows que ayuda a entrenadores de baloncesto a analizar partidos
grabados: abrir el partido, marcar acciones con el teclado, crear y anotar clips, organizarlos en sesiones y exportar
vídeos para jugadores y equipo técnico.

Este repositorio contiene **solo** lo necesario para descargar e instalar KAIROS y para que la aplicación se actualice
sola. No contiene el código fuente ni ningún dato de usuarios.

## Descargar

> **Estado: todavía no hay ninguna versión pública.** La primera aparecerá en
> [Releases](../../releases) cuando esté lista. Hasta entonces, no hay nada que descargar aquí.

Cuando exista, descarga siempre desde la página de [Releases](../../releases) **la versión marcada como «Latest»**:

| Archivo | Para qué sirve |
|---|---|
| `KAIROS-Setup-X.Y.Z.exe` | **El instalador. Es lo único que necesitas.** |
| `KAIROS-Setup-X.Y.Z.exe.sha256` | Suma de comprobación para verificar la descarga (opcional) |
| `update-manifest.json` y `update-manifest.json.sig` | Los usa KAIROS para actualizarse con seguridad; no hace falta abrirlos |

## Instalar (3 pasos)

1. Descarga y ejecuta `KAIROS-Setup-X.Y.Z.exe`. **No necesita permisos de administrador** y no hay que instalar nada más
   (Python, VLC y FFmpeg ya van incluidos).
2. Sigue el asistente (puedes crear un acceso directo en el escritorio).
3. Abre **KAIROS** desde el menú Inicio y empieza a trabajar.

Requisitos: Windows 10 u 11 de 64 bits.

**Aviso de Windows (SmartScreen).** De momento el instalador no lleva firma de Microsoft, así que la primera vez Windows
puede mostrar «Windows protegió su PC». Pulsa **Más información → Ejecutar de todas formas**. Si quieres comprobar que el
archivo es el original, compara su SHA-256 con el del archivo `.sha256` de la misma versión:

```powershell
Get-FileHash .\KAIROS-Setup-X.Y.Z.exe -Algorithm SHA256
```

## Actualizaciones

KAIROS comprueba al abrirse si hay una versión nueva. Si la hay, te lo indica con un aviso discreto:
**«Nueva versión disponible»** → **Actualizar ahora** / **Más tarde** / **Ver novedades**. Con «Actualizar ahora» descarga
la actualización, **comprueba su firma digital**, se reinicia y vuelve a abrirse sola. Tus proyectos, clips, sesiones,
categorías y preferencias **no se tocan**. Solo se ofrecen versiones estables.

## Tus datos

KAIROS guarda tu biblioteca en tu propio equipo (`%LOCALAPPDATA%\BasketAnalisis`), separada del programa. Instalar,
actualizar o desinstalar KAIROS **no borra ni modifica esa carpeta**. Tus vídeos originales nunca se modifican. La
sincronización con Google Drive es opcional y solo envía metadatos, nunca vídeos.

## Soporte

¿Algo no funciona? Abre una [incidencia](../../issues) indicando tu versión de Windows y la versión de KAIROS (menú
**Ayuda → Acerca de**). No adjuntes vídeos ni datos personales.

## Licencias de terceros

KAIROS incluye componentes de terceros (entre otros VLC/libVLC, FFmpeg y Qt, bajo licencias LGPL). Sus avisos, las
condiciones y los enlaces al código fuente de esos componentes están en [`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt)
y se instalan junto con la aplicación.

---
© KAIROS. Todos los derechos reservados. Las condiciones de uso se publicarán junto con la primera versión.
