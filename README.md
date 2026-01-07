# Optimizacion-de-Windows-11
Optimización de Windows 11 configurando opciones de aplicaciones, apariencia, sugerencias y privacidad.

Recomendaciones en Inicio

Configuración - Personalización - Inicio
* Mostrar aplicaciones agregadas recientemente
* Mostrar archivos recomendados en inicio
* Mostrar recomendaciones

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Retirar widgets de la pantalla de bloqueo

Configuración - Personalización - Pantalla de bloqueo
* Estado de la pantalla de bloqueo - Ninguno
* Personalizar pantalla de bloqueo - imagen fija

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Retirar Notificaciones de experiencias de usuario

Configuración - Sistema - Notificaciones - Configuración adicional
* Mostrar la experiencia de Bienvenida
* Sugerir formas de sacar el máximo partido de Windows
* Obtener recomendaciones

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Bloquear Telemetría

Configuración - Privacidad y seguridad - Recomendaciones y ofertas
* Deshabilitar todo

Configuración - Privacidad y seguridad - Diagnostico y comentarios
* Enviar los datos de diagnostico 

Bloquear servicio de Telemetria en Service.msc y con archivo host

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Bloquear ubicación para apps

Configuración - Privacidad y seguridad - Ubicación

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Limpiar barra de tareas

Configuración - Personalización - Barra de tareas

* Windgets
* Barra de búsqueda

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Activar o desactivar notificaciones por separado

Configuración - Sistema - Notificaciones 
* Deshabilitar todo o solo no que no interese

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Quitar avisos en el explorador de archivos

Explorador de archivos - opciones - Ver

* Deshabilitar mostrar notificaciones del proveedor de sincronización 

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Deshabilitar función de ser visible en red

configuración - red e internet - configuración avanzada de red - configuración avanzada de uso compartido

* Detección de redes
* Uso compartido de archivos e impresoras (Publicas y privadas)


*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/
Bloquear acceso a Información de cuenta


Configuración - Privacidad y Seguridad - información de cuenta

* Deshabilitar Acceso a la información de la cuenta

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Deshabilitar programas que inician con Windows

Configuración - Aplicaciones - Inicio

Quitar todo lo que no necesitas que se inicien con Windows

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Quitar Blodware de forma Automatizada

* Ejecutar PowerShell como administrador
Ingresar el texto

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

confirmar con S

* Ejecutar el script removedor.ps1

* Ejecutar PowerShell como administrador
Ingresar el texto

Set-ExecutionPolicy Restricted -Scope CurrentUser

confirmar con S

Quitar Blodware de forma Manual

Configuración -  Aplicaciones  - Aplicaciones instaladas

Desinstalar las aplicaciones que no utilices que vienen con Windows

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Deshabilitar Recall

Configuración - Privacidad y Seguridad - Capturas de pantalla y grabación de pantalla

*Acceso a capturas de pantalla y grabación de pantalla

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Evitar aplicaciones en segundo plano

Configuración -  Aplicaciones  - Aplicaciones instaladas - Opciones - Opciones adicionales

* Opción de ejecutar en segundo plano - Nunca

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/

Menú contextual de Windows 10

Ejecutar cmd como administrador

Ingresar instrucción y ejecutar
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve   

