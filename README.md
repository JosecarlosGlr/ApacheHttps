# Apache Https
### José Carlos Goméz-Lobo Ramírez

## 1 Investigación
HTTPS funciona añadiendo una capa de cifrado (TLS/SSL) sobre el protocolo HTTP, asegurando la comunicación entre un navegador y un servidor web. Utiliza un certificado digital para verificar la identidad del servidor y un sistema de claves pública y privada para cifrar y descifrar los datos, protegiendo la información de interceptaciones y manipulaciones.

Los certificados SSL/TLS se dividen principalmente en autofirmados, que son creados y firmados por el propio solicitante, y los emitidos por una Autoridad de Certificación (CA) confiable, que son validados y firmados por un tercero de confianza. 

Los autofirmados son adecuados para entornos internos de desarrollo y pruebas, ya que el cifrado es básico pero no ofrecen autenticación y generan advertencias de seguridad en navegadores externos. 

Los certificados de CA son necesarios para sitios web públicos porque proporcionan autenticación, evitan las advertencias del navegador y garantizan la identidad del sitio a los usuarios.

Para habilitar SSL/TLS en Ubuntu, el módulo principal de Apache2 que necesita es mod_ssl. Se activa ejecutando el comando sudo a2enmod ssl en la terminal, seguido del reinicio del servicio de Apache con sudo systemctl restart apache2.


## 2 Ejecución técnica:

![Verificación estado apache2](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/1.png)  
Primero verificamos el estado de Apache2


![Habilitar los módulos SSL y headers](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/2.png)  
Habilito los módulos SSL y headers y recargo apache


![Genero certidicado ssl/tls](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/3.png)
![Genero certidicado ssl/tls](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/4.png)  

Genero un certificado SSL/TLS:
Certificado autofirmado.

![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/5.png)
![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/6.png)  
Configuro un VirtualHost para escuchar en el puerto 443 usando HTTPS.

![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/7.png)
![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/8.png)  
Adapto las directivas necesarias para redirección HTTP → HTTPS.

![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/9.png)   
Reinicio apache para comprobar que funciona lo que he hecho
![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/12.png)
![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/13.png)
![Configuro un VirtualHost](https://github.com/JosecarlosGlr/ApacheHttps/blob/main/14.png)  
Lo que ocurre cuando ahora entro a https://gci.example y http://gci.example

## Conclusiones



## Bibliografía
[¿Que es el protocolo https](https://www.cloudflare.com/es-es/learning/ssl/what-is-https/)  
[Tipos de certificados SSL/TLS](https://kinsta.com/es/blog/tls-vs-ssl/)  


## Dificultades encontradas

