# 👠 Pisadas Digitales - E-commerce 

> Plataforma de comercio electrónico especializada en calzado y accesorios de moda, con panel administrativo en desarrollo para gestión de inventario. Proyecto académico convertido en un caso de estudio completo del ciclo de vida del desarrollo de software.

---


## 📖 Descripción

**Pisadas Digitales** es una plataforma de comercio electrónico de moda que surge como proyecto de plan de negocio universitario. Representa una necesidad real del mercado: permitir que pequeños emprendedores de moda puedan gestionar su inventario y vender productos en línea sin necesidad de conocimientos técnicos avanzados.


## ✨ Características

### Para Clientes
- 🛍️ **Catálogo de Productos** - Visualización intuitiva de calzado y accesorios
- 🔍 **Búsqueda y Filtros Avanzados** - Filtrar por género, precio, color y tamaño
- 📱 **Diseño Responsive** - Experiencia optimizada en móvil, tablet y desktop
- 📦 **Historial de Pedidos** - Seguimiento de compras realizadas
- 🛒 **Carrito Persistente** - Datos almacenados en LocalStorage
- 🛒 **Carrito ** - conecta al whatsApp empresa

### Para Administradores
##este modulo se encuentra en desarrollo.
- 👤 **Autenticación Segura** - Sistema de login y registro con JWT
- - 🔐 **Recuperación de Contraseña** - Sistema seguro con email verification
- 📊 **Panel de Control** - Dashboard con estadísticas clave
- ➕ **Gestión de Productos** - CRUD completo (crear, leer, actualizar, eliminar)
- 👥 **Gestión de Usuarios** - Control de acceso y permisos
- ⚙️ **Configuración General** - Personalización de la plataforma
- 📊 **Reportes** - Análisis de ventas y comportamiento de usuarios (en desarrollo)
- 🔔 **Notificaciones** - Alertas de nuevos pedidos y actividad

---

## 🚀 Demo en Vivo

La plataforma está desplegada y lista para explorar:

