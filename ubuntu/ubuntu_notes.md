# Mi experiencia con Ubuntu  

Explicaré algunos puntos desde que volví a iniciar con Ubuntu. Digo volví a iniciar porque perdí todos mis archivos no por culpa de Ubuntu, sino por no guardar una copia de seguridad antes de transferir mis archivos por USB.<br>
Trataré de escribir de la forma más entendible el proceso que fui siguiendo para configurar mi computadora. Asimismo, iré explicando lo que aprendí de Ubuntu a medida que personalizo mi área de trabajo. 

Realizaré las anotaciones por fecha, trataré de citar todas las fuentes posibles. Estoy usando Ubuntu 24.04 LTS

## 23/Junio/2024

### Visual Studio Code

Realicé la instalación desde la tienda de aplicaciones Snap. Tuve dificultades para iniciar la aplicación, se detenía cada vez que la abría y tenía que forzar cerrarla. Intenté la instalación con el paquete para Debian que ofrece VS Code en su web con el comando `sudo apt install ./<paquete>.deb` y tuve los mismos resultados. Reinicié mi máquina para que la aplicación pueda ejecutarse correctamente.

Luego de realizar la instalación seguí los pasos básicos iniciales que me inclucaba la guía de VS Code. Instalé las extensiones para Java, Python y Markdown.

Me hacía falta una extensión de previsualización de Markdown, por lo que instalé `Markdown Preview Enhanced`. En las notas de VS Code escribo los comandos que voy aprendiendo.


## 24/Junio/2024

### Escritorio

Para personalizar mi escritorio con las extensiones que ofrece `GNOME` primeramente pensé en instalar el navegador Brave. Lo instalé en un inicio desde la Snap Store, sin embargo, se dificultó el proceso. Pese a instalar el conector al navegador que se indica en la wiki de Gnome[^1] y la extensión en el navegador[^2], me aparecía el siguiente error:

> Aunque la extensión de integración con GNOME Shell está en ejecución, no se ha detectado el conector del equipo. Consulte la documentación para obtener instrucciones sobre cómo instalar el conector.

Leyendo alguna información de internet[^3] comprendí que puede ser un error de la tienda de Snap. Por lo tanto, decidí instalar Brave mediante `apt` siguiendo las instrucciones de instalación de la página[^4]. Posteriormente, instalé la extensión nuevamente[^2] y ¡sorpresa! o no, el error ya no aparecía. Sin embargo, decidí intentarlo con Firefox, busqué la extensión[^5], la añadí y el error había desaparecido. 

> Con el objetivo de apoyar la no monopolización de los navegadores[^6][^7], utilizaré Firefox

Pero... un momento, el error había desaparecido, sin embargo, las extensiones aún no se pueden instalar. Buscando soluciones nuevamente en internet, encontré este hilo de reddit[^8] que describe perfectamente el problema que estaba pasando. Fue donde me enteré de la existencia de Gnome Extensions Manager[^9]. Instalé la aplicación con el comando `sudo apt-get install gnome-shell-extension-manager` y me liberé de problemas, ya que de la misma aplicación es posible administrar e instalar extensiones.

# 25/Junio/2024

### Escritorio

Explorando en internet y en el gestor de extensiones, me encontré con varias que me parecieron interesantes y útiles. Estas son las extensiones que instalé:
- Gnome Clipboard History[^10]: Guarda una historia de los elementos copiados en el portapapeles. Es posible eliminar los elementos que ya no consideres necesarios, asimismo 
- Dash to Dock[^11]: Ubuntu tiene su propia extensión para el dock, sin embargo, esta me gusta más estéticamente.
- GSConnect[^12]: Para conectar el móvil al sistema. Simula un touchpad en el celular, permite transferir archivos, permite ejecutar comandos desde el celular, entro otras funcionalidades.
- Just Perfection[^13]: Para personalizar el escritorio de GNOME, cambiar comportamiento o eliminar elementos de la interfaz.
- Gnome Open Weather[^14]: Habilita una opción en la barra de tareas para ver datos acerca del clima.
- Place Status Indicatpr[^15]: Permite una navegación rápida entre directorios desde la barra de tareas. 
- Simple Net Speed[^16]: Muestra la velocidad de internet en la barra de tareas.


[^1]: Especificación de la instalación del [conector para Ubuntu](https://gnome.pages.gitlab.gnome.org/gnome-browser-integration/pages/installation-guide.html#ubuntu_linux)
[^2]: Extensión para [navegadores basados en Chromium](https://chromewebstore.google.com/detail/integraci%C3%B3n-con-gnome-she/gphhapmejobijbbhgpjhcjognlahblep?hl=es)
[^3]: Chromium con snap presenta [errores que ya son conocidos](https://www.enmimaquinafunciona.com/pregunta/163717/aunque-la-extension-de-integracion-de-gnome-shell-se-esta-ejecutando-no-se-detecta-el-conector-nativo-del-host)
[^4]: Instalar [Brave para linux](https://brave.com/linux/)
[^5]: Extensión para [navegadores basados en mozilla](https://addons.mozilla.org/es/firefox/addon/gnome-shell-integration/?utm_source=|addons.mozilla.org&utm_medium=referral&utm_content=search)
[^6]: [Mozilla vs Chromium](https://www.threads.net/@midu.dev/post/CubeQI5gajh?hl=es)
[^7]: [El monopolio de Chrome](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.lavanguardia.com/tecnologia/20190529/462555222714/google-chrome-monopolio.html&ved=2ahUKEwj_h8Tbt_WGAxVvBLkGHa5kCn4QFnoECB4QAQ&usg=AOvVaw15I32fwnC36MflPqEV0WX3)
[^8]: [No se pueden instalar las extensiones - Gnome](https://www.reddit.com/r/gnome/comments/1clnms1/cant_install_extensions/)
[^9]: [Gnome Extensions Manager](https://mattjakeman.com/apps/extension-manager)
[^10]: [Gnome Clipboard History](https://github.com/SUPERCILEX/gnome-clipboard-history)
[^11]: [Dash to Dock](https://micheleg.github.io/dash-to-dock/)
[^12]: [GSConnect](https://github.com/GSConnect/gnome-shell-extension-gsconnect/wiki)
[^13]: [Just Perfection](https://gitlab.gnome.org/jrahmatzadeh/just-perfection)
[^14]: [Gnome Open Weather](https://github.com/penguin-teal/gnome-openweather)
[^15]: [Place Status Indicator](https://extensions.gnome.org/extension/8/places-status-indicator/)
[^16]: [Simple Net Speed](https://github.com/biji/simplenetspeed)