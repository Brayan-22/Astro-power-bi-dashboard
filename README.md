# Power BI Dashboard - Astro App

SPA minimalista en Astro para mostrar un informe de Power BI embebido con diseño sobrio y responsivo.

## Características

- ⚡️ Astro con output estático para máximo rendimiento
- 🎨 Diseño limpio y responsivo
- 📱 Totalmente adaptable a móviles
- 🚀 Optimizado para Vercel
- 🔄 Controles para recargar, abrir en nueva pestaña y pantalla completa

## Estructura del Proyecto

```
power-bi-app/
├── src/
│   ├── components/
│   │   ├── Header.astro        # Cabecera con logo y controles
│   │   └── PowerBIEmbed.astro  # Iframe de Power BI con lógica
│   ├── layouts/
│   │   └── Layout.astro        # Layout principal con estilos globales
│   └── pages/
│       └── index.astro         # Página principal
├── astro.config.mjs            # Configuración de Astro + Vercel
└── package.json
```

## Desarrollo Local

```bash
# Instalar dependencias (si no lo hiciste ya)
npm install

# Iniciar servidor de desarrollo
npm run dev

# El servidor estará disponible en http://localhost:4321
```

## Build para Producción

```bash
# Generar build estático optimizado
npm run build

# Preview del build
npm run preview
```

## Despliegue en Vercel

### Opción 1: Despliegue automático con GitHub

1. Sube el proyecto a un repositorio de GitHub
2. Ve a [vercel.com](https://vercel.com) y haz login
3. Click en "Add New Project"
4. Importa tu repositorio de GitHub
5. Vercel detectará automáticamente que es un proyecto Astro
6. Click en "Deploy"

### Opción 2: Despliegue con Vercel CLI

```bash
# Instalar Vercel CLI globalmente
npm i -g vercel

# Desde la raíz del proyecto
vercel

# Para producción
vercel --prod
```

## Personalización

### Cambiar la URL del informe de Power BI

Edita `src/pages/index.astro` y modifica la constante `reportUrl`:

```astro
const reportUrl = "TU_URL_DE_POWER_BI_AQUI";
```

### Modificar estilos

Los estilos están organizados por componente:
- Estilos globales: `src/layouts/Layout.astro`
- Cabecera: `src/components/Header.astro`
- Área de embed: `src/components/PowerBIEmbed.astro`

### Variables CSS

Las variables CSS están definidas en `Layout.astro`:

```css
:root{
  --bg:#f5f7f8;
  --card:#ffffff;
  --muted:#6b7280;
  --accent:#0f172a;
  --shadow: 0 6px 18px rgba(15,23,42,0.08);
  --radius:12px;
  --maxw:1200px;
}
```

## Scripts Disponibles

- `npm run dev` - Inicia el servidor de desarrollo
- `npm run build` - Construye la aplicación para producción
- `npm run preview` - Previsualiza el build de producción localmente

## Tecnologías

- [Astro](https://astro.build) - Framework web moderno
- [Vercel](https://vercel.com) - Plataforma de hosting
- Power BI - Plataforma de visualización de datos de Microsoft