| Componente | URL |
|-----------|-----|
| **Tienda Principal** | [pisadas-digitales-vanessa-osorio.netlify.app](https://pisadas-digitales-vanessa-osorio.netlify.app/) |
| **Panel de Admin** | [/admin](https://pisadas-digitales-vanessa-osorio.netlify.app/admin) |
| **Login** | [/auth/login](https://pisadas-digitales-vanessa-osorio.netlify.app/auth/login) |

### Credenciales de Prueba

```

Email: test@pisadas.com
Contraseña: test123
```

---

## 🛠️ Stack Tecnológico

### Frontend
```
✓ React 19        - Librería UI moderna
✓ TypeScript      - Tipado estático
✓ React Router    - Navegación declarativa
✓ React Query     - Manejo de estado servidor
✓ Axios           - Cliente HTTP
✓ React Hook Form - Gestión de formularios
✓ Vite            - Build tool ultra-rápido
✓ ESLint          - Linting y calidad de código
```

### Backend
```
✓ Node.js 22+     - Runtime JavaScript server-side
✓ Express 5       - Framework web minimalista
✓ TypeScript      - Tipado estático
✓ SQLite 3        - Base de datos embebida
✓ JWT             - Autenticación stateless
✓ bcryptjs        - Hashing de contraseñas
✓ CORS            - Control de origen cruzado
✓ Nodemon         - Auto-reload en desarrollo
```

### DevOps & Despliegue
```
✓ Git             - Control de versiones
✓ Netlify         - Hosting frontend (CI/CD)
✓ Render          - Hosting backend
✓ GitHub          - Repositorio y colaboración
```

---


## 💻 Guía de Uso

### Para Clientes

1. **Explora la Tienda**
   - Navega a la sección de productos
   - Filtra por género, precio, color y tamaño
   - Visualiza detalles del producto

2. **Registrarse**
   - Accede a [/auth/register](https://pisadas-digitales-vanessa-osorio.netlify.app/auth/register)
   - Completa el formulario con tus datos
   - Recibe un email de confirmación

3. **Comprar Productos**
   - Agrega productos al carrito
   - Procede a checkout
   - Realiza el pago (integración en progreso)

4. **Recuperar Contraseña**
   - Si olvidas tu contraseña, ve a [/auth/forgot-password](https://pisadas-digitales-vanessa-osorio.netlify.app/auth/forgot-password)
   - Recibe un email con instrucciones
   - Establece una nueva contraseña

### Para Administradores

1. **Acceder al Panel**
   - Inicia sesión con credenciales de admin
   - Serás redirigido automáticamente al dashboard
 Modulo administrativo en proceso de desarrollo. 

---

## 🏗️ Arquitectura

### Arquitectura General

```
┌─────────────────────────────────────────────────┐
│         Frontend (React + Vite)                 │
│  - SPA con React Router                         │
│  - Estado con React Query                       │
│  - Hosted en Netlify                            │
└──────────────┬──────────────────────────────────┘
               │ HTTP/REST API
               ├─ CORS enabled
               └─ JWT Authentication
┌──────────────▼──────────────────────────────────┐
│       Backend (Express + Node.js)               │
│  - RESTful API con TypeScript                   │
│  - SQLite para persistencia                     │
│  - Hosted en Render                             │
└─────────────────────────────────────────────────┘
```

### Flujo de Autenticación

```
1. Usuario ingresa credenciales
   ↓
2. Backend valida en BD (bcryptjs)
   ↓
3. Backend genera JWT token
   ↓
4. Frontend almacena token en localStorage
   ↓
5. Solicitudes posteriores incluyen Authorization header
   ↓
6. Backend valida JWT en cada request
```

### Capas de la Aplicación

#### Frontend
- **Pages**: Componentes de páginas principales
- **Components**: Componentes reutilizables
- **Hooks**: Lógica personalizada
- **Services/API**: Integración con backend
- **Context**: Estado global (carrito, autenticación)
- **Utils**: Funciones auxiliares

#### Backend
- **Routes**: Definición de endpoints
- **Controllers**: Lógica de negocio
- **Services**: Servicios especializados
- **Middleware**: Validación y autenticación
- **Config**: Configuración (CORS, BD, etc.)
- **DB**: Schema y queries SQLite

---

## 📂 Estructura del Proyecto

```
pisadas-digitales/
├── Frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── auth/          (Login, Register, ResetPassword)
│   │   │   ├── admin/         (Dashboard, Productos, Usuarios)
│   │   │   └── store/         (Tienda, Productos, Blog)
│   │   ├── components/        (Componentes reutilizables)
│   │   ├── api/               (Servicios HTTP)
│   │   ├── context/           (Context API)
│   │   ├── hooks/             (Custom hooks)
│   │   ├── utils/             (Funciones auxiliares)
│   │   ├── router/            (Configuración de rutas)
│   │   └── App.tsx
│   ├── public/                (Assets estáticos)
│   ├── .env                   (Variables de entorno)
│   ├── vite.config.ts
│   ├── tsconfig.json
│   └── package.json
│
├── backend/
│   ├── src/
│   │   ├── router.ts          (Rutas principales)
│   │   ├── server.ts          (Configuración Express)
│   │   ├── db.ts              (Inicialización SQLite)
│   │   ├── auth/
│   │   │   ├── authRouter.ts
│   │   │   ├── authController.ts
│   │   │   ├── jwt.ts
│   │   │   └── passwordResetController.ts
│   │   ├── config/
│   │   │   └── cors.ts
│   │   ├── middleware/
│   │   │   └── validation.ts
│   │   ├── services/
│   │   │   └── emailService.ts
│   │   └── index.ts
│   ├── .env                   (Variables de entorno)
│   ├── tsconfig.json
│   └── package.json
│
├── README.md(Este archivo)
├──

---

## 🚀 Despliegue

## actualmente:
- ✓backend: onrender
- ✓ frontend: netlify
- para demostración Demo, a futuro se va a desplegar AWS


## 🎓 Conocimientos Demostrados

Este proyecto demuestra experiencia en todo el ciclo de vida del desarrollo de software:

### ✅ Frontend Development
- ✓ React 19 con TypeScript
- ✓ Arquitectura escalable de componentes
- ✓ Manejo avanzado de estado (React Query, Context API)
- ✓ Formularios complejos (React Hook Form)
- ✓ Routing dinámico (React Router v7)
- ✓ Responsive design y mobile-first
- ✓ Integración con APIs RESTful
- ✓ Linting y control de calidad (ESLint)

### ✅ Backend Development
- ✓ Node.js y Express.js
- ✓ TypeScript para backend
- ✓ Autenticación JWT
- ✓ Encriptación de contraseñas (bcryptjs)
- ✓ Validación de datos
- ✓ CORS y seguridad web
- ✓ Manejo de emails (Resend)
- ✓ Base de datos relacional (SQLite)

### ✅ DevOps & Infraestructura
- ✓ CI/CD (Netlify & Render)
- ✓ Control de versiones (Git)
- ✓ Variables de entorno y configuración
- ✓ Despliegue en la nube
- ✓ Monitoreo básico y logs

### ✅ Metodología & Procesos
- ✓ Desarrollo iterativo
- ✓ Planificación de features
- ✓ Versionamiento semántico
- ✓ Documentación técnica completa
- ✓ Gestión de proyecto desde cero

### ✅ Soft Skills
- ✓ Resolución de problemas
- ✓ Pensamiento crítico
- ✓ Comunicación técnica
- ✓ Planificación y organización
- ✓ Aprendizaje continuo

---


## 👤 Autor

**Vanessa Osorio Ortiz**

- 📧 Email: vanessaosorio.dev@gmail.com
- 🔗 GitHub: [Tu GitHub](https://github.com/tu-usuario)

**Sobre mí:** Desarrolladora Full Stack apasionada por crear soluciones digitales innovadoras. Este proyecto representa mi compromiso con la excelencia en desarrollo y mi capacidad para conceptualizar, diseñar e implementar aplicaciones web complejas desde cero.

---



