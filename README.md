# Optimizacion de Windows 11
Este repositorio muesta como realizar la optimización de Windows 11 configurando y/o deshabilitando opciones de aplicaciones, apariencia, sugerencias y privacidad, la mayoria desde el menú de Configuración que viene por defecto.

## Retirar notificaciones de experiencias de usuario y de aplicaciones

Para retirar las notificaciones de Windows que generan las aplicaciones que se tienen instaladas en el equipo, así como las notificaciones que te muestra para configurar algún servicio propio de Microsoft (como Copilot, OneDrive, etc.) se puede realizar desde:

Configuración - Sistema - Notificaciones

### Activar o desactivar notificaciones de aplicaciones instaladas por separado

- En el apartado de "Notificaciones de aplicaciones y otros remitentes", ubicar las aplicaciones de las cuales se requiere deshabilitar las notificaciones y pulsar el interruptor al modo Desactivado

![Deshabilitar notificaciones de aplicaciones](/images/Notificaciones_de_aplicaciones.jpg)


### Notificaciones de experiencias de usuario

 - En el apartado de "Notificaciones de aplicaciones y otros remitentes", ubicar y abrir "Configuración adicional" y deshabilitar las opciones:
  
    * Muestra la experiencia de bienvenida de Windows después de las actualizaciones y cuando haya iniciado sesión para mostrar las novedades.
    * Sugerir formas de sacar el máximo partido de Windows y finalizar la configuración de este dispositivo.
    * Obtener recomendaciones y sugerencias al usar Windows.

![Deshabilitar notificaciones de experiencias de usuario](/images/Notificaciones_de_experiencias_de_usuario.jpg)


*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/



Configuración - Sistema - Notificaciones 
* Deshabilitar todo o solo no que no interese

*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/





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

Limpiar barra de tareas

Configuración - Personalización - Barra de tareas

* Windgets
* Barra de búsqueda

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

