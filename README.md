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

1. Importar el archivo `.aia` en Kodular Creator.
2. Abrir el proyecto `Gestor de Celulares`.
3. Probarlo mediante Kodular Companion o generar el APK.
4. Crear un usuario y registrar celulares para verificar el CRUD y los reportes.

## Entrega

- Repositorio: https://github.com/DavidSantiagoEscamilla/gestor-de-celulares
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
- CRUD inicial de celulares conectado a TinyDB: guardar/actualizar usa la etiqueta `celular_modelo` y eliminar ejecuta `Clear Tag` con confirmación visual.
- Recuperación funcional con TinyDB: valida el correo vacío y consulta la contraseña usando el correo como etiqueta; si no existe, devuelve el valor predeterminado vacío.
- Pendiente: completar lectura parametrizada del listado, reportes parametrizados, sensores visibles y pruebas finales.
