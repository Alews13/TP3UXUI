# Coffea landing page

Landing page estática para el TP de Diseño UX/UI. Implementada con HTML5 semántico y CSS3, sin JavaScript ni frameworks.

## Estructura

- `index.html`: las nueve secciones de la landing.
- `css/tokens.css`: colores, tipografías, radios, escala tipográfica y espaciado.
- `css/base.css`: reset, estilos base, foco visible y movimiento reducido.
- `css/layout.css`: contenedores, espaciado y botones.
- `css/components/`: estilos independientes por componente.
- `assets/img/` y `assets/icons/`: directorios previstos para exportaciones finales desde Figma.
- `404.html`: página de error.
- `netlify.toml`: publicación desde la raíz y encabezados básicos.

## Ejecutar localmente

Abrir `index.html` directamente en un navegador o servir la carpeta con cualquier servidor estático local. No hay comando de build.

## Despliegue en Netlify

1. Subir el proyecto a un repositorio GitHub o GitLab.
2. En Netlify, importar ese repositorio.
3. Dejar Build command vacío y configurar Publish directory como `.`.
4. Publicar la rama principal. Netlify proporciona HTTPS automáticamente.

## Decisiones y pendientes respecto del PRD

- El sitio contiene las nueve secciones indicadas y utiliza HTML semántico, BEM, custom properties, Flexbox/Grid y carruseles con `scroll-snap`.
- El menú móvil usa `<details>/<summary>`; los favoritos son estados visuales con checkbox; el newsletter valida el email en el navegador, pero no envía datos.
- Las fotos de productos y fondos apuntan actualmente a imágenes remotas de Unsplash para que la maqueta sea visible. Para fidelidad final, reemplazarlas por los 29 assets exportados desde el Figma, comprimirlos a AVIF/WebP con fallback JPG y confirmar las licencias.
- Los importes conservan `Rs. 200` como en el diseño de referencia. El PRD indica que debe confirmarse si se reemplazan por pesos argentinos.
- El diseño de referencia solo cubre 1920 px. Los breakpoints restantes son una propuesta responsive basada en el PRD, pendiente de validación con diseño.
- No se puede afirmar que se cumplan los umbrales de Lighthouse, validadores W3C o diferencia visual de 4 px sin ejecutar las pruebas en producción y comparar contra el archivo Figma original.

## Checklist de entrega

- [x] Nueve secciones en una página.
- [x] Sin JavaScript.
- [x] Design tokens centralizados.
- [x] HTML semántico, foco visible y skip link.
- [x] Diseño responsive sin anchos fijos globales.
- [ ] Sustituir imágenes remotas por assets aprobados/exportados desde Figma.
- [ ] Validar HTML y CSS en W3C.
- [ ] Medir Lighthouse en la URL de Netlify.
- [ ] Comparar visualmente contra Figma a 1920 px.
