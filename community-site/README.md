# Sitio Web de la Comunidad Boorie

Este directorio contiene el código fuente del sitio web de la comunidad Boorie.

## 🌐 Descripción General

El sitio web de la comunidad sirve como punto central para:
- Información sobre el proyecto
- Documentación y recursos
- Blog y noticias
- Foro de la comunidad
- Casos de éxito
- Portal de contribuyentes

## 🏗️ Arquitectura Técnica

### Stack Tecnológico
- **Frontend**: Next.js 14 + TypeScript
- **Styling**: Tailwind CSS
- **Backend**: FastAPI (compartido con API principal)
- **Base de Datos**: PostgreSQL
- **CMS**: Strapi (headless CMS)
- **Hosting**: Vercel + AWS

### Estructura de Directorios

```
community-site/
├── src/                    # Código fuente
│   ├── app/               # App Router de Next.js
│   ├── components/        # Componentes React
│   ├── lib/              # Utilidades y helpers
│   ├── styles/           # Estilos globales
│   └── types/            # TypeScript types
├── content/               # Contenido estático
│   ├── blog/             # Posts del blog
│   ├── docs/             # Documentación
│   ├── case-studies/     # Casos de éxito
│   └── tutorials/        # Tutoriales
├── assets/               # Recursos estáticos
│   ├── images/          # Imágenes y gráficos
│   ├── videos/          # Videos tutoriales
│   └── downloads/       # Recursos descargables
├── public/              # Archivos públicos
└── tests/               # Tests del sitio
```

## 📄 Páginas Principales

### 1. **Home** (`/`)
- Hero section con llamada a la acción
- Características principales
- Casos de éxito destacados
- Últimas noticias del blog
- Testimonios

### 2. **Sobre Nosotros** (`/about`)
- Misión y visión
- Historia del proyecto
- Equipo y contribuyentes
- Socios y patrocinadores
- Hoja de ruta

### 3. **Características** (`/features`)
- Lista detallada de funcionalidades
- Comparación con otras soluciones
- Demos interactivas
- Videos explicativos

### 4. **Documentación** (`/docs`)
- Guía de inicio rápido
- Documentación técnica
- API reference
- Tutoriales
- FAQ

### 5. **Comunidad** (`/community`)
- Cómo contribuir
- Código de conducta
- Eventos y meetups
- Discord/Foro
- Programa de embajadores

### 6. **Blog** (`/blog`)
- Artículos técnicos
- Casos de uso
- Actualizaciones del proyecto
- Tutoriales
- Entrevistas

### 7. **Recursos** (`/resources`)
- Downloads
- Papers académicos
- Presentaciones
- Webinars grabados
- Herramientas

### 8. **Soporte** (`/support`)
- Centro de ayuda
- Contacto
- Reporte de bugs
- Solicitud de características
- Soporte empresarial

## 🎨 Diseño y UX

### Principios de Diseño
- **Accesible**: WCAG 2.1 AA compliance
- **Responsive**: Mobile-first
- **Rápido**: Core Web Vitals optimizado
- **Multilingüe**: Español, Inglés, Portugués
- **Tema**: Claro/Oscuro

### Paleta de Colores
```css
--primary: #0066CC      /* Azul agua */
--secondary: #00A86B    /* Verde esmeralda */
--accent: #FF6B6B      /* Coral para alertas */
--neutral: #4A5568     /* Grises */
--background: #FFFFFF  /* Fondo claro */
--text: #1A202C       /* Texto principal */
```

## 🔧 Desarrollo

### Instalación
```bash
cd community-site
npm install
npm run dev
```

### Scripts Disponibles
```bash
npm run dev        # Desarrollo local
npm run build      # Build de producción
npm run start      # Servidor de producción
npm run lint       # Linting
npm run test       # Tests
npm run deploy     # Deploy a producción
```

### Variables de Entorno
```env
NEXT_PUBLIC_API_URL=https://api.boorie.org
NEXT_PUBLIC_SITE_URL=https://boorie.org
DATABASE_URL=postgresql://...
STRAPI_URL=https://cms.boorie.org
```

## 📊 Analytics y Métricas

Rastreamos (respetando privacidad):
- Páginas más visitadas
- Fuentes de tráfico
- Conversiones (descargas, registros)
- Engagement del blog
- Métricas de comunidad

## 🌍 Internacionalización

Soportamos múltiples idiomas:
- Español (es)
- Inglés (en)
- Portugués (pt)
- Francés (fr) - próximamente

## 🚀 Deployment

### Producción
- Frontend: Vercel
- API: AWS ECS
- Base de datos: AWS RDS
- CDN: CloudFront
- Dominio: boorie.org

### Staging
- URL: staging.boorie.org
- Actualización automática desde rama `develop`

## 🤝 Contribuir al Sitio

Para contribuir al sitio web:
1. Lee [CONTRIBUTING.md](../CONTRIBUTING.md)
2. Revisa los [issues abiertos](https://github.com/boorie/boorie/labels/website)
3. Únete al canal #website en Discord
4. Envía tu PR

## 📝 Licencia

El contenido del sitio está bajo Creative Commons BY-SA 4.0
El código está bajo Apache 2.0