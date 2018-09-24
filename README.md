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
- Transferencia de archivos mediante un cliente Samba

Algunas modificaciones de la versión oficial de [LibreELEC]() gracias a [Milhouse]()

- Inclusión de [Kodi - Media Center]() v18, Leila
- Compatibilidad con Inputstream y Widevine

# Antes de Empezar

Para la construcción de tu propio Media Center con [CosmOS](), es necesario la obtención de los siguientes materiales:

- [Raspberry Pi 3]
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

Para proceder a instalar el sistema, nos aseguramos de tener "vacía" nuestra tarjeta SD. Ésto lo logramos mediante dos métodos disponibles para Windows y Linux. Se recomienda la utilización de Windows para este paso.

**Procedimiento en Windows**

1. Insertamos nuestra tarjeta SD en el ordenador y procedemos a descargar el siguiente programa [SD Card Formating]().
2. 

