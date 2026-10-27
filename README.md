# Organiza tus proyectos

Sistema del taller *Organiza tus proyectos*. Cada alumno recibe un link propio con su tablero:
**Ventas → Producción → Cobranza**.

- `/` — panel para dar de alta alumnos (pide contraseña).
- `/?t=TOKEN` — tablero de cada alumno.

Es un sitio estático (solo `index.html`, sin build) desplegado en Vercel. Los datos viven en Supabase,
en las tablas `taller_alumnos`, `taller_proyectos` y `taller_config`, cerradas con RLS; todo el acceso
pasa por funciones `taller_*` que validan el token del alumno o la contraseña del panel.
