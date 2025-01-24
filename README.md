# Todo Management API - Backend

Este repositorio contiene el backend de una aplicación para la gestión de tareas, construido con Node.js, TypeScript y MongoDB. La API permite a los usuarios autenticados crear, leer, actualizar y eliminar tareas, siguiendo las mejores prácticas en desarrollo de software.

## Tabla de Contenidos

- [Características](#características)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Requisitos Previos](#requisitos-previos)
- [Configuración](#configuración)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Comandos Disponibles](#comandos-disponibles)
- [Swagger API Documentation](#swagger-api-documentation)
- [Testing](#testing)

---

## Características

- **CRUD de Tareas:** Crear, obtener, actualizar y eliminar tareas.
- **Autenticación:** Protegido con Auth0 usando JWT.
- **Validación:** Validación de datos de entrada con Zod.
- **Documentación:** API documentada con Swagger.
- **Pruebas:** Pruebas unitarias con Jest y Supertest.
- **Configuración Modular:** Código dividido en capas (rutas, controladores, servicios, middlewares, modelos).

---

## Tecnologías Utilizadas

- **Node.js**
- **Express**
- **TypeScript**
- **MongoDB con Mongoose**
- **Auth0 para autenticación**
- **Zod para validación de esquemas**
- **Swagger para documentación**
- **Jest y Supertest para pruebas**

---

## Requisitos Previos

Asegúrate de tener instalados los siguientes programas:

- [Node.js](https://nodejs.org/) (versión recomendada: >= 18)
- [MongoDB](https://www.mongodb.com/) (local o Atlas)
- [Yarn](https://yarnpkg.com/) o [npm](https://www.npmjs.com/)

---

## Configuración

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Antonioedwardsd/devlabs-backend
   cd proyecto-backend
   ```

2. Instala las dependencias:

   ```bash
   npm install
   ```

3. Configura las variables de entorno. Crea un archivo `.env` en la raíz del proyecto basado en el siguiente ejemplo:

   ```env
   PORT=5000
   MONGO_URI=tu_mongo_uri
   AUTH0_CLIENT_ID=tu_auth0_client_id
   AUTH0_CLIENT_SECRET=tu_auth0_client_secret
   AUTH0_API_AUDIENCE=tu_auth0_audience
   AUTH0_ISSUER=tu_auth0_issuer
   NODE_ENV=development
   ```

4. Inicia la aplicación en modo desarrollo:

   ```bash
   npm run dev
   ```

5. Accede a la aplicación en `http://localhost:5000`.

---

## Estructura del Proyecto

```plaintext
backend/
├── src/
│   ├── __tests__/          # Pruebas unitarias
│   ├── config/             # Configuración de la base de datos
│   ├── controllers/        # Lógica de los endpoints
│   ├── middlewares/        # Middlewares de la aplicación
│   ├── models/             # Modelos de datos de MongoDB
│   ├── routes/             # Definición de rutas
│   ├── services/           # Servicios reutilizables
│   ├── validators/         # Validación de datos de entrada
│   └── index.ts            # Entrada principal de la API
├── swagger.yml             # Documentación de la API
├── package.json            # Dependencias y scripts
├── tsconfig.json           # Configuración de TypeScript
├── .env                    # Variables de entorno
```

---

## Comandos Disponibles

- **Desarrollo:**
  ```bash
  npm run dev
  ```
- **Compilación:**
  ```bash
  npm run build
  ```
- **Iniciar aplicación compilada:**
  ```bash
  npm run start
  ```
- **Pruebas:**
  ```bash
  npm test
  ```

---

## Swagger API Documentation

La documentación de la API está disponible en `http://localhost:5000/api-docs`.

---

## Testing

Para ejecutar las pruebas unitarias:

```bash
npm test
```

Las pruebas se encuentran en `src/__tests__/` y verifican la funcionalidad de los controladores y las rutas principales.

---
