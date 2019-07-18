# Paginaweb


Marco Morales
Raúl Valenzuela
José Vera




Para instalar la página proyecto es necesario tener instalada la APP xampp en la computadora.

https://www.apachefriends.org/es/download.html 
LINK DE DESCARGA.

habiendo instalado xampp, hay que descomprimir el archivo Proyecto.zip.
el archivo resultante debe ser direccionado a la carpeta htdocs dentro de la carpeta de xampp.
luego inicializar xampp e ir a phpmyadmin, crear una nueva base de datos llamada "shoppingcart"
y dentro de ella crear dos tablas nuevas con los siguientes códigos en sql:

CREATE TABLE `tblproduct` (
`id` int(8) NOT NULL AUTO_INCREMENT,
`name` varchar(255) NOT NULL,
`code` varchar(255) NOT NULL,
`image` text NOT NULL,
`description` text NOT NULL,
PRIMARY KEY (`id`),
UNIQUE KEY `product_code` (`code`)
) ENGINE=InnoDB AUTO_INCREMENT=1



CREATE TABLE `shop_session` (
`id` varchar(40) NOT NULL,
`ip_address` varchar(45) NOT NULL,
`timestamp` int(10) unsigned NOT NULL DEFAULT '0',
`data` blob NOT NULL,
PRIMARY KEY (`id`),
KEY `ci_sessions_timestamp` (`timestamp`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8


finalmente para acceder a la página, utilizar la url "localhost/Proyecto" en el buscador del browser para acceder a la página.
