# Apache Https
### José Carlos Goméz-Lobo Ramírez

## 1 Investigación
HTTPS funciona añadiendo una capa de cifrado (TLS/SSL) sobre el protocolo HTTP, asegurando la comunicación entre un navegador y un servidor web. Utiliza un certificado digital para verificar la identidad del servidor y un sistema de claves pública y privada para cifrar y descifrar los datos, protegiendo la información de interceptaciones y manipulaciones.

Los certificados SSL/TLS se dividen principalmente en autofirmados, que son creados y firmados por el propio solicitante, y los emitidos por una Autoridad de Certificación (CA) confiable, que son validados y firmados por un tercero de confianza. 

Los autofirmados son adecuados para entornos internos de desarrollo y pruebas, ya que el cifrado es básico pero no ofrecen autenticación y generan advertencias de seguridad en navegadores externos. 

Los certificados de CA son necesarios para sitios web públicos porque proporcionan autenticación, evitan las advertencias del navegador y garantizan la identidad del sitio a los usuarios.

Para habilitar SSL/TLS en Ubuntu, el módulo principal de Apache2 que necesita es mod_ssl. Se activa ejecutando el comando sudo a2enmod ssl en la terminal, seguido del reinicio del servicio de Apache con sudo systemctl restart apache2.


## 2 Ejecución técnica:
        Instalar y verificar el estado de Apache2 en Ubuntu.
        Habilitar los módulos SSL y headers.
        Generar un certificado SSL/TLS:
            Opción A: Certificado autofirmado.
            Opción B: Certificado de Let’s Encrypt usando Certbot.
        Configurar un VirtualHost para escuchar en el puerto 443 usando HTTPS.
        Adaptar las directivas necesarias para redirección HTTP → HTTPS (opcional pero recomendado).
        Reiniciar/recargar Apache y validar la correcta implementación mediante navegador o curl.
## 3 Entrega final:
        Un documento estilo memoria en markdown con:
        Resumen de la investigación teórica.
        Descripción paso a paso de la implementación.
        Capturas de pantalla o resultados que verifiquen el acceso vía https://.
        Conclusiones finales sobre el proceso y dificultades encontradas.

## Conclusiones



## Bibliografía

[Chuletario md](https://markdownlivepreview.com/?authuser=0)
[Pdf introducción a GitHub](https://github.com/JosecarlosGlr/Practica-GitHub-MarkDown/blob/main/GitHub_%20Introducci%C3%B3n.pdf)
