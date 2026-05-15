# 🔤 WalkMe Tours - Tipografía & Font Guide

## 📋 TIPOGRAFÍAS PRINCIPALES

### 1. **GT Eesti Pro Display Bold**
**Archivo:** `GT_Eesti_Pro_Display_Bold_-_OTF.otf`  
**Tipo:** Display Font (Titulares y Heroicos)  
**Peso:** Bold (700)  
**Uso Principal:** Títulos principales, headings, branding prominente

**Características:**
- ✨ Tipografía moderna y geométrica
- 🎯 Alto contraste y legibilidad
- 💪 Peso bold perfecto para H1 y H2
- 📱 Excelente en pantalla y impreso
- 🌍 Soporte multiidioma

**Dónde usar:**
```
✅ USAR PARA:
   • H1 - Título principal (48-56px)
   • H2 - Subtítulos heroicos (36-44px)
   • Logo/Branding
   • Banderas promocionales
   • Encabezados de sección prominentes
   • Call-to-action statements

❌ NO USAR PARA:
   • Body text (muy pesado)
   • Párrafos largos
   • Descripciones detalladas
   • Textos pequeños < 24px
```

**Especificaciones técnicas:**
- Familia: GT Eesti Pro Display
- Peso: Bold (700)
- Ancho: Regular
- Tipo: Serif geométrico
- Recomendación de línea: 1.2 - 1.3
- Recomendación de kerning: Manual si es necesario

---

### 2. **Travel Soulmates Weight**
**Archivo:** `Travel_Soulmates_Weight_-_OTF.otf`  
**Tipo:** Decorativa/Display Font  
**Peso:** Regular  
**Uso Principal:** Acentos, detalles decorativos, branding creativo

**Características:**
- 🎨 Fuente artística y creativa
- ✈️ Temática viajera/aventurera
- 🎭 Carácter distintivo y memorable
- 💫 Perfecta para accents y detalles especiales
- 📌 Ligera y elegante

**Dónde usar:**
```
✅ USAR PARA:
   • Tagline/Slogan principal
   • Logotipo (letras específicas)
   • Encabezados decorativos
   • Palabras clave aisladas
   • Iconografía con texto
   • Detalles de branding
   • Redes sociales (posts destacados)

❌ NO USAR PARA:
   • Texto corrido
   • Párrafos
   • Menús de navegación
   • Body text
```

---

## 📐 SISTEMA DE TIPOGRAFÍA COMPLETO

### JERARQUÍA VISUAL

```
NIVEL 1 - TITULARES PRINCIPALES (Display)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: GT Eesti Pro Display Bold
Tamaño: 48-56px
Peso: Bold (700)
Línea: 1.2
Color: #E91E8C (Magenta) o #2D6B4F (Verde)
Ejemplo: "Tu próxima AVENTURA"

NIVEL 2 - SUBTÍTULOS HEROICOS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: GT Eesti Pro Display Bold
Tamaño: 36-44px
Peso: Bold (700)
Línea: 1.3
Color: #F4DC4F (Amarillo) o #FFFFFF
Ejemplo: "Paradise Islands"

NIVEL 3 - ENCABEZADOS (H3)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: Inter, Poppins (fallback)
Tamaño: 28px
Peso: Semi-bold (600)
Línea: 1.4
Color: #2D6B4F
Ejemplo: "Qué incluye este tour"

NIVEL 4 - ENCABEZADOS (H4)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: Inter, Poppins (fallback)
Tamaño: 24px
Peso: Semi-bold (600)
Línea: 1.4
Color: #2D6B4F
Ejemplo: "Horarios disponibles"

NIVEL 5 - TEXTO CUERPO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: Inter, Roboto, Poppins
Tamaño: 16px
Peso: Regular (400)
Línea: 1.6
Color: #333333
Ejemplo: "Paragrafos largos de descripción..."

NIVEL 6 - TEXTO PEQUEÑO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: Inter, Roboto
Tamaño: 14px
Peso: Regular (400)
Línea: 1.6
Color: #666666
Ejemplo: "Información adicional, subtextos"

NIVEL 7 - CAPTIONS/LABELS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Fuente: Inter, Roboto
Tamaño: 12px
Peso: Regular (400)
Línea: 1.5
Color: #999999
Ejemplo: "Duración • 8 horas"
```

---

## 🎨 COMBINACIONES TIPOGRÁFICAS RECOMENDADAS

### Combinación 1: HEROICA (Impactante)
```
H1: GT Eesti Pro Display Bold - 52px - #E91E8C
   "Tu próxima"
Decorativo: Travel Soulmates - 48px - #F4DC4F
   "AVENTURA"
```

### Combinación 2: ELEGANTE (Sofisticada)
```
H1: GT Eesti Pro Display Bold - 48px - #2D6B4F
   "Paradise Islands"
H2: Travel Soulmates - 32px - #D4A74F
   "Snorkel & Cenotes"
```

### Combinación 3: FUNCIONAL (Legibilidad)
```
H1: GT Eesti Pro Display Bold - 44px - #E91E8C
   "Reservation Confirmed"
Body: Inter 16px - #333333
   "Tu tour ha sido reservado con éxito..."
```

---

## 💻 IMPLEMENTACIÓN WEB

### @font-face CSS

```css
/* GT Eesti Pro Display Bold */
@font-face {
    font-family: 'GT Eesti Pro Display';
    src: url('/fonts/GT_Eesti_Pro_Display_Bold.otf') format('opentype');
    font-weight: 700;
    font-style: normal;
    font-display: swap;
}

/* Travel Soulmates Weight */
@font-face {
    font-family: 'Travel Soulmates';
    src: url('/fonts/Travel_Soulmates_Weight.otf') format('opentype');
    font-weight: 400;
    font-style: normal;
    font-display: swap;
}

/* Fallback Fonts (System Fonts) */
@font-face {
    font-family: 'Inter';
    src: url('/fonts/inter.woff2') format('woff2');
    font-display: swap;
}
```

### Uso en CSS

```css
/* Títulos Principales */
h1 {
    font-family: 'GT Eesti Pro Display', 'Montserrat', sans-serif;
    font-size: 48px;
    font-weight: 700;
    line-height: 1.2;
    letter-spacing: -1px;
    color: #E91E8C;
}

/* Subtítulos Decorativos */
.hero-accent {
    font-family: 'Travel Soulmates', 'Poppins', sans-serif;
    font-size: 44px;
    font-weight: 400;
    color: #F4DC4F;
    text-transform: uppercase;
    letter-spacing: 2px;
}

/* Texto Regular */
p, body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 1.6;
    color: #333333;
}
```

---

## 📱 RESPONSIVE TYPOGRAPHY

### DESKTOP (1200px+)
```
H1: 56px
H2: 44px
H3: 32px
H4: 24px
Body: 16px
Small: 14px
Caption: 12px
```

### TABLET (768px - 1199px)
```
H1: 48px
H2: 36px
H3: 28px
H4: 22px
Body: 16px
Small: 14px
Caption: 12px
```

### MOBILE (< 768px)
```
H1: 36px
H2: 28px
H3: 24px
H4: 20px
Body: 15px
Small: 13px
Caption: 11px
```

---

## ✨ DETALLES TIPOGRÁFICOS

### KERNING & TRACKING
```
Display Bold (Titles):
  Letter-spacing: -1px a -2px (apriete)
  
Travel Soulmates:
  Letter-spacing: 2px a 4px (expansión)
  
Body Text:
  Letter-spacing: 0px (normal)
```

### LINE HEIGHT
```
H1-H3: 1.2 - 1.3 (tight, para impacto)
H4-H5: 1.4 (legibilidad mejorada)
Body: 1.6 (confort de lectura)
Small text: 1.5 (readability)
```

### TEXT TRANSFORM
```
✅ MAYÚSCULAS:
   - Títulos principales: GT Eesti Pro Bold
   - Labels: text-transform: uppercase (14px)
   
❌ EVITAR MAYÚSCULAS:
   - Textos largos
   - Párrafos
   - Descripciones
```

---

## 🎯 CASOS DE USO REALES

### HERO SECTION (Home Page)
```
Fondo: #2D6B4F
═══════════════════════════════════════
Agencia oficial del Grupo Xcaret
(Travel Soulmates, 20px, #D4A74F)

Tu próxima AVENTURA
(GT Eesti Bold, 52px, #E91E8C + #F4DC4F)

Agencia oficial • Mejores precios • Confirmación instantánea
(Inter, 16px, #FFFFFF)

[VER TODOS LOS TOURS]
(Inter, 16px Bold, #2D6B4F fondo #F4DC4F)
```

### TOUR CARD
```
┌─────────────────────────────┐
│ Paradise Islands            │ ← GT Eesti Bold, 24px, #2D6B4F
│ Snorkel • 8 horas          │ ← Inter, 14px, #666666
│ Incluye comida y equipo     │ ← Inter, 14px, #333333
│                             │
│ USD $89 / MXN $1,646        │ ← Inter Bold, 18px, #E91E8C
│                             │
│  [RESERVAR AHORA]          │ ← Inter Bold, 14px, CTA
└─────────────────────────────┘
```

### DESCRIPCIÓN DE TOUR
```
¿Qué incluye este tour?
(GT Eesti Bold, 28px, #2D6B4F)

✓ Acceso a cenotes naturales
✓ Equipo de snorkel incluido
✓ Almuerzo típico yucateco
✓ Traslados desde hotel

(Inter, 16px, body text)
```

---

## 📚 FALLBACK FONTS (Si no cargan las OTF)

Si la conexión es lenta o hay problemas, use estas alternativas:

```css
/* Para GT Eesti Pro Display (Display Bold) */
font-family: 'GT Eesti Pro Display', Montserrat, 'Trebuchet MS', sans-serif;

/* Para Travel Soulmates (Decorativa) */
font-family: 'Travel Soulmates', 'Brush Script MT', Poppins, cursive;

/* Para Body Text */
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
```

---

## 🔧 INSTALACIÓN

### Para Diseñadores (Figma, Adobe):
1. Descargar los archivos `.otf`
2. Doble-clic para instalar en tu sistema
3. Reiniciar la aplicación de diseño
4. Buscar "GT Eesti" y "Travel Soulmates" en las fuentes

### Para Desarrolladores (Web):
1. Subir archivos a carpeta `/fonts/` en servidor
2. Usar `@font-face` como se especifica arriba
3. Agregar preload en `<head>`:
```html
<link rel="preload" as="font" href="/fonts/GT_Eesti_Pro_Display_Bold.otf" type="font/otf" crossorigin>
<link rel="preload" as="font" href="/fonts/Travel_Soulmates_Weight.otf" type="font/otf" crossorigin>
```

---

## 📊 RESUMEN RÁPIDO

| Elemento | Fuente | Tamaño | Peso | Color |
|----------|--------|--------|------|-------|
| H1 Heroico | GT Eesti Bold | 48-56px | 700 | #E91E8C |
| H2 Subtítulo | GT Eesti Bold | 36-44px | 700 | #F4DC4F |
| H3/H4 | Inter/Poppins | 24-28px | 600 | #2D6B4F |
| Body | Inter/Roboto | 16px | 400 | #333333 |
| Decorativo | Travel Soulmates | 32-48px | 400 | #D4A74F |
| Labels | Inter | 12-14px | 400 | #999999 |

---

**Última actualización:** 9 mayo 2026  
**Responsable:** Maria Wignall - WalkMe Tours  
**Archivos:** GT_Eesti_Pro_Display_Bold_-_OTF.otf | Travel_Soulmates_Weight_-_OTF.otf
