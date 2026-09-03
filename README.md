# El horror có(s)mico — Archivo sonoro

Buscador visual del podcast, conectado en vivo a Supabase.

## Desplegar en Vercel (recomendado, gratis)

### Opción A — sin usar terminal, arrastrando la carpeta
1. Entra en https://vercel.com y crea una cuenta (puedes usar tu email o GitHub).
2. En el panel, pulsa **Add New → Project**.
3. Elige **"Deploy without Git"** (o similar) y arrastra esta carpeta completa (`horror-cosmico-app`) — o comprímela en `.zip` primero si te lo pide así.
4. Vercel detecta automáticamente que es un proyecto Vite. Deja los ajustes por defecto y pulsa **Deploy**.
5. En 1-2 minutos te da una URL pública tipo `https://horror-cosmico-app.vercel.app`.

### Opción B — con GitHub (mejor para actualizaciones futuras)
1. Crea un repositorio nuevo en GitHub y sube esta carpeta (puedes arrastrar los archivos directamente en la web de GitHub, sin usar git en terminal).
2. En Vercel: **Add New → Project → Import Git Repository**, elige ese repositorio.
3. Deploy. Cada vez que subas cambios al repositorio, Vercel lo volverá a publicar solo.

## Probarlo en tu ordenador antes de publicar (opcional)

Necesitas [Node.js](https://nodejs.org) instalado (versión 18 o superior).

```bash
npm install
npm run dev
```

Abre la URL que te indique la terminal (normalmente `http://localhost:5173`).

## Estructura

- `src/App.jsx` — el componente del buscador (el mismo que ya conoces, sin cambios).
- `src/main.jsx` — punto de entrada de React.
- Las credenciales de Supabase (`SUPABASE_URL`, `SUPABASE_ANON_KEY`) están dentro de `src/App.jsx`. Son la clave pública (`anon`/`publishable`), segura de tener en el código del cliente.
