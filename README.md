# README de Traefik Proyect
## Modificaciones en docker-compose.yml
- Cambiar el subdominio del docker compose 
- Genera el usuario y clave para autenticar el dashboard traefik con el comando: 
```sh
echo $(htpasswd -nb USER "PASSWORD") | sed -e s/\\$/\\$\\$/g
```
- Busca el Proveedor de DNS, genera el Token para la API y pega el TOKEN al final del archivo
## Modificaciones en traefik.yml
- Configurar que el Dashboard sea seguro o inseguro **Con usuario y clave o no**
- Conlocar el `provider` en el Challenege DNS
## Creacion de archivo para el letsencrypt
- Crea el archivo acme.json en la carpeta letsencrypt y cambiar los permisos con el siguiente comando:
```sh
chmod 600 /letsencrypt/acme.json
```
## Subi proyecto
Termina de subir el proyecto con:
```sh
docker-compose up -d
```