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

- Repositorio: https://github.com/DavidSantiagoEscamilla/gestor-de-celulares
- Proyecto Kodular: https://creator.kodular.io/#310887870258310564
- Archivo `.aia`: pendiente de confirmar en la carpeta de descargas después de exportarlo desde Kodular.
- Video: pendiente de publicación.

## Estado de construcción

- Interfaz y navegación base configuradas en Kodular.
- Navegación entre inicio, registro, recuperación, menú, administración, listado, reportes y sensores conectada.
- Pantallas de formulario, listado, reportes, recuperación y sensores creadas.
- TinyDB compartido con el espacio `GestorDeCelulares`.
- Acelerómetro y sensor de ubicación añadidos a `ScreenSensores`.
- Registro funcional: correo como clave y contraseña como valor en TinyDB, con confirmación visual.
- Autenticación local funcional: el correo consulta la contraseña guardada en TinyDB y la compara con la ingresada antes de abrir `ScreenMenu`.
- Navegación corregida: `Registrarse` abre `ScreenRegistro` y `Recuperar contraseña` abre `ScreenRecuperar`.
- Retornos visibles añadidos: los módulos principales regresan a `ScreenMenu`, mientras registro y recuperación regresan a `Screen1`.
- Validación estática de navegación realizada en Kodular: rutas revisadas en las ocho pantallas y `0` errores de bloques; los avisos restantes son advertencias del diseñador.
- CRUD de celulares conectado a TinyDB: guardar/actualizar conserva modelo, marca, almacenamiento y precio en una lista bajo la etiqueta `celular_modelo`; eliminar ejecuta `Clear Tag` con confirmación visual.
- Recuperación funcional con TinyDB: valida el correo vacío y consulta la contraseña usando el correo como etiqueta; si no existe, devuelve el valor predeterminado vacío.
- Validación de datos reforzada: almacenamiento usa entrada numérica entera y precio usa entrada decimal; registro, login y recuperación muestran validaciones de campos vacíos.
- Listado/historial conectado: `ScreenListado` carga automáticamente el registro persistido desde TinyDB al inicializarse.
- Reporte conectado: `ScreenReportes` carga las entradas almacenadas en TinyDB dentro de un `List View`.
- Sensores conectados: acelerómetro y ubicación tienen eventos que actualizan visualmente la pantalla `ScreenSensores`.
- Pendiente de evidencia: ejecutar el recorrido completo en Kodular Companion o emulador Android, capturar las pruebas y publicar el video; no se marca como ejecutado porque actualmente no hay un dispositivo Android disponible.
