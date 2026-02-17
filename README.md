# Control de Pacientes

Interfaz web simple para registrar pacientes, tratamientos, abonos y alertas por deudas mayores a 10 días.

## Uso rápido

1. Abre `index.html` en Chrome/Edge.
2. Pulsa **Crear archivo en Documentos** para generar un JSON en tu carpeta Documentos.
3. Si ya tienes un archivo, pulsa **Seleccionar archivo existente**.
4. Cada nuevo paciente se guarda en memoria y, si hay archivo activo, también se escribe en ese archivo.
5. Al refrescar, la página intenta recuperar automáticamente el último archivo usado (si el navegador mantiene permisos).

## Búsqueda

- El buscador se abre/cierra con un botón de icono.
- Puedes filtrar por **palabra clave**, **fecha inicio** y **fecha fin**.
- La búsqueda no discrimina entre mayúsculas y minúsculas.
- Los nuevos registros se almacenan en MAYÚSCULAS para mantener consistencia.

## Alertas y saldos

- Se muestra alerta cuando el paciente tiene deuda pendiente y pasaron más de 10 días desde la fecha de ingreso.
- En la tabla se muestra estado de saldo:
  - `FALTANTE` (resaltado en rojo).
  - `A FAVOR` cuando pagó de más.
  - `AL DÍA` cuando no hay diferencia.

## Nota técnica

La escritura en archivos locales usa **File System Access API** (Chrome/Edge). En navegadores sin soporte, funcionará solo el respaldo local en `localStorage`.

## Instalar `xmllint`

- Ubuntu / Debian: `sudo apt update && sudo apt install -y libxml2-utils`
- Fedora / RHEL / CentOS: `sudo dnf install -y libxml2`
- Alpine: `sudo apk add libxml2-utils`
- macOS (Homebrew): `brew install libxml2`

Verificación: `xmllint --version`
