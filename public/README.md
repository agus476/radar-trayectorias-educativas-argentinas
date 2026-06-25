# Demo HTML estática

Esta carpeta está preparada para publicar una versión estática del dashboard principal como HTML pre-renderizado.

## Qué es la demo

La demo esperada es `public/index.html`, generado desde `abandono_escolar_argentina_dashboard.ipynb` **después de ejecutar el notebook con credenciales válidas de PostgreSQL/Supabase**.

La demo HTML:

- no ejecuta Python;
- no consulta PostgreSQL/Supabase en tiempo real;
- no requiere variables de entorno;
- no reemplaza al notebook original;
- sirve para que evaluadores o recruiters revisen el resultado visual desde un link público.

## Cómo generar `public/index.html`

Desde la raíz del repositorio, con el notebook ya ejecutado y con sus outputs guardados:

```bash
jupyter nbconvert --to html abandono_escolar_argentina_dashboard.ipynb --output-dir public --output index.html
```

Opcionalmente, para ocultar las celdas de código y dejar una salida más orientada a presentación:

```bash
jupyter nbconvert --to html abandono_escolar_argentina_dashboard.ipynb --output-dir public --output index.html --no-input
```

## Publicación estática

### GitHub Pages

1. Generar `public/index.html`.
2. Subir los cambios al repositorio.
3. Configurar GitHub Pages para publicar desde la carpeta `public/` o copiar el HTML a la rama/ruta configurada para Pages.

### Vercel

1. Generar `public/index.html`.
2. Importar el repositorio en Vercel.
3. Usar configuración estática sin framework.
4. Publicar la carpeta `public/` como salida estática.

## Seguridad

Antes de publicar, revisar que el HTML no contenga secretos:

```bash
rg -n "password|DB_PASSWORD|postgresql://|supabase|apikey|secret|token" public
```

Las menciones documentales a nombres de variables pueden ser válidas, pero no debe aparecer ninguna credencial real, token ni cadena de conexión completa.
