# Tarjeta de Matrimonio 3D

Invitación web interactiva para la boda de **Yenifer & César** — 30 de septiembre de 2026, Restaurante La Criolla (Anserma, Caldas).

Construida con **Svelte 5 (runes)**, **TypeScript**, **Tailwind CSS 4** y **Three.js**.

## Inicio rápido

```bash
npm install
npm run dev
```

## Scripts

| Comando | Descripción |
|---|---|
| `npm run dev` | Servidor de desarrollo |
| `npm run build` | Build de producción |
| `npm run preview` | Vista previa del build |
| `npm run check` | Verificación de tipos |
| `npm run deploy` | Build + despliegue a GitHub Pages |
| `npm run photos` | Regenerar derivados de fotos |
| `npm run shot` | Captura headless (Chrome) |
| `npm run test` | Tests |

## Estructura

```
src/
├─ App.svelte              # Canvas WebGL + secciones HTML
├─ app.css                 # Tema Negro & Oro (Tailwind 4)
├─ lib/
│  ├─ config.ts            # Configuración editable (nombres, fecha, fotos)
│  ├─ state.svelte.ts      # Estado con runes
│  ├─ personal.ts          # Datos personalizados
│  ├─ preload.ts           # Precarga de multimedia
│  ├─ api/rsvp.ts          # Envío de confirmaciones
│  ├─ components/          # UI: Preloader, Hero, Gallery, Countdown, RSVP...
│  └─ three/
│     ├─ world.ts          # Renderer, cámara, scroll, picking
│     ├─ envelope.ts       # Acto I-II: sobre, lacre, tarjeta
│     ├─ gallery.ts        # Acto III: carrusel de fotos 3D
│     ├─ dust.ts           # Partículas de polvo dorado
│     ├─ materials.ts      # Materiales PBR
│     ├─ textures.ts       # Carga y generación de texturas
│     └─ utils.ts          # Utilidades de animación
├─ public/fotos/           # Fotos optimizadas (no subir originales)
├─ libphp/                 # Backend PHP (confirmaciones → Google Sheets)
└─ scripts/                # Scripts auxiliares
```

## Despliegue

```bash
npm run deploy
```

Publica el build en **GitHub Pages** vía `gh-pages`.

Para despliegue manual: sube el contenido de `dist/` al servidor destino.

## Stack

- **Svelte 5** — runes, reactividad por signals
- **Three.js** — escena 3D: sobre lacrado, carrusel de fotos, polvo dorado
- **Tailwind CSS 4** — theming con `@theme`
- **TypeScript** — tipado estricto
- **Vite** — bundler y dev server
