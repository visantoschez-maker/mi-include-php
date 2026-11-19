# Ejercicio de Include
### Víctor Santos Sánchez - 2ºASIR

Este proyecto demuestra cómo dividir una página web en varias partes reutilizables utilizando la función include de PHP dentro de un entorno controlado con Docker. El objetivo principal es evitar repetir el mismo código HTML en diferentes páginas y facilitar el mantenimiento del sitio web.

## El entorno de ejecución y depuración

El archivo de configuración de Docker levanta un servidor web con PHP integrado y conecta nuestra carpeta local llamada app directamente con el interior del contenedor. De esta manera, cualquier cambio que guardemos en nuestro editor se refleja al instante al recargar el navegador en el puerto 8080. Además, el archivo de configuración de Visual Studio Code prepara el terreno para que Xdebug pueda conectarse y permitirnos revisar el código paso a paso si ocurre algún error.

## El flujo del archivo principal

Cuando abrimos la página en el navegador, el servidor ejecuta el archivo index.php como punto de partida. Lo primero que hace este archivo es crear una variable llamada titulo y asignarle un texto descriptivo. Inmediatamente después, utiliza la instrucción include para traer el contenido del archivo encabezado.php y pegarlo justo en ese lugar antes de continuar leyendo el resto del documento.

## La integración del encabezado y el pie de página

Al insertarse el archivo encabezado.php dentro del archivo principal, este hereda automáticamente todas las variables creadas anteriormente. Gracias a esto, la etiqueta title del documento HTML puede imprimir el valor de la variable titulo sin problemas. Posteriormente, el archivo principal muestra un encabezado grande con ese mismo texto y vuelve a utilizar la instrucción include para insertar el contenido de pie.html, logrando así ensamblar una página web completa a partir de tres archivos independientes.