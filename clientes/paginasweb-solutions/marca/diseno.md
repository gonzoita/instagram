---
doc_type: sistema_diseno_marca
schema_version: "3.0"
brand_name: "paginasweb.solutions"
profile_ref: "perfil-maestro-paginasweb-solutions.md"
identity_path: "normalizar"
production_route: "ambas"
direction: "Tecnológica B2B de Alta Velocidad (Contraste Crítico)"
generated_at: "2026-10-09"
production_ready: false
---

# paginasweb.solutions — SISTEMA DE DISEÑO

## D00 · Estado del sistema y resumen ejecutivo

Este sistema normaliza los activos de identidad de `paginasweb.solutions` a partir de su perfil maestro B2B y su isotipo angular (monograma "PW" dinámico en contenedor triangular). Se establece una arquitectura de diseño de alto impacto visual y contraste estricto, calibrada para servir tanto a la ruta de WordPress (tema de bloques FSE) como a la ruta estática (HTML5/CSS sin dependencias).

La identidad resuelve una deficiencia técnica crítica del rojo primario (`#E50914`): su insuficiencia de contraste sobre fondo blanco (ratio 3.99:1). Para blindar la accesibilidad WCAG AA sin alterar el impacto de marca, se crea el rol formal `brand-primary-text` (`#B8000A`, ratio 5.92:1 sobre blanco), reservado para tipografía, enlaces y elementos interactivos sobre superficies claras. La combinación base opera con una estética tecnológica oscura predominante (`bg: #0D0D0D`, `surface: #171717`), tipografía grotesca técnica en titulares (*Space Grotesk*) y neutralidad corporativa en textos de lectura (*Inter*).

El sistema se entrega cerrado con tokens congelados, reglas de animación acelerada por hardware (`transform` y `opacity`), componentes estandarizados (`tarjeta-borde` y `boton-suave`) y exportaciones ejecutables para ambas rutas de despliegue.

---

## D01 · Fundamento — Decisiones del perfil maestro hacia el sistema visual

| Sección del Perfil Maestro | Decisión de Negocio / Estrategia | Decisión Visual Resultante |
|---|---|---|
| **M02 / M03 / M04** | Velocidad de ejecución (48h), pragmatismo B2B, sin burocracia de agencias tradicionales. | Tiempos de animación ágiles (`quick: 200ms`, `smooth: 320ms`), composición geométrica firme, eliminación de ornamentos decorativos y curvaturas infantiles. |
| **M05** | Voz asertiva, sobria, técnica, de empresario a empresario. | Tipografía de lectura neutra (*Inter*), jerarquía tipográfica con escala modular de estándar corporativo (1.250), titulares técnicos en *Space Grotesk*. |
| **M06 / M07** | Ecosistemas de ventas B2B, software propio, pauta y automatización con IA. | Estética de terminal de software y plataforma digital de alta tecnología: fondo oscuro profundo (`#0D0D0D`), bordes milimétricos técnicos (`#262626`) y acentos de ejecución en rojo industrial. |
| **M12** | Identidad previa con isotipo angular "PW" en rojo y blanco sobre negro. | Preservación del carácter del isotipo mediante normalización del rojo `#E50914`, bifurcación a `#B8000A` para legibilidad textual y establecimiento de radios suaves (4px a 8px) alineados al acabado del monograma. |
| **M16** | Prohibición de fórmulas mágicas y banalidad estética. | Prohibición absoluta de degradados multicolor, tipografías manuscritas, sombras difusas decorativas e iconografía inconsistente. |

---

## D02 · Tabla de slugs congelados

Los slugs listados a continuación representan identificadores de sistema inmutables. No deben alterarse tras el paso a producción.

