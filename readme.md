# Es importante clonar las aplicaciones de frontend y backend dentro de este directorio

# Dependencias

Para ejecutar esta aplicación se debe contar con las siguientes dependencias instaladas.

- Docker
- docker-compose

# Habilitar los archivos de variables de ambiente de cada parte de la aplicación

- Para el backend renombrar el .env.example a .env
- Para el frontend renombrar el .env.local.example a .env.local

# Para levantar los contenedores de la aplicación
docker compose -f "docker-compose.yml" up -d --build

# Para hacer build de la aplicación
docker-compose run backend npm run build

# Para ejecutar las migraciones
docker exec emtech_backend npm run typeorm:run

# Para ejecutar los seeders del proyecto
docker exec emtech_backend npm run typeorm:seed