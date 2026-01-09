# Optimización de Windows 11
Este repositorio muesta como realizar la optimización de Windows 11 configurando y/o deshabilitando opciones de aplicaciones, apariencia, sugerencias y privacidad, la mayoria desde el menú de Configuración que viene por defecto.

## Retirar notificaciones de experiencias de usuario y de aplicaciones

Para retirar las notificaciones de Windows que generan las aplicaciones que se tienen instaladas en el equipo, así como las notificaciones que te muestra para configurar algún servicio propio de Microsoft (como Copilot, OneDrive, etc.) se puede realizar desde:

**Configuración - Sistema - Notificaciones**

### Activar o desactivar notificaciones de aplicaciones instaladas por separado

En el apartado de **"Notificaciones de aplicaciones y otros remitentes"**, ubicar las aplicaciones de las cuales se requiere deshabilitar las notificaciones y pulsar el interruptor al modo **Desactivado**.

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

Tanto en las opciones de **Redes Privadas** así como **Redes Publicas** se tienen que deshabilitar las opciones de:

* Detección de redes.
* Uso compartido de archivos e impresoras.

![Deshabilitar ser visible en la red](/images/Visibilidad_en_la_red.jpg)

---
---

## Retirar widgets de la pantalla de bloqueo

Para retirar los Widgets de noticias e información de productos de Microsoft que se muestran en la pantalla de bloqueo, así como dejar una imagen fija, se tiene que ingresar a:

**Configuración - Personalización - Pantalla de bloqueo**

y se tienen que cambiar las opciones: 

* Personalizar pantalla de bloqueo a **Imagen**.
> [!NOTE]
> 
> Se puede seleccionar una imagen ya almacenada en el equipo con el botón **Examinar Fotos**.
* Estado de la pantalla de bloqueo a **Ninguno**.

![Retirar widgets de la pantalla de bloqueo](/images/Widgets_pantalla_bloqueo.jpg)

---
---

## Retirar recomendaciones en Inicio de Windows

Para deshabilitar las recomendaciones que Windows te muestra siempre al abrir el menu de inicio se tiene que ingresar a: 

**Configuración - Personalización - Inicio**

y deshabilitar las siguientes opciones:

* Mostrar aplicaciones agregadas recientemente.
* Mostrar archivos recomendados en Inicio, archivos recientes en el Explorador de archivos y elementos en Listas de accesos directos.
* Mostrar recomendaciones para sugerencias, accesos directos, nuevas aplicaciones y mucho más.

![Deshabilitar recomendaciones de inicio](/images/Recomendaciones_de_inicio.jpg)

---
---

## Limpiar barra de tareas

Este apartado hace referencia al retiro de los Widgets de noticias y el botón de busqueda en la barra de tareas de Windows, para ello se tienen que ingresar a:

**Configuración - Personalización - Barra de tareas**

y en el apartado de **Elementos de la barra de tareas** cambiar las opciones de:

* Buscar a **Ocultar**.
* Windgets a **Desactivado**.

![Limpiar barra de tareas](/images/Barra_tareas.jpg)

---
---

## Quitar Blodware (programas que vienen instalados con Windows)

Es recomendable retirar los programas que vienen por defecto en Windows que no utilices (como los servicios de Xbox, Bing, Teams, Sugerencias, etc.) para evitar uso de espacio en disco y procesos en segundo plano innecesarios que consuman recursos.

### De forma Manual

Para revisar el listado de programas que vienen por defecto y eliminar los que creemos convenientes se tiene que ingresar a:

**Configuración -  Aplicaciones  - Aplicaciones instaladas**

y dar click en el botón de **Opciones** de los programas identificados y selecionar la opción de **Desinstalar**.

![Retirar Blodware de forma manual](/images/Blodware_manual.jpg)

### De forma Automatizada

Este proceso se puede realizar también mediante un script el cual viene incluido en este repositorio, que se ejecuta por medio de PowerShell, en el que se enlistan los siguientes servicios a desinstalar:

