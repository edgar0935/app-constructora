# 📖 Manual de Instalación — App Constructora

Este documento describe los pasos necesarios para instalar y ejecutar el sistema **App Constructora** en un entorno local o con contenedores Docker.

---

## 🔧 Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- [Node.js](https://nodejs.org/) v18 o superior
- [pnpm](https://pnpm.io/) como gestor de paquetes
- [MariaDB](https://mariadb.org/) (si deseas correr la base de datos localmente)
- [Docker](https://www.docker.com/) y [Docker Compose](https://docs.docker.com/compose/) (opcional, para ejecución en contenedores)
- Git

---

## ▶️ Instalación local

### 1. Clonar el repositorio
```bash
git clone https://github.com/edgar0935/app-constructora.git
cd app-constructora

2. Instalar dependencias
pnpm install --recursive

3. Configurar la base de datos
Crea una base de datos en MariaDB llamada constructora_app.

Importa el archivo SQL ubicado en db/dump.sql (si existe).

Configura las variables de entorno en backend/.env:
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=tu_password
DB_NAME=constructora
JWT_SECRET=tu_clave_segura

4. Ejecutar el backend
cd backend
pnpm build
pnpm start
El backend quedará disponible en http://localhost:5174.

5. Ejecutar el frontend
cd inventario-constructora
pnpm dev
El frontend quedará disponible en http://localhost:5173.

🐳 Instalación con Docker
1. Levantar servicios
En la raíz del proyecto:
docker-compose up --build

Esto levantará:

MariaDB en localhost:3306

Backend en http://localhost:5174

Frontend en http://localhost:5173

2. Variables de entorno
Configura las variables en docker-compose.yml o en archivos .env según sea necesario.