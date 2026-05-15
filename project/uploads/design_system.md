# 🎨 Design System — WalkMe Tours

> **Documento:** Paleta de colores, tipografía, espaciado y componentes base  
> **Versión:** 1.0 | **Fecha:** Abril 2026  
> **Relacionado con:** [Assets](../Assets/) | [Home Copy](../../3_CONTENIDO/Home/home_page_copy.md)

---

## Paleta de Colores

### Colores Primarios

| Nombre | HEX | RGB | Tailwind | Uso |
|--------|-----|-----|----------|-----|
| **Verde WalkMe** | `#00A651` | 0, 166, 81 | `green-600` custom | CTAs, badges, highlights |
| **Azul Oscuro** | `#003366` | 0, 51, 102 | `blue-900` custom | Headlines, nav, texto principal |
| **Naranja Acento** | `#FF6B00` | 255, 107, 0 | `orange-500` custom | Urgencia, badges, precio |

### Colores Neutros

| Nombre | HEX | RGB | Tailwind | Uso |
|--------|-----|-----|----------|-----|
| **Blanco** | `#FFFFFF` | 255, 255, 255 | `white` | Fondos, texto sobre oscuro |
| **Gris Claro** | `#F5F7FA` | 245, 247, 250 | `gray-50` | Fondos de sección alternada |
| **Gris Medio** | `#E8ECF0` | 232, 236, 240 | `gray-200` | Bordes, separadores |
| **Gris Texto** | `#6B7280` | 107, 114, 128 | `gray-500` | Texto secundario, meta |
| **Negro Suave** | `#1A1A2E` | 26, 26, 46 | `gray-900` custom | Body text principal |

### Colores Semánticos

| Nombre | HEX | Uso |
|--------|-----|-----|
| **Éxito** | `#16A34A` | Booking confirmado, disponible |
| **Error** | `#DC2626` | Error de pago, agotado |
| **Advertencia** | `#D97706` | Pocas plazas, urgencia |
| **Info** | `#2563EB` | Notas informativas |

### Variables CSS (Tailwind Config)

```javascript
// tailwind.config.ts
module.exports = {
  theme: {
    extend: {
      colors: {
        brand: {
          green:  '#00A651',
          'green-dark': '#007A3D',
          'green-light': '#E6F7EE',
          navy:   '#003366',
          'navy-light': '#0A4A8C',
          orange: '#FF6B00',
          'orange-light': '#FFF0E6',
        },
      },
    },
  },
}
```

---

## Tipografía

### Fuentes

| Rol | Fuente | Variantes | Fuente de carga |
|-----|--------|-----------|----------------|
| **Headings** | Inter | 700 (Bold), 800 (ExtraBold) | Google Fonts |
| **Body** | Inter | 400 (Regular), 500 (Medium) | Google Fonts |
| **Mono** (código) | JetBrains Mono | 400 | Google Fonts |

**Por qué Inter:** Excelente legibilidad en pantalla, funciona perfectamente en español e inglés, libre y carga rápido.

### Escala Tipográfica

| Nombre | Tamaño | Line Height | Weight | Tailwind | Uso |
|--------|--------|-------------|--------|----------|-----|
| **Display XL** | 56px | 1.1 | 800 | `text-5xl font-extrabold` | Hero headlines |
| **Display L** | 40px | 1.2 | 700 | `text-4xl font-bold` | H1 de páginas internas |
| **H2** | 32px | 1.25 | 700 | `text-3xl font-bold` | Section headlines |
| **H3** | 24px | 1.35 | 600 | `text-2xl font-semibold` | Card titles, sub-sections |
| **H4** | 20px | 1.4 | 600 | `text-xl font-semibold` | Tour names, pillars |
| **Body L** | 18px | 1.6 | 400 | `text-lg` | Descripción larga, about |
| **Body** | 16px | 1.6 | 400 | `text-base` | Texto general |
| **Body S** | 14px | 1.5 | 400 | `text-sm` | Labels, meta, badges |
| **Caption** | 12px | 1.4 | 400 | `text-xs` | Notas, términos, footers |

### Ejemplo de uso Next.js

```jsx
// next.config.ts — cargar fuente
import { Inter } from 'next/font/google'

const inter = Inter({
  subsets: ['latin'],
  variable: '--font-inter',
  display: 'swap',
})

// En layout.tsx
<html className={inter.variable}>
```

---

## Espaciado

Usar escala de 4px base (Tailwind default).

| Token | px | Tailwind | Uso típico |
|-------|----|----------|-----------|
| `xs` | 4px | `p-1` | Gap mínimo, icono-texto |
| `sm` | 8px | `p-2` | Padding interno de badges |
| `md` | 16px | `p-4` | Padding de cards small |
| `lg` | 24px | `p-6` | Padding de cards standard |
| `xl` | 32px | `p-8` | Padding de secciones |
| `2xl` | 48px | `p-12` | Separación entre secciones |
| `3xl` | 64px | `p-16` | Espaciado hero |
| `4xl` | 96px | `p-24` | Márgenes de página desktop |

### Secciones de página

```css
/* Padding estándar para secciones */
.section { @apply py-16 md:py-24; }
.section-sm { @apply py-10 md:py-16; }

/* Max width del contenedor */
.container { @apply max-w-7xl mx-auto px-4 sm:px-6 lg:px-8; }
```

---

## Componentes Base

### Botones

```jsx
// Primario — Verde (CTA principal)
<button className="bg-brand-green hover:bg-brand-green-dark text-white font-semibold px-6 py-3 rounded-lg transition-colors">
  Book Now
</button>

// Secundario — Outline azul
<button className="border-2 border-brand-navy text-brand-navy hover:bg-brand-navy hover:text-white font-semibold px-6 py-3 rounded-lg transition-colors">
  Learn More
</button>

// WhatsApp — Verde WhatsApp
<button className="bg-[#25D366] hover:bg-[#1ebe5d] text-white font-semibold px-6 py-3 rounded-lg flex items-center gap-2 transition-colors">
  <WhatsAppIcon /> Chat with Us
</button>

// Urgencia — Naranja
<button className="bg-brand-orange hover:bg-orange-600 text-white font-semibold px-6 py-3 rounded-lg transition-colors">
  Reserve Now — Limited Spots
</button>
```

### Cards de Tour

```
┌─────────────────────────────┐
│  [IMAGEN 16:9]              │
│  [Badge categoría]          │
├─────────────────────────────┤
│  Nombre del Tour            │ ← H4, brand-navy
│  ★★★★★ 4.9 (127)           │ ← Caption, gray
│  ⏱ 4h · 👥 Máx 8 personas  │ ← Body S, gray
│                             │
│  "Descripción breve..."     │ ← Body S, 2 líneas máx
│                             │
│  Desde $35 USD    [Ver →]   │ ← Price verde · CTA
└─────────────────────────────┘
```

### Badges / Pills

```jsx
// Categoría
<span className="bg-brand-green-light text-brand-green text-xs font-semibold px-3 py-1 rounded-full">
  Xcaret Parks
</span>

// Destacado
<span className="bg-brand-orange text-white text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wide">
  ⭐ Most Popular
</span>

// Disponible
<span className="bg-green-100 text-green-700 text-xs font-semibold px-3 py-1 rounded-full">
  ● Available
</span>

// Agotado
<span className="bg-red-100 text-red-600 text-xs font-semibold px-3 py-1 rounded-full">
  ● Sold Out
</span>
```

### Rating Stars

```jsx
// Mostrar: ★★★★★ 4.9 (500 reviews)
<div className="flex items-center gap-1">
  <div className="flex text-yellow-400">★★★★★</div>
  <span className="font-semibold text-sm text-gray-900">4.9</span>
  <span className="text-sm text-gray-500">(500 reviews)</span>
</div>
```

---

## Iconografía

**Librería:** Lucide React (ya incluida en el stack)

| Icono | Uso | Nombre Lucide |
|-------|-----|---------------|
| 📍 Mapa | Ubicación, tours | `MapPin` |
| ⭐ Estrella | Rating | `Star` |
| ⏱ Reloj | Duración | `Clock` |
| 👥 Personas | Grupo | `Users` |
| 💬 Chat | WhatsApp | `MessageCircle` |
| ✓ Check | Incluido | `Check` |
| ✗ X | No incluido | `X` |
| 🗓 Calendario | Fechas | `Calendar` |
| 💳 Tarjeta | Pago | `CreditCard` |
| 🔒 Candado | Seguridad | `Lock` |
| 🔋 Batería | E-bikes | `Battery` |
| 🚴 Bici | E-bikes | `Bike` |
| 🌿 Hoja | Eco/Natural | `Leaf` |
| ⚡ Rayo | Rápido | `Zap` |

---

## Imágenes — Estilo Visual

### Filtros y Tratamiento

- **Fotos de hero:** Overlay oscuro `rgba(0,0,0,0.35)` para legibilidad del texto
- **Cards de tour:** Sin filtro, imágenes vividas y saturadas
- **Hover en cards:** Zoom suave `scale-105` con `transition-transform duration-300`
- **About/Team:** Blanco y negro suave con acento verde en hover (opcional)

### Ratio de imágenes por componente

| Componente | Ratio | Ejemplo |
|-----------|-------|---------|
| Hero | 16:9 o 21:9 (cinematic) | 1920×1080 |
| Tour card | 3:2 | 600×400 |
| Blog thumbnail | 16:9 | 800×450 |
| About team | 1:1 | 400×400 |
| Partner logos | Variable (original) | SVG preferido |

---

## Responsive Breakpoints

```javascript
// Tailwind defaults (usar estos)
sm:  640px   // Móvil grande / tablet pequeña
md:  768px   // Tablet
lg:  1024px  // Desktop pequeño
xl:  1280px  // Desktop estándar
2xl: 1536px  // Desktop grande
```

**Regla general:** Diseñar primero para 390px (iPhone 14), luego expandir.

---

## Tokens de Sombra

```javascript
// tailwind.config.ts
boxShadow: {
  'card': '0 2px 8px rgba(0, 51, 102, 0.08)',
  'card-hover': '0 8px 24px rgba(0, 51, 102, 0.15)',
  'modal': '0 20px 60px rgba(0, 0, 0, 0.3)',
  'button': '0 2px 4px rgba(0, 166, 81, 0.3)',
}
```

---

*Ver también:*  
*→ [Logos y Assets](../Assets/lista_de_logos_imagenes.md)*  
*→ [Home Copy](../../3_CONTENIDO/Home/home_page_copy.md)*