| Categoría | Slug Canónico | Nombre Visible (Editor) | Rol y Ámbito de Uso |
|---|---|---|---|
| Color | `brand-primary` | Primario Marca | Rojo enérgico del isotipo para fondos, acentos y superficies grandes. |
| Color | `brand-primary-text` | Primario Texto | Rojo oscuro accesible (5.92:1) reservado para enlaces y textos sobre fondos claros. |
| Color | `text-on-brand` | Texto sobre Marca | Blanco puro contrastado (4.81:1) sobre superficies `brand-primary`. |
| Color | `brand-secondary` | Secundario Marca | Rojo sangre profundo para estados hover y contrastes secundarios. |
| Color | `accent` | Acento Interactivo | Rojo de alta vibración para micro-interacciones y estados hover. |
| Color | `accent-hover` | Acento Hover | Variante tonal para retroalimentación al interactuar. |
| Color | `bg` | Fondo Principal | Negro carbón profundo como lienzo base de la interfaz tecnológica. |
| Color | `surface` | Superficie Base | Gris carbón para contenedores, tarjetas y paneles. |
| Color | `surface-alt` | Superficie Alterna | Gris de elevación para filas alternas, bloques secundarios y badges. |
| Color | `border` | Borde Técnico | Gris sutil para delimitación de bloques y rejillas. |
| Color | `text-strong` | Texto Principal | Blanco tiza de máxima jerarquía para lectura sobre superficies oscuras. |
| Color | `text-muted` | Texto Secundario | Gris medio para metadatos, subtítulos y etiquetas descriptivas. |
| Color | `text-inverse` | Texto Inverso | Negro profundo cuando se fuerza un bloque o botón sobre fondo claro. |
| Color | `success` | Éxito | Verde funcional para confirmaciones operativas. |
| Color | `warning` | Advertencia | Ámbar técnico para alertas y estados de precaución. |
| Color | `danger` | Error | Rojo crítico de sistema para fallos y validaciones. |
| Color | `info` | Información | Azul técnico para avisos del sistema. |
| Tipografía | `display` | Tipografía Titulares | Familia técnica geométrica (*Space Grotesk*) para títulos de impacto. |
| Tipografía | `body` | Tipografía Cuerpo | Familia neutra de alto rendimiento (*Inter*) para lectura y datos. |
| Espacio | `xs`, `sm`, `md`, `lg`, `xl`, `xxl`, `xxxl` | Espaciados | Escala modular basada en múltiplos de 4px (4px a 96px). |
| Radio | `none`, `sm`, `md`, `lg`, `xl`, `full` | Esquinas | Radios de contorno del sistema, dominando `md` (8px) y `sm` (4px). |

---

## D03 · Logo

### Versiones del sistema
1. **Isotipo Principal:** Monograma estilizado "PW" en blanco insertado en contenedor triangular rojo sobre base cuadrada oscura (versión canónica actual).
2. **Horizontal (Pendiente de vectorización):** Isotipo al extremo izquierdo acompañado de la marca denominativa en bloque tipográfico técnico: `paginasweb.solutions`.
3. **Monocromo Positivo (Negro sobre fondo blanco):** Triángulo y monograma delimitados en negro puro `#000000` con calado perimetral.
4. **Monocromo Negativo (Blanco sobre fondo oscuro):** Totalidad de trazos y monograma en blanco puro `#FFFFFF`.
5. **Favicon / App Icon:** Monograma "PW" maximizado con sangría mínima de seguridad en formato 32×32px, 192×192px y 512×512px.

### Zona de protección y escala mínima
* **Zona de protección (1X):** Unidad de medida $X$ equivalente al ancho de la barra diagonal de la letra "P" del monograma. Ningún texto, margen de página ni elemento gráfico puede situarse a menos de $1X$ de cualquier extremo del logo. En soportes mínimos restringidos (favicons o avatares), se tolera $0.5X$.
* **Tamaño mínimo digital:** Isotipo aislado: 24×24px. Logotipo completo horizontal: 160px de ancho.
* **Tamaño mínimo impreso:** Isotipo aislado: 8 mm de ancho. Logotipo completo: 35 mm de ancho.

### Reglas de fondo
* **Fondos permitidos:** `bg` (`#0D0D0D`), `surface` (`#171717`), `surface-alt` (`#212121`), y blanco puro `#FFFFFF` (únicamente con versión normalizada con letras oscuras o monocromo positivo).
* **Sobre fotografía:** Permitido exclusivamente sobre zonas homogéneas de bajo ruido visual con luminancia controlada o mediante placa de contraste oscura al 60% de opacidad.

### Usos prohibidos
1. Deformar la proporción horizontal o vertical del isotipo.
2. Rotar el ángulo del triángulo o del monograma respecto a su eje de diseño.
3. Modificar los colores del isotipo alterando el rojo corporativo o aplicando degradados.
4. Aplicar sombras difusas, biseles, brillos o efectos 3D.
5. Emplear el isotipo rasterizado con fondo negro cuadrado montado sobre fondos claros sin recortar.
6. Reemplazar la tipografía del nombre de la marca por fuentes serifadas o script.
7. Disminuir la escala por debajo del umbral mínimo donde la punta del triángulo interior se empasta.
8. Colocar el logo sobre fondos de color saturado (ej. verde, azul, naranja).

---

## D04 · Color

### Valores y conversiones técnicas

