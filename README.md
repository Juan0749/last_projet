# Control de Pacientes (INGRESOS)

Aplicación web local para controlar pacientes, pagos y deudas.

## Cambios clave solicitados

- **Archivo de trabajo oculto/expandible**.
- Archivo de trabajo en modo simple (como versión anterior):
  - Crear archivo en Documentos.
  - Seleccionar archivo existente.
  - Guardar manualmente.
- **Nuevo ingreso** con método de pago: `EFECTIVO` o `TARJETA`.
- Se eliminó catálogo fijo de 50 productos y tratamientos.
- Nuevo módulo de **productos manuales** (crear/eliminar), persistentes en el mismo archivo local.
- Al crear paciente, el campo producto usa los productos manuales guardados.
- Se puede **editar paciente** y **agregar nuevos pagos** (separados de pago inicial), mostrando historial con fechas.
- Alertas por deuda >10 días desde el último pago.
- Estado de saldo en tabla: `FALTANTE` (rojo), `A FAVOR`, `AL DÍA`.

## Flujo recomendado

1. Abrir `index.html` en Chrome/Edge.
2. En **Archivo de trabajo** > **Crear archivo en Documentos** o **Seleccionar archivo existente**.
3. Crear productos en **Productos manuales**.
4. Registrar pacientes en **Nuevo ingreso**.
5. Usar **Editar / Pago** para actualizar datos y agregar pagos faltantes.

## Nota técnica

- Si el navegador no soporta File System Access API, la app conserva respaldo en `localStorage`.
- Se normaliza texto en MAYÚSCULAS para mantener búsquedas consistentes.
