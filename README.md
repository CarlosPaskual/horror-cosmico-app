El horror có(s)mico — Buscador visual

Interfaz de búsqueda visual para el podcast de terror **[El horror có(s)mico](https://horror-cosmico-app-vvbi.vercel.app/)**, conectada en vivo a una base de datos relacional en Supabase con más de 260 episodios catalogados.

🔗 **Demo en vivo:** [horror-cosmico-app-vvbi.vercel.app](https://horror-cosmico-app-vvbi.vercel.app/)

Qué hace

Permite explorar el archivo completo del podcast — episodios, personas citadas, temas tratados y obras referenciadas — sin depender de un buscador de texto plano, consultando directamente el esquema relacional del proyecto en tiempo real.

Stack

- **React + Vite** — interfaz y bundling
- **Supabase (PostgreSQL)** — base de datos y API en tiempo real
- **Vercel** — despliegue continuo

Proyecto relacionado

Este front-end consume el esquema definido en [`horror-cosmico-database`](enlace-cuando-lo-crees), donde está el diseño relacional completo (17 tablas: episodios, personas, temas, secciones, obras citadas y videojuegos referenciados).

Estructura


Desarrollo local

Requiere [Node.js](https://nodejs.org/) 18 o superior.

```bash
npm install
npm run dev
```

La app se sirve por defecto en `http://localhost:5173`.

Despliegue

El proyecto está configurado para desplegar en Vercel con cero configuración adicional (detecta Vite automáticamente). Cualquier fork o clon puede desplegarse conectando el repo en [vercel.com](https://vercel.com) → *Add New → Project → Import Git Repository*.

Notas de seguridad

Las credenciales de Supabase (`SUPABASE_URL`, `SUPABASE_ANON_KEY`) están en `src/App.jsx`. Son la clave pública (`anon`/`publishable`) de Supabase, diseñada para exponerse en código de cliente — el acceso real a los datos se controla vía Row Level Security en la base de datos, no ocultando esta clave.
