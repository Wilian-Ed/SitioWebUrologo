# Sistema de Blog - Instrucciones para el Doctor

## Cómo agregar artículos al blog

### Opción 1: Archivos Markdown (Recomendado para el futuro)

Para implementar un sistema completo de blog con archivos markdown, siga estos pasos:

1. **Instalar dependencias adicionales** (si aún no están instaladas):
   ```bash
   npm install @astrojs/markdown-remark
   ```

2. **Crear la carpeta de contenido**:
   - Cree una carpeta `src/content/blog/` si no existe
   - Configure el esquema de contenido en `src/content/config.ts`

3. **Crear artículos**:
   - Cada artículo será un archivo `.md` en `src/content/blog/`
   - Ejemplo: `src/content/blog/mi-primer-articulo.md`

   ```markdown
   ---
   title: "Título del Artículo"
   description: "Breve descripción del artículo"
   date: 2024-01-15
   author: "Dr. Guillermo Ixquiac"
   image: "/images/blog/articulo-1.jpg"
   tags: ["salud", "prevención"]
   ---

   # Contenido del artículo

   Aquí va el contenido del artículo en formato Markdown...
   ```

### Opción 2: Sistema Actual (Edición Manual)

Actualmente el blog está configurado con artículos de ejemplo en el código. Para agregar nuevos artículos:

1. Edite el archivo `src/pages/blog/index.astro`
2. Busque el array `blogPosts`
3. Agregue nuevos objetos al array siguiendo este formato:

```javascript
const blogPosts = [
	{
		id: 'articulo-1',
		title: 'Título del Artículo',
		excerpt: 'Breve resumen del artículo que aparecerá en la tarjeta...',
		date: '2024-01-15',
		author: 'Dr. Guillermo Ixquiac',
		readTime: '5 min',
		slug: '/blog/articulo-1',
		image: '/images/blog/articulo-1.jpg'
	},
	// Más artículos...
];
```

4. Cree una página individual para cada artículo en `src/pages/blog/[nombre-del-articulo].astro`

### Opción 3: Sistema de Gestión de Contenido (CMS)

Para una solución más completa sin necesidad de editar código:

1. **Considere usar un CMS headless** como:
   - Contentful
   - Sanity.io
   - Strapi
   - Ghost

2. **Beneficios**:
   - Interfaz visual para crear y editar artículos
   - No requiere conocimientos de programación
   - Gestión de imágenes integrada
   - Programación de publicaciones
   - Trabajo colaborativo

## Estructura Recomendada de Artículos

Los artículos sobre urología pueden incluir:

1. **Educación del Paciente**
   - Condiciones urológicas comunes
   - Síntomas a los que prestar atención
   - Cuándo buscar atención médica

2. **Prevención y Salud**
   - Hábitos saludables
   - Prevención de enfermedades
   - Ejercicios y dieta

3. **Tratamientos y Procedimientos**
   - Explicación de procedimientos (ej: HoLEP)
   - Qué esperar antes y después
   - Recuperación y cuidados

4. **Novedades Médicas**
   - Nuevas tecnologías
   - Estudios recientes
   - Avances en tratamientos

## Buenas Prácticas

- **Frecuencia**: Publicar 1-2 artículos por mes
- **Longitud**: Entre 500-1000 palabras
- **Imágenes**: Usar imágenes médicas apropiadas o ilustraciones
- **SEO**: Incluir palabras clave relevantes
- **Tono**: Profesional pero accesible para pacientes
- **Disclaimer**: Incluir nota de que el contenido es informativo y no reemplaza consulta médica

## Contacto para Soporte Técnico

Si necesita ayuda para implementar cualquiera de estas opciones, contacte al equipo de desarrollo.
