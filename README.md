# Disclaimer
El propósito del siguiente proyecto es enseñar a la comunidad la configuración de un MediaCenter para Raspberry 2 y 3. El sistema propuesto ha sido configurado con el fin de facilitar la instalación de recursos multimedia, así como herramientas de streaming, video juegos y programas listos para utilizar. Mediante una serie librerías y recursos de código libre, se pretende mostrar a la comunidad la facilidad de construcción de un MediaCenter inteligente. Al mismo tiempo se recopilan los mejores proyectos para Raspberry y mostrando el trabajo de los desarrolladores para integrarlos en un sistema fácil de instalar y utilizar. **El proyecto no pretende incentivar a la piratería ni a la comercialización de contenido ilegal. Se limita al aprendizaje y utilización de recursos informáticos**.

# Introducción
CosmOS, cuyo nombre deriva de la idea "del todo", está compuesto de varios programas y addons que ofrecen al usuario "todo el entretenimiento". CosmOS está basado en [LibreELEC](http://libreelec.wiki/), un sistema que, en sí, ya ofrece herramientas de entretenimiento. Sin embargo, en esta modificación, se provee de Add-ons configurados y listos para utilizar en una Raspberry. Agradezco al proyecto por ofrecer utilidades como Add-ons de Conectividad Wifi y Bluetooh, y servicios de configuración. CosmOS, no es nada en especial, sólo una recopilación de [Software Libre](https://www.gnu.org/philosophy/free-sw.es.html) funcionando para el completo entretenimiento.

Entre los Add-ons y características que CosmOS posee, encontramos:

- Sistema basado en [LibreELEC]
- Interfaz basada en [Kodi - Media Center (18)](), lo que implica que tendrá todas sus funciones
- Add-ons de configuraciones (Conectividad Wifi, Bluetooh y servidores SMB)
- Skin [Xperience1080i]() corriendo de manera fluída
- Proveedores de información (Descargan información de películas, series de TV y música)
- Compatibilidad con [Inpustream]() para reproducción streaming con el complemento [Widevine]()
- Compatibilidad con Add-ons de video como [Netflix]() y [Amazon Prime Video]() hasta una calidad de 720p
- Add-ons de [YouTube](), [DailyMotion](), [Twitch](), [Steam Comunity](), entre otros descargables
- Script de [Spotify], cuyo objetivo es reproducir música desde un Smartphone con la aplicación
- Modo Consola (Emuladores Retro) gracias a [GameStarter]() (Utiliza RetroArch y EmulationStation)
- Compatibilidad con controles USB, Bluetooh y mandos de televisión vía HDMI con la tecnología CEC
- Software para iluminación de AmbiLight
- Reproductor de música, video, radio y TV, en diversos formatos
- Compatibilidad con múltiples servicios de IPTV
- Cast desde Smartphones ([YouTube]() y [DailyMotion]()), además de contenido local como música, videos e imágenes
- Cast desde sitios web. Facilidad de transmitir cualquier web video gracias a [Yatse]() y [Web Video Cast]()
- Transferencia de archivos mediante un cliente Samba

Algunas modificaciones de la versión oficial de [LibreELEC]() gracias a [Milhouse]()

- Inclusión de [Kodi - Media Center v18](), Leia
- Compatibilidad con Inputstream y Widevine
- Puede consultar más información sobre cambios recientes y nuevos lanzamientos en el siguiente tema [LibreELEC Testbuilds for RaspberryPi (Kodi 18.0)](https://forum.kodi.tv/showthread.php?tid=298461)

# Antes de Empezar

Para la construcción de tu propio Media Center con [CosmOS](), es necesario la obtención de los siguientes materiales:

- [Raspberry Pi 3]()
- Adaptador de corriente a 5v , 2.5A
- Tarjeta MicroSD de 8gb (mínimo) clase 10 (Garantiza la lectura y escritura de al menos 10mb/s)
- Ventilador de 5V 
- Cable HDMI para conectar a televisión 
- Caja para Raspberry (Necesaria para protección)
- Disipadores para el procesador y chip gráfico de Raspberry
- Micro Switch para reiniciar el sistema sin desconectarla de la fuente de alimentación (necesario soldar)
- Teclado, mouse y control USB (Temporales para la instalación)

# Montando el Hardware de Raspberry

# Instalación del Sistema

Para proceder a instalar el sistema, nos aseguramos de tener "vacía" nuestra tarjeta SD. Sin embargo, en caso de no estarlo, al momento de grabar nuestra imagen `CosmOS-rpi23-1.img` en nuestra tarjeta SD, el programa lo hará automáticamente. Para la comodidad del usuario, el procedimiento lo realizaremos en un ordenador con Windows. Las instrucciones en Linux, se dejarán comentadas al final de este apartado.

**Procedimiento en Windows**

1. Descargamos la siguiente utilidad [SD Imager](https://sourceforge.net/projects/sdimager/). 
2. Insertamos nuestra SD Card, y la seleccionamos dentro del programa.
3. En el apartado **Image File** seleccionamos la ruta del fichero `CosmOS-rpi23-1.img`, el cual lo descargaremos de la sección **Releases** del presente sitio. Para la última versión, presiona el siguiente enlace [last versionn]().
4. Presionamos el botón **Write** y esperamos el tiempo estimado por el programa.
5. Una vez finalizado, retiramos la SD Card del ordenador y la colocamos en nuestra **Raspberry Pi 3**.
6. Continuamos la instalación en nuestra Raspberry Pi. 

**Procedimiento en Linux**

Puedes obtener las instrucciones detalladas presionando el siguiente enlace [Installing operating system images on Linux](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md).

# Conexiones

Usaremos la herramienta de **LibreELEC** para configurar conexiones y dispositivos de CosmOS.

![](https://wiki.libreelec.tv/_media/wiki/le-settings-system.png?w=400&tok=17b2a2)

**Conectado mandos inalámbricos, BLuetooth o controles vía HDMI**

Si posees un mando compatible, es recomendado conectarlo y configurarlo para navegar por la interfaz. Es posible que necesite un teclado USB para configurar dicha entrada. 

1. En caso de poseer un televisor con la tecnología CEC, puedes controlar CosmOS con el mando del mismo dispositivo. Para saber si tu televisor posee esta característica puedes revisar el siguiente enlace [Control Kodi con mando de TV HDMI CEC](https://www.kodimania.com/viewtopic.php?t=70).

2. Para configurar un mando Bluetooth, deberás seguir las instrucciones de tu control. Con la ayuda de un teclado, diríjase a la sección **Apps** de la interfaz (ícono de engranaje). Abra presionando <kbd>ENTER</kbd> en un teclado/mando CEC. Al abrir observarás un `Addon-Splash`, para continuar presiona el botón <kbd>BACK</kbd>. Dentro de la configuración diríjase a `Bluetooth -> Nombre del dispositivo -> Pair`. Al finanizar deberás seguir los siguientes pasos para mapear el mando [Configurando Controles](https://kodi.wiki/view/HOW-TO:Configure_controllers).

3. En caso de tener un mando o gamepad wireless USB, deberás conectarlo y mapearlo siguiente las instrucciones de [Configurando Controles](https://kodi.wiki/view/HOW-TO:Configure_controllers).


**Conectado un mando desde Android/IOS/Windows**

Puedes descargar mandos a distancia disponibles para Android. En caso de tener otro sistema, deberás buscar en su respectiva **Tienda de Aplicaciones**. En esta configuración, usaremos dos aplicaciones muy populares para controlar nuestro sistema.


|Mando|Descripción|
|-----|---------------|
|Kore|Mando oficial para Kodi con todas las funciones del sistema|
|Yatse|Mando con características de transmisión de contenido local y web hacia el media-center|



El usuario podrá escoger una de las aplicaciones y para conectarla deberá seguir los respectivos pasos de cada mando.

**Conectando una red wifi o cableada**

Para poder disfrutar de todas las funciones de CosmOS, es necesario una conexión a internet. La configuración rápida de **LibreELEC** nos ayudará en el proceso.

1. En caso de poseer una conexión cableda, colócala el el puerto `LAN` de la Raspberry Pi. Listo.
2. Para conectarse a una red inalámbrica, diríjase a la sección **Apps** de la interfaz y localice el ícono del engranaje. 
3. Abra presionando <kbd>ENTER</kbd> en un teclado/mando CEC o <kbd>A</kbd> en joysticks (Previamente configurado para Inalámbrico y Bluetooth).
4. Al abrir observarás un `Addon-Splash`, para continuar presiona el botón <kbd>Return</kbd>, <kbd>BACK</kbd> o <kbd>B</kbd> dependiendo del dispositivo.
5. Dentro de la configuración diríjase a `Connections -> Nombre de la red -> Conect`.
6. Pedirá la autentificación de la red, asegúrese de escribir correctamente. En caso de errores, puede volver a intentarlo.
7. Verifique que el estado de la red se encuentre en `ready`.
8. Para evitar problemas con direcciones IP de otros dispositivos y garantizar el funcionamiento del contro remoto en Android, se ha dejado con una dirección estática (DHCP) en `192.168.1.16`. Puedes cambiarla en el mismo apartado.
9. Tu dispositivo está listo para reproducir contenido Online.
  
**Conectando un dispositivo a CosmOS mediante SAMBA para transferir archivos**

CosmOS tiene activado el cliente [SAMBA]() por defecto, así podrás transferir y compartir los archivos del sistema a cualquier dispositivo compatible. Las opciones de configuración están disponibles en la ruta `Services -> Samba`. 

|Opción|Descripción|
|-----|---------------|
|Enable Samba|Activa o desactiva el servidor Samba|
|User Samba Password Authentication|Activa o desactiva la protección del servidor con una contraseña|
|Auto-Share External Drives|Activa o desactiva la compartición de discos externos conectados al sistema|

Para transferir archivos a CosmOS se recomiendan los siguientes procedimientos.

**NOTA:** Si se ha modificado la dirección IP estática de CosmOS, deberá reemplazar los valores correspondientes. Revise el literal octavo del apartado **Conectando una red wifi o cableada**

|Plataforma|Procedimiento|
|-----|---------------|
|Windows|En el explorador de archivos ingrese la siguiente dirección `\\192.168.1.16\`|
|Sistemas basados en Ubuntu|En el explorador de archivos ingrese la siguiente dirección `smb://192.168.1.16/`|
|Android|Descarga la aplicación [ES File Explorer]() y accede en la categoría **LAN**|

Para más información de configuración ingrese al siguiente enlace [Services LibreELEC](https://wiki.libreelec.tv/libreelec_settings#tab__services). Si desea conectar a equipos con MacOS revise [MacOS Samba](https://wiki.libreelec.tv/accessing_libreelec#tab__sambasmb).

**Accediendo a Kodi mediante la Interfaz Web**

Podrás observar la reproducción, controlar el contenido y verificar estados de Kodi accediendo a la **Interfaz Web**. Dentro de un navegador web accede a la siguiente dirección:

**NOTA:** Si se ha modificado la dirección IP estática de CosmOS, deberá reemplazar los valores correspondientes. Revise el literal octavo del apartado **Conectando una red wifi o cableada**

```

http://192.168.1.16:8080

```

Para más información revise [Web Interface](https://kodi.wiki/view/Web_interface).

# Aplicaciones (Add-ons)

CosmOS viene configurado con addons de las aplicaciones más populares multiplataformas. Los addons disponibles en CosmOS se encuentran en la siguiente tabla.

|Applicación|Descripción|
|-----|---------------|
|[Netflix](https://github.com/asciidisco/plugin.video.netflix)|Disfruta del contenido de Netflix de forma nativa en Kodi|
|[Amazon Prime Video](https://github.com/Sandmann79/xbmc/tree/master/plugin.video.amazon-test)|Disfruta del contenido de Amazon Prime Video disponible en diversos países|
|[Spotify](https://github.com/kodi-community-addons/plugin.audio.spotify)|Explora reproduce y transmite contenido de Spotify|
|[Tidal](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Soundcloud](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Twitch](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[YouTube](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Vimeo](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Dailymotion](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Retro Consola](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Plex](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[CosmOS Manual](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Settings](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Crackle](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[CosmOS Cast](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|
|[Retro Consola](https://github.com/tamland/kodi-tidal)|Reproduce música en hi-fi directamente de Tidal (antes WIMP)|

**Abriendo un Addon previamente instalado**

CosmOS utiliza un **script** simple que lanza los addons con un **splash**, es decir que mostrará una breve imagen en pantalla completa de cada aplicación. Para forzar la apertura del addon presiona el botón <kbd>Return</kbd>, <kbd>BACK</kbd> o <kbd>B</kbd> dependiendo del dispositivo (si el **splash** no desaparece).

 En caso de continuar con el problema, puedes obtener soporte y/o actualizaciones creando un tema en la sección **issues**.

**Configurando Addons**
**Instalando nuevos Addons**

# Streaming y Casting

# Consola Retro

# Biblioteca de Películas, Series y Música

# Ambientación

# Expandiendo funciones

# LibreELEC Services

# Copias de Seguridad