1. Microsoft GamingAp
2. Xbox Gaming Overla
3. Xbox Identity Provide
4. Gaming Service
5. Microsoft BingWeathe
6. Microsoft Windows People Experience Host
7. Microsoft XboxGame Callable UI
8. Microsoft Xbox Speech To Text Overlay
9. Microsoft Outlook For Windows
10. MSTeams
11. Microsoft Xbox TCUI
12. Microsoft BingNews
13. Microsoft GetHelp
14. Microsoft PowerAutomate Desktop
15. Microsoft Microsoft Solitaire Collection
16. Microsoft Microsoft Office Hub
17. Clipchamp Clipchamp
18. Microsoft BingSearch
19. Microsoft Windows Client CoreAI
20. Microsoft Windows Feedback Hub

Para realiza este proceso se tiene que habilitar la ejecución de scripts de Windows mediante PowerShell, de la siguiente manera:

* Ejecutar **PowerShell** como administrador e ingresar la siguiente instrucción y confirmar la instrucción tecleando S:

```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

![Activar permisos de ejecución de script](/images/Activar_permiso_scripts.jpg)

* Ejecutar el script removedor.ps1 (clic derecho al script y ejecutar con PowerShell)

![Eecutar scrip removedor](/images/Ejecutar_script.jpg)

* En la misma ventana de PowerShell que se habilito el permiso de uso de scripts, se tiene que ingresar la siguiente instrucción y confirmar la instrucción tecleando S para deshabilitar ejecución de scripts:

```
Set-ExecutionPolicy Restricted -Scope CurrentUser
```

![Desactivar permisos de ejecución de script](/images/Desactivar_permiso_scripts.jpg)

---
---

## Evitar aplicaciones en segundo plano

Con la finalidad de evitar consumo de recursos innecesarios en el sistema se pueden deshabilitar la opcion de ejecutar en segundo plano los programas instalados, desde:

**Configuración -  Aplicaciones  - Aplicaciones instaladas - Opciones - Opciones avanzadas**

y en el apartado **Permisos de aplicaciones en segundo plano** cambiar la siguiente opción:

* Permitir que esta aplicación se ejecute en segundo plano a **Nunca**.

![Descripción de la imagen](/images/Programas_segundo_plano.jpg)

---
---

## Deshabilitar programas que inician al arrancar Windows

Para mejor el arranque de Windows, se tiene que deshabilitar el arranque de programas que no son necesarios desde inicio desde:

**Configuración - Aplicaciones - Inicio**

Y quitar todo lo que no necesitas que se inicien con Windows cambiando el interruptor al modo **Desactivado**.

![Deshabilitar programas que inician con Windows](/images/Programas_inicio_windows.jpg)

---
---

## Bloquear Telemetría

Windows desde siempre tiene de raiz la recolección de datos de todo lo que se hace en el sistema, y para evitar esta intromisión se tiene que ingresar a: 

**Configuración - Privacidad y seguridad - General**

y se tienen que **Deshabilitar** todas las opciones de este apartado. 

![Deshabilitar opciones de privacidad general](/images/Privacidad_general.jpg)

posteriormente ingresar a:

**Configuración - Privacidad y seguridad - Diagnostico y comentarios**

y en el apartado de **Datos de diagnóstico**, **Desactivar** la opción de **Enviar los datos de diagnóstico opcionales.**

![Deshabilitar opciones de privacidad de diagnosticos](/images/Privacidad_diagnostico.jpg)

también se tiene que ingresar a **Servicios de Windows** desde el apartado de **Ejecutar** e ingresar el comando:

```
service.msc
```

ubicar el servicio de **Experiencia del usuario y telemetría asociadas** y dar clic derecho en el y seleccionar **Propiedades**, presionar el botón **Detener** y posteriomente cambiar la opción de **Tipo de inicio** a **Deshabilitado**.

![Deshabilitar servicio de experiencia de usuario](/images/Servicio_experiencia_usuario.jpg)

Por ultimo se puede bloquear la conexión de servidores a donde se envia la información recopilada del sistema agregando información al archivo host (aquí se agrega un archivo que puedes usar para reemplazarlo). 

![Bloquear DNS](/images/Archivo_host.jpg)

Se puede consultar el repositorio de [hagezi/dns-blocklist](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#native) para mayor información, en el apartado de **Native Tracker - Windows/Host**

---
---

## Bloquear ubicación para apps

Para evitar que los programas tengan acceso a la ubicación del equipo se ingresa a:

**Configuración - Privacidad y seguridad - Ubicación**

y cambiar la opción de **Servicios de ubicación** a **Desactivado**.

![Deshabilitar ubicación](/images/Privacidad_ubicacion.jpg)

---
---

## Bloquear acceso a Información de cuenta

Para evitar que los programas instalados tengan acceso a la información de cuenta de usuario del equipo se ingresa a:


**Configuración - Privacidad y Seguridad - información de cuenta**

y cambiar la opción de **Acceso a la información de la cuenta** a **Desactivado**.

![Deshabilitar acceso a la cuenta](/images/Informacion_cuenta.jpg)

---
---

## Deshabilitar el acceso a la captura de pantalla (Recall)

Para deshabilitar el acceso de Windows y los programas a las capturas de pantalla que se realizan en el equipo se ingresa a:

**Configuración - Privacidad y Seguridad - Capturas de pantalla y grabación de pantalla**

y se cambia la opción de **Acceso a capturas de pantalla y grabación de pantalla** a **Desactivado**.

![Deshabilitar captura de pantallas](/images/Privacidad_capturas_pantalla.jpg)

---
---

## Deshabilitar servicios de Copilot

Para retirar todos los servicios de Microsoft Copilot, puedes ingresar al repositorio de [zoicware/RemoveWindowsAI](https://github.com/zoicware/RemoveWindowsAI), copiar el script del apartado de **Launch with UI** y pegarlo en PowerShell iniciado como administrador.

```
& ([scriptblock]::Create((irm "https://raw.githubusercontent.com/zoicware/RemoveWindowsAI/main/RemoveWindowsAi.ps1")))
```

![Ejecucion de script en PowerShell](/images/Script_copilot.jpg)

y dar clic en Apply una vez cargada la interfaz grafica con todas las opciones seleccionadas.

![Script grafico](/images/Script_copilot_UI.jpg)

Para completar el proceso es necesario reiniciar la pc.

---
---

## Quitar avisos en el explorador de archivos

Para retirar las sugerencias de copias de seguridad en OneDrive y demás productos de Microsoft se ingresa a:

**Explorador de archivos - Opciones - Ver**

y retirar el check de la casilla **Mostrar notificaciones del proveedor de sincronización**.

![Deshabilitar avisos en explorador de archivos](/images/Avisos_explorador_archivos.jpg)

---
---

## Deshabilitar el inicio rápido de Windows

Para evitar que Windows guarde los registros de lo que se esta utilizando en la sesión activa para iniciar "rapidamente" al encender el equipo se tiene que ingresar a:

**Panel de contro - Opciones de energía - Elegir la acción de los botones de inicio/apagado**

y dar clic en la opción **Cambiar la configuración no disponible actualmente** y **Desactivar** la opción **Activar inicio rápido**

![Deshabilitar inicio rápido de Windows](/images/Inicio_rapido.jpg)

Si no se hace, despues de un tiempo el sistema empieza a mostrarse lento, esto porque en el apagado de sistema, en vez de eliminar procesos que ya no estan en uso, los guarda para volver a cargarlos en el arranque.

---
---

## Menú contextual de Windows 10

Si deseas regresar al menú contextual de Windows 10 que aparece al dar clic derecho sobre algún archivo, tienes que ingresar a Simbolo de sistema como administrador y ejecutar la siguiente instrucción:

```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve   
```

![Activar Menu contextual de Windows 10](/images/menu_contextual_w10.jpg)

![Activar Menu contextual de Windows 10](/images/menu_contextual_w10_activo.jpg)

___
___

## Espero que esto te sea de utilidad y gracias por llegar hasta aquí.
