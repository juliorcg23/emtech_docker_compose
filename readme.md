# Es importante clonar las aplicaciones de frontend y backend dentro de este directorio


# Instalar dependencias de las aplicaciones
- cd emtech-backend
- npm install

- cd emtech-frontend
- npm install

# Para levantar los contenedores de la aplicación
docker compose -f "docker-compose.yml" up -d --build

# Para hacer build de la aplicación
docker-compose run backend npm run build

# Para ejecutar las migraciones
docker exec emtech_backend npm run typeorm:run

# Para ejecutar los seeders del proyecto
docker exec emtech_backend npm run typeorm:seed