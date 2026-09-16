# Corte 1 — Plan de implementación

**Objetivo:** completar la lógica funcional y la evidencia pendiente del Gestor de Celulares para el Corte 1.

**Arquitectura:** la aplicación seguirá usando Kodular con TinyDB local. La sesión activa se identificará por el correo guardado en TinyDB; los registros de celulares se guardarán asociados a ese usuario y las pantallas de listado y reportes leerán únicamente sus datos.

**Tecnología:** Kodular Creator, TinyDB, Accelerometer Sensor y Location Sensor.

## Tareas

- [ ] Validar los campos del formulario de celulares: no vacíos, almacenamiento y precio numéricos, y valores mayores o iguales a cero.
- [x] Guardar y actualizar modelo, marca, almacenamiento y precio en TinyDB.
- [x] Cargar el listado/historial persistido y permitir eliminar el registro con confirmación.
- [x] Crear un reporte visible de las entradas almacenadas en TinyDB.
- [x] Mostrar eventos visuales para movimiento y cambio de ubicación.
- [x] Revisar rutas y verificar cero errores de bloques en las pantallas.
- [ ] Exportar el proyecto `.aia`, grabar la demostración en emulador Android y completar el enlace del video.

## Criterio de cierre

El desarrollo queda preparado cuando Kodular muestre cero errores de bloques, los datos se conserven en TinyDB, el listado y reporte lean la información guardada y los dos sensores tengan eventos visibles. La evidencia de ejecución en Companion/emulador, el archivo `.aia` exportado y el video se completan al disponer del entorno Android.
