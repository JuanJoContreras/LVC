# La Voz del Campo — Landing Page

Landing institucional one-page para la Confederación Nacional de la Agricultura Familiar Campesina de Chile.

## Estructura

```
/
├── index.html          # Landing completa (HTML + CSS + JS, sin dependencias)
├── assets/img/         # Imágenes (carrusel hero, eventos, logo)
├── vercel.json
└── README.md
```

No usa frameworks ni build step. Es HTML estático puro — funciona en cualquier hosting (Vercel, Tecnoinver/cPanel, GitHub Pages).

## Subir a GitHub

```bash
git init
git add .
git commit -m "Landing La Voz del Campo — versión inicial"
git branch -M main
git remote add origin https://github.com/JuanJoContreras/landing.vozdelcampo.git
git push -u origin main
```

## Desplegar en Vercel

**Opción A — Dashboard:**
1. Entra a vercel.com → "Add New Project"
2. Importa el repo `landing.vozdelcampo` desde GitHub
3. Framework preset: **Other** (sitio estático, sin build command)
4. Deploy

**Opción B — CLI:**
```bash
npm i -g vercel
vercel login
vercel --prod
```

Al conectar el dominio `vozdelcampo.cl` en Vercel: Project Settings → Domains → agregar dominio → apuntar los DNS según lo indicado por Vercel (o mantener en Tecnoinver si se define ese hosting, ver Cláusula 2 del contrato).

## Pendientes de contenido (ver checklist de insumos)

- [ ] Logo real de La Voz del Campo (reemplazar el marcador "VC" en `.brand-mark` y `.foot-brand .m`)
- [ ] 9 fotos del directorio (`assets/img/directorio/`)
- [ ] Fotos + descripción de 3 a 6 eventos (`assets/img/eventos/`)
- [ ] Textos institucionales definitivos (misión/visión ya incorporados desde el PPT Asamblea La Ligua 2026)
- [ ] Correo receptor del formulario de contacto (actualmente placeholder en `handleSubmit()`)
- [ ] Credenciales de hosting si se usa Tecnoinver en vez de Vercel

## Carrusel del Hero

El fondo del hero rota automáticamente cada 5 segundos entre 4 imágenes (`assets/img/campo1.jpg` a `campo6.jpg`, extraídas del material de campo entregado). Para agregar o cambiar imágenes, editar el bloque `#heroCarousel` en `index.html` y agregar/quitar `<div class="hero-slide">`.
