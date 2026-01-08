# Optimización de Windows 11
Este repositorio muesta como realizar la optimización de Windows 11 configurando y/o deshabilitando opciones de aplicaciones, apariencia, sugerencias y privacidad, la mayoria desde el menú de Configuración que viene por defecto.

## Retirar notificaciones de experiencias de usuario y de aplicaciones

Para retirar las notificaciones de Windows que generan las aplicaciones que se tienen instaladas en el equipo, así como las notificaciones que te muestra para configurar algún servicio propio de Microsoft (como Copilot, OneDrive, etc.) se puede realizar desde:

**Configuración - Sistema - Notificaciones**

### Activar o desactivar notificaciones de aplicaciones instaladas por separado

En el apartado de **"Notificaciones de aplicaciones y otros remitentes"**, ubicar las aplicaciones de las cuales se requiere deshabilitar las notificaciones y pulsar el interruptor al modo **Desactivado**

![Deshabilitar notificaciones de aplicaciones](/images/Notificaciones_de_aplicaciones.jpg)


### Notificaciones de experiencias de usuario

En el apartado de **"Notificaciones de aplicaciones y otros remitentes"**, ubicar y abrir **"Configuración adicional"** y deshabilitar las opciones:

* Muestra la experiencia de bienvenida de Windows después de las actualizaciones y cuando haya iniciado sesión para mostrar las novedades.
* Sugerir formas de sacar el máximo partido de Windows y finalizar la configuración de este dispositivo.
* Obtener recomendaciones y sugerencias al usar Windows.

![Deshabilitar notificaciones de experiencias de usuario](/images/Notificaciones_de_experiencias_de_usuario.jpg)

---
---

## Deshabilitar función de ser visible en la red

Para evitar que se el equipo pueda ser visible por otros equipos dentro de una red al a la que se esta conectando, se tiene que ingresar a: 

**Configuración - Red e Internet - Configuración avanzada de red - Configuración avanzada de uso compartido**

Tanto en las opciones de Redes Privadas como Redes Publicas se tienen que deshabilitar las opciones de:

* Detección de redes.
* Uso compartido de archivos e impresoras.

![Deshabilitar ser visible en la red](/images/Visibilidad_en_la_red.jpg)

---
---

## Retirar recomendaciones en Inicio de Windows

Para las recomendaciones que Windows te muestra siempre al abrir el menu de inicio se tiene que ingresar a: 

**Configuración - Personalización - Inicio**

y deshabilitar las siguientes opciones:

* Mostrar aplicaciones agregadas recientemente.
* Mostrar archivos recomendados en Inicio, archivos recientes en el Explorador de archivos y elementos en Listas de accesos directos.
* Mostrar recomendaciones para sugerencias, accesos directos, nuevas aplicaciones y mucho más.

![Deshabilitar recomendaciones de inicio](/images/Recomendaciones_de_inicio.jpg)

---
---

## Retirar widgets de la pantalla de bloqueo

Configuración - Personalización - Pantalla de bloqueo
* Estado de la pantalla de bloqueo - Ninguno
* Personalizar pantalla de bloqueo - imagen fija

![Descripción de la imagen](/images/picture.jpg)

---
---

## Limpiar barra de tareas

Configuración - Personalización - Barra de tareas

* Windgets
* Barra de búsqueda

![Descripción de la imagen](/images/picture.jpg)

---
---

## Bloquear Telemetría

Configuración - Privacidad y seguridad - Recomendaciones y ofertas
* Deshabilitar todo

Configuración - Privacidad y seguridad - Diagnostico y comentarios
* Enviar los datos de diagnostico 

Bloquear servicio de Telemetria en Service.msc y con archivo host

![Descripción de la imagen](/images/picture.jpg)

---
---

## Bloquear ubicación para apps

Configuración - Privacidad y seguridad - Ubicación

![Descripción de la imagen](/images/picture.jpg)

---
---

## Quitar avisos en el explorador de archivos

Explorador de archivos - opciones - Ver

* Deshabilitar mostrar notificaciones del proveedor de sincronización 

![Descripción de la imagen](/images/picture.jpg)

---
---
## Bloquear acceso a Información de cuenta


Configuración - Privacidad y Seguridad - información de cuenta

* Deshabilitar Acceso a la información de la cuenta

![Descripción de la imagen](/images/picture.jpg)


---
---



## Quitar Blodware (programas que vienen instalados con Windows)

### De forma Automatizada

* Ejecutar PowerShell como administrador
Ingresar el texto

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

confirmar con S

* Ejecutar el script removedor.ps1

* Ejecutar PowerShell como administrador
Ingresar el texto

Set-ExecutionPolicy Restricted -Scope CurrentUser

confirmar con S

![Descripción de la imagen](/images/picture.jpg)


### De forma Manual

Configuración -  Aplicaciones  - Aplicaciones instaladas

Desinstalar las aplicaciones que no utilices que vienen con Windows

Deshabilitar programas que inician con Windows

Configuración - Aplicaciones - Inicio

Quitar todo lo que no necesitas que se inicien con Windows

![Descripción de la imagen](/images/picture.jpg)

---
---

## Deshabilitar Recall

Configuración - Privacidad y Seguridad - Capturas de pantalla y grabación de pantalla

*Acceso a capturas de pantalla y grabación de pantalla

![Descripción de la imagen](/images/picture.jpg)

---
---

## Evitar aplicaciones en segundo plano

Configuración -  Aplicaciones  - Aplicaciones instaladas - Opciones - Opciones adicionales

* Opción de ejecutar en segundo plano - Nunca

![Descripción de la imagen](/images/picture.jpg)

---
---

## Menú contextual de Windows 10

Ejecutar cmd como administrador

Ingresar instrucción y ejecutar

```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve   
```

![Descripción de la imagen](/images/picture.jpg)
