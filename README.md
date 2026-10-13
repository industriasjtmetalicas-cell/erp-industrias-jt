# ERP Industrias Metálicas J&T S.A.S.
Base React + TypeScript + Supabase para desplegar separada de la aplicación anterior. No modifica ni elimina la base de datos.

## Requisitos
Node.js 20+ y acceso al proyecto Supabase.

## Ejecutar
1. Copiar `.env.example` a `.env.local`.
2. Completar `VITE_SUPABASE_URL` y `VITE_SUPABASE_ANON_KEY` con la URL del proyecto y la clave **publishable**. Nunca usar `service_role` ni una clave secreta en frontend.
3. Ejecutar `npm install` y `npm run dev`.
4. Para compilar: `npm run build`.

## Seguridad
Cliente configurado para el esquema PostgreSQL `app`; Supabase Auth; rol validado desde `app.usuarios` y `app.roles`; no hay selector de roles. RLS sigue siendo obligatoria y es la autoridad de acceso real.
Esta entrega es una primera base: Dashboard conectado a conteos reales, CRUD de clientes y proveedores, navegación y pantallas pendientes explícitas. No se declara funcional un módulo pendiente ni se usan datos ficticios.
