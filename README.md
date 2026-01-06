# Adoptanet

Adoptanet es un MVP de una aplicación web orientada a la gestión de animales en adopción. Permite a organizaciones y personas publicar anuncios de adopción y recibir solicitudes de interesados, centralizando la información para facilitar el contacto y el proceso de adopción.

## Características

- **Catálogo de Animales:** Explora perfiles detallados de perritos, gatitos y otros animales en busca de un hogar.
- **Publicación Sencilla:** Si eres un rescatista o una organización, puedes registrarte y publicar fácilmente los perfiles de los animales a tu cuidado.
- **Proceso de Solicitud:** ¿Encontraste a tu futuro mejor amigo? Envía una solicitud de adopción directamente desde la plataforma.
- **Gestión para Publicantes:** Los publicantes pueden revisar y gestionar las solicitudes recibidas para contactar a los adoptantes.

## Tecnologías Utilizadas

- **Frontend:** React, TypeScript, Vite, Shadcn/UI
- **Backend:** Python con FastAPI
- **Base de Datos:** MariaDB
- **Despliegue:** Docker y Docker Compose

## Despliegue y Ejecución

Para levantar el proyecto en tu entorno local, solo necesitas tener Docker y Docker Compose instalados. El proceso es muy sencillo:

### 1. Clona este repositorio

Si aún no lo has hecho, clona el proyecto en tu máquina.

### 2. Crea el archivo de entorno

El proyecto utiliza un archivo `.env` para gestionar las variables de entorno necesarias para la base de datos y la comunicación entre el frontend y el backend.

Crea un archivo llamado `.env` en el directorio raíz del proyecto con el siguiente contenido:

```bash
# Variables para la Base de Datos (MariaDB)
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=adoptanet
MYSQL_USER=user
MYSQL_PASSWORD=password
DATABASE_URL=mysql+pymysql://user:password@db/adoptanet

# URL para la API (usada por el Frontend)
VITE_API_URL=http://localhost:8000
```

### 3. Levanta los contenedores

Una vez que tengas el archivo `.env` listo, abre una terminal en la raíz del proyecto y ejecuta el siguiente comando:

```bash
cd despliegue && docker compose up 
```

Este comando construirá las imágenes de Docker para el frontend y el backend, iniciará los contenedores y los dejará corriendo en para que sea en segundo plano agregar la flag (`-d`).

¡Y listo!
- El **frontend** estará accesible en `http://localhost:5173`
- El **backend** estará operativo en `http://localhost:8000`

## Cómo detener la aplicación

Para detener todos los servicios, puedes usar el siguiente comando en la terminal:

```bash
docker compose down
```




