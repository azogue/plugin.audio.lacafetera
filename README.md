# KODI *add-on* para *[La Cafetera de Radiocable](http://www.radiocable.com)*

*Plugin* que permite reproducir cómodamente, en **[KODI](https://kodi.tv)**, los podcasts de **[La Cafetera de Radiocable](https://www.spreaker.com/user/radiocable)** disponibles a través de la API pública de la plataforma spreaker.com.

Muestra un sencillísimo menú con:
- Un acceso directo para reproducir el último episodio publicado, o bien acceder al *live-stream* cuando se está emitiendo en directo.
- Acceso a la lista de episodios existentes, presentados de 10 en 10, empezando por el más reciente.
- Búsqueda de episodios por texto contenido en el nombre.

Este `add-on` es una pequeña adaptación del ya existente para el acceso general a [spreaker.com](http://spreaker.com), realizado por [MetalKettle](https://twitter.com/metal_kettle), y disponible [aquí en zip](http://offshoregit.com/metalkettle/zips/plugin.audio.spreaker/plugin.audio.spreaker-1.0.4.zip), que, a su vez, se basa en el trabajo de [t0mm0](https://github.com/t0mm0) en el [KODI common script module](https://github.com/t0mm0/xbmc-urlresolver/tree/master/script.module.t0mm0.common).

En este caso, este `add-on` se limita a presentar únicamente los episodios de **La Cafetera**.
En mi caso, esto me resulta muy cómodo para escucharla en la tele del salón, con altavoces de verdad, además de permitirme automatizar fácilmente la reproducción de nuevos episodios en su emisión, o existentes a una hora programada. Sí, para poner de despertador el episodio del día anterior, en el hilo musical, para empezar bien el día.

Siéntete libre de modificarlo a conveniencia.

Que te aproveche, **Resistencia!**

-----

## Instalación
- Descarga el *plugin* como archivo zip a un lugar accesible desde KODI --> **[plugin.zip](https://github.com/azogue/plugin.audio.lacafetera/archive/master.zip)**
- En KODI, entra en **SISTEMA -> Ajustes -> Add-ons -> Instalar desde un archivo .zip**, y selecciona el archivo zip que has descargado.

## Uso remoto
Además del uso directo, a través de los menús de KODI, es posible lanzar la orden al add-on de reproducir inmediatamente el último episodio disponible, permitiendo automatizar fácilmente este acto desde cualquier plataforma.
Se trata de pedir a KODI que ejecute el add-on con el parámetro `mode=playlast`.
Desde la línea de comandos, por ejemplo, la orden es la siguiente:

    curl --user KODI_USER:KODI_PASSWORD --header "Content-Type: application/json" --data-binary '{"id": 1, "params": {"params": {"mode": "playlast"}, "addonid": "plugin.audio.lacafetera"}, "jsonrpc": "2.0", "method": "Addons.ExecuteAddon"}' http://KODI_IP:KODI_PORT/jsonrpc

También se le puede pedir al add-on que, simplemente, ejecute la función de KODI de *despertar*: `xbmc.executebuiltin('CECActivateSource()')`, para encender el equipo al que está conectado. El parámetro en este caso es: `mode=wakeup`.
Desde la línea de comandos sería:

    curl --user KODI_USER:KODI_PASSWORD --header "Content-Type: application/json" --data-binary '{"id": 1, "params": {"params": {"mode": "wakeup"}, "addonid": "plugin.audio.lacafetera"}, "jsonrpc": "2.0", "method": "Addons.ExecuteAddon"}' http://KODI_IP:KODI_PORT/jsonrpc

-----

## Capturas de pantalla

* Menú principal de KODI - Sección Música:
![screenshot-06-music-main.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-06-music-main.jpg)
* Reproducción de episodio:
![screenshot-01-play-full-screen.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-01-play-full-screen.jpg)
* Índice general del add-on mostrando el último episodio, la navegación de episodios, y el comando de búsqueda:
![screenshot-02-index.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-02-index.jpg)
* Navegación por episodios emitidos:
![screenshot-03-list.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-03-list.jpg)
* Diálogo de búsqueda de episodios:
![screenshot-04-search-input.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-04-search-input.jpg)
* Episodios encontrados:
![screenshot-05-search-found.jpg](https://github.com/azogue/plugin.audio.lacafetera/raw/master/resources/screenshots/screenshot-05-search-found.jpg)

- - -

#### Para terminar, plantéate que [esto merece la pena](http://www.radiocable.com/mecenas.html).
