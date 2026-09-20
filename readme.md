# App Constructora

Sistema integral de inventario y gestión de vehículos para constructora Brun&Fer.  
Incluye **backend (Node.js/Express/TypeScript)**, **frontend (React/Vite)**, **base de datos (MariaDB)** y **CI/CD con GitHub Actions**.

---

## 🚀 Tecnologías principales
- **Backend:** Node.js, Express, TypeScript, pnpm
- **Frontend:** React + Vite
- **Base de datos:** MariaDB
- **Contenedores:** Docker + Docker Compose
- **CI/CD:** GitHub Actions

---

## 📂 Estructura del proyecto
app-constructora/
├── backend/                 # API REST con Express
├── inventario-constructora/ # Frontend React + Vite
├── db/                      # Scripts SQL y documentación de la base de datos
├── docs/                    # Manuales y diagramas
└── .github/workflows/ci.yml # Pipeline CI/CD




---

## ▶️ Instalación local

### 1. Clonar el repositorio
```bash
git clone https://github.com/edgar0935/app-constructora.git
cd app-constructora

Instalar dependencias***********
pnpm install --recursive


3. Ejecutar backend
cd backend
pnpm build
pnpm start

4. Ejecutar frontend
cd inventario-constructora
pnpm dev

🐳 Ejecución con Docker
En la raíz del proyecto:
docker-compose up --build

Esto levantará:

MariaDB en localhost:3306

Backend en http://localhost:5174

Frontend en http://localhost:5173


🔐 Autenticación
El backend usa JWT para proteger rutas privadas.
Configura tu .env con:
JWT_SECRET=tu_clave_segura
