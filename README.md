# React-Docker-Dev-Env
React + Node Express + mysql development environment

## NOTA: AUN ANDO PROBANDO COMO FUNCIONA

# Notas Importantes
- Necesitas crear una carpeta llamada ```mysql_mount``` dentro del directorio raiz para que el contenedor de mysql pueda guardar los módelos.

# Como se usa?
Literal copia los archivos de la react app en ```frontent``` y el backend en ```./backend```. Necesitas un ```ṕackage.json``` en cada uno para se puedan construir los contenedores. 

# Comandos Utiles:
```
docker exec database /usr/bin/mysqldump -u root --password=cisco stuff > backup.sql # exportar la base de datos a un archivo
docker exec -it database bash # crear una terminal. Sustituir "database" por cualquiera de los servicios en docker-compose.yaml
docker-compose up 
docker-compose down

```