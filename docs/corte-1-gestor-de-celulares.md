# Gestor de Celulares Corte 1

## Datos de la entrega

- Estudiante: David Santiago Escamilla Castro
- Correo institucional: descamillac@unicartagena.edu.co
- Ejercicio: 11 Celulares
- Tecnología: Kodular
- Persistencia: TinyDB en el dispositivo

## Alcance

La aplicación permite registrar usuarios y administrar un inventario personal de celulares. Cada usuario puede crear, consultar, actualizar y eliminar únicamente sus propios registros.

## Pantallas

1. `ScreenLogin`: inicio de sesión y acceso a registro y recuperación.
2. `ScreenRegistro`: creación de usuario con nombre, correo, contraseña y pregunta de seguridad.
3. `ScreenRecuperar`: recuperación de acceso mediante correo y pregunta de seguridad.
4. `ScreenMenu`: navegación a celulares, reportes y sensores.
5. `ScreenCelulares`: formulario de creación y edición.
6. `ScreenListado`: consulta y eliminación de celulares.
7. `ScreenReportes`: reportes parametrizados.
8. `ScreenSensores`: lectura de acelerómetro y ubicación.

## Datos

### Usuario

`id`, `nombre`, `email`, `password`, `preguntaSeguridad`, `respuestaSeguridad`

### Celulares

`id`, `usuarioEmail`, `marca`, `email`, `pulgadas`, `megapx`, `ram`, `almacenamientoPpal`, `almacenamientoSecun`, `sistemaOperativo`, `operador`, `tecnologiaDeBanda`, `wifi`, `bluetooth`, `camaras`, `marcaCpu`, `velocidadCpu`, `nfc`, `huella`, `ir`, `resistenteAgua`, `cantidadSim`

## Persistencia local

TinyDB utilizará estas etiquetas:

- `usuarios`: lista de objetos de usuario.
- `celulares`: lista de objetos de celulares.
- `sesionActiva`: correo del usuario autenticado.

Todos los registros de celulares se filtran por `usuarioEmail` antes de mostrarse.

## Sensores

- `AccelerometerSensor`: detecta movimiento fuerte y solicita confirmación antes de limpiar el formulario.
- `LocationSensor`: obtiene latitud y longitud al guardar un celular; la ubicación se conserva como información adicional del registro.

## Reportes parametrizados

### Reportes de usuarios

1. Usuarios registrados por nombre o fragmento de correo.
2. Usuarios con o sin registros de celulares.

### Reportes de celulares

1. Celulares filtrados por marca, sistema operativo u operador.
2. Celulares filtrados por rango de RAM, pulgadas o cantidad de SIM.

## Validaciones

- Campos obligatorios no vacíos.
- Correo con formato válido.
- Correo de usuario único.
- Contraseña y confirmación coincidentes.
- Valores numéricos mayores o iguales a cero.
- Pulgadas, megapíxeles, RAM, almacenamiento y velocidad de CPU con formato numérico.
- Cantidad de SIM como número entero positivo.
- Opciones booleanas para Wi-Fi, Bluetooth, NFC, huella, IR y resistencia al agua.

## Criterios de aceptación

- Un usuario puede registrarse e iniciar sesión.
- Un usuario no puede consultar ni modificar celulares de otra cuenta.
- El CRUD funciona después de cerrar y volver a abrir la app.
- Los dos reportes de usuarios y los dos de celulares aceptan parámetros.
- Los dos sensores se activan y su funcionamiento se puede demostrar en el video.
- La aplicación muestra mensajes claros de éxito, error y validación.