```
[brand-primary]
HEX:     #E50914
RGB:     rgb(229, 9, 20)
HSL:     hsl(357°, 92%, 47%)
CMYK:    0%, 96%, 91%, 10% (Aproximación digital sujeta a prueba física)
Pantone: PMS 185 C (Referencia de aproximación)

[brand-primary-text]
HEX:     #B8000A
RGB:     rgb(184, 0, 10)
HSL:     hsl(357°, 100%, 36%)
CMYK:    0%, 100%, 95%, 28%
Pantone: PMS 187 C

[text-on-brand]
HEX:     #FFFFFF
RGB:     rgb(255, 255, 255)
HSL:     hsl(0°, 0%, 100%)

[brand-secondary]
HEX:     #8F0007
RGB:     rgb(143, 0, 7)
HSL:     hsl(357°, 100%, 28%)

[accent]
HEX:     #FF1F2D
RGB:     rgb(255, 31, 45)
HSL:     hsl(356°, 100%, 56%)

[accent-hover]
HEX:     #CC000B
RGB:     rgb(204, 0, 11)
HSL:     hsl(357°, 100%, 40%)

[bg]
HEX:     #0D0D0D
RGB:     rgb(13, 13, 13)
HSL:     hsl(0°, 0%, 5%)

[surface]
HEX:     #171717
RGB:     rgb(23, 23, 23)
HSL:     hsl(0°, 0%, 9%)

[surface-alt]
HEX:     #212121
RGB:     rgb(33, 33, 33)
HSL:     hsl(0°, 0%, 13%)

[border]
HEX:     #2E2E2E
RGB:     rgb(46, 46, 46)
HSL:     hsl(0°, 0%, 18%)

[text-strong]
HEX:     #F5F5F5
RGB:     rgb(245, 245, 245)
HSL:     hsl(0°, 0%, 96%)

[text-muted]
HEX:     #A3A3A3
RGB:     rgb(163, 163, 163)
HSL:     hsl(0°, 0%, 64%)

[text-inverse]
HEX:     #0D0D0D
RGB:     rgb(13, 13, 13)
HSL:     hsl(0°, 0%, 5%)

[success]
HEX:     #10B981
RGB:     rgb(16, 185, 129)
HSL:     hsl(160°, 84%, 39%)

[warning]
HEX:     #F59E0B
RGB:     rgb(245, 158, 11)
HSL:     hsl(38°, 92%, 50%)

[danger]
HEX:     #EF4444
RGB:     rgb(239, 68, 68)
HSL:     hsl(0°, 84%, 60%)

[info]
HEX:     #3B82F6
RGB:     rgb(59, 130, 246)
HSL:     hsl(217°, 91%, 60%)
```

> **ADVERTENCIA OBLIGATORIA:** La conversión a CMYK es aproximada y depende directamente del perfil de color asignado (FOGRA39 / GRACoL), el sustrato de papel y la maquinaria de impresión. Debe validarse rigurosamente mediante prueba de color física antes de autorizar cualquier tiraje comercial.

### Escalas de luminosidad

| Nivel | `brand-primary` (Rojo) | `neutro` (Gris Técnico / Carbón) |
|---|---|---|
| **50** | `#FEE2E2` | `#FAFAFA` |
| **100** | `#FECACA` | `#F5F5F5` (Usado como `text-strong` en temas oscuros) |
| **200** | `#FCA5A5` | `#E5E5E5` |
| **300** | `#F87171` | `#D4D4D4` |
| **400** | `#EF4444` | `#A3A3A3` (Usado como `text-muted`) |
| **500** | `#E50914` (Primario base) | `#737373` |
| **600** | `#B8000A` (Primario texto) | `#525252` |
| **700** | `#8F0007` | `#404040` |
| **800** | `#6B0005` | `#2E2E2E` (Usado como `border`) |
| **900** | `#450003` | `#171717` (Usado como `surface`) |
| **950** | `#260002` | `#0D0D0D` (Usado como `bg`) |

---

## D05 · Matriz de contraste verificada

| Primer Plano (FG) | Fondo (BG) | Ratio Calculado | Cumplimiento WCAG | Aplicación Autorizada |
|---|---|---|---|---|
| `text-strong` (`#F5F5F5`) | `bg` (`#0D0D0D`) | **17.82:1** | AAA | Titulares, textos de cuerpo, lectura continua. |
| `text-strong` (`#F5F5F5`) | `surface` (`#171717`) | **15.42:1** | AAA | Bloques de tarjeta, paneles y módulos. |
| `text-strong` (`#F5F5F5`) | `surface-alt` (`#212121`) | **13.41:1** | AAA | Secciones alternas y barras de control. |
| `text-muted` (`#A3A3A3`) | `bg` (`#0D0D0D`) | **7.51:1** | AAA | Subtítulos, metadatos y notas secundarias. |
| `text-muted` (`#A3A3A3`) | `surface` (`#171717`) | **6.50:1** | AA | Descripciones breves en tarjetas. |
| `text-on-brand` (`#FFFFFF`) | `brand-primary` (`#E50914`) | **4.81:1** | AA | Texto de botones primarios y banners de impacto. |
| `brand-primary-text` (