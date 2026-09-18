# Gestor de Celulares

Aplicación móvil desarrollada en Kodular para el ejercicio 11 de la actividad de desarrollo de aplicaciones.

## Autor

David Santiago Escamilla Castro  
descamillac@unicartagena.edu.co

## Corte 1

- Tecnología: Kodular.
- Persistencia: TinyDB local.
- Entidad principal: Celulares.
- Entidad obligatoria: Usuario.
- Sensores: acelerómetro y ubicación.

## Funcionalidades

- Registro, inicio de sesión y recuperación de contraseña.
- CRUD de usuarios y celulares.
- Historial personal de celulares.
- Reportes parametrizados.
- Detección de movimiento y captura de ubicación.

## Ejecución

1. En Kodular Creator, usar `Project > Export selected project (.aia)` para descargar el archivo fuente.
2. Importar ese `.aia` en otra cuenta o abrir directamente el proyecto `Gestor de Celulares`.
3. Probarlo mediante Kodular Companion o un emulador Android.
4. Crear un usuario y registrar celulares para verificar el CRUD, el listado y el reporte.

## Entrega

- Repositorio: [gestor-de-celulares](https://github.com/DavidSantiagoEscamilla/gestor-de-celulares)
- Proyecto Kodular: [Gestor de Celulares](https://creator.kodular.io/#310887870258310564)
- Archivo `.aia`: [GestorDeCelulares.aia](GestorDeCelulares.aia)
- APK: [GestorDeCelulares.apk](GestorDeCelulares.apk)
- Video demostrativo: [ver video en YouTube](https://youtu.be/gk4jm_BIegM)

El video presenta el funcionamiento de la aplicación, la navegación entre pantallas, la autenticación, el CRUD, la persistencia local y el uso del acelerómetro y del sensor de ubicación.

## Estado de construcción

- [x] Interfaz y navegación base configuradas en Kodular.
- [x] Navegación entre inicio, registro, recuperación, menú, administración, listado, reportes y sensores conectada.
- [x] Diez pantallas creadas para el flujo de autenticación, administración, celulares, reportes y sensores.
- [x] TinyDB compartido con el espacio `GestorDeCelulares`.
- [x] Acelerómetro y sensor de ubicación añadidos a `ScreenSensores`, con actualización visual de movimiento, latitud y longitud.
- [x] Registro funcional: correo como clave y contraseña como valor en TinyDB, con confirmación visual.
- [x] Autenticación local funcional: el correo consulta la contraseña guardada en TinyDB y la compara con la ingresada antes de abrir `ScreenMenu`.
- [x] Cierre de sesión que limpia la variable del usuario activo y retorna a `Screen1`.
- [x] Navegación corregida: `Registrarse` abre `ScreenRegistro` y `Recuperar contraseña` abre `ScreenRecuperar`.
- [x] Retornos visibles añadidos: los módulos principales regresan a `ScreenMenu`, mientras registro y recuperación regresan a `Screen1`.
- [x] Validación estática de navegación realizada en Kodular: rutas revisadas en las diez pantallas y `0` errores de bloques.
- [x] CRUD de celulares conectado a TinyDB: guardar, consultar, actualizar y eliminar conserva modelo, marca, almacenamiento y precio asociados al usuario activo.
- [x] CRUD de usuarios conectado a TinyDB: el panel de administración lista usuarios, permite actualizar contraseñas y eliminar cuentas.
- [x] Recuperación funcional con TinyDB: valida el correo vacío y consulta la contraseña usando el correo como etiqueta.
- [x] Validación de datos reforzada: almacenamiento usa entrada numérica entera, precio usa entrada decimal y los formularios validan campos vacíos y datos incorrectos.
- [x] Listado e historial conectados: `ScreenListado` carga automáticamente los registros persistidos desde TinyDB.
- [x] Reportes conectados: `ScreenReportes` carga las entradas almacenadas en TinyDB dentro de un `List View`.
- [x] Video demostrativo publicado en YouTube y enlazado en la sección de entrega.

## Verificación final pendiente

Los archivos fuente y la APK ya están incorporados al repositorio local. Después de subir los cambios a GitHub, se comprobará que el repositorio sea público, que ambos archivos se puedan descargar y que la APK abra correctamente.
