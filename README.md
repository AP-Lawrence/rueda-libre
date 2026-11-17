#  Rueda Libre v2.0 — Alquiler de bicicletas y rutas en Medellín

Sitio web responsivo y accesible para **Rueda Libre**, servicio de alquiler de bicicletas urbanas, de montaña y eléctricas, además de recorridos guiados por Medellín.

 **Demo en vivo (GitHub Pages):** [https://ap-lawrence.github.io/rueda-libre/](https://ap-lawrence.github.io/rueda-libre/)

---

##  Evolución del proyecto

### Semana 1 — Rueda Libre v1.0 (HTML5 Semántico, Accesibilidad y CSS Base)
- **Estructura semántica:** Maquetación de las 3 páginas (`index.html`, `paginas/tarifas.html`, `paginas/reservas.html`) con `header`, `nav`, `main`, `section`, `article`, `aside` y `footer`.
- **Tablas y formularios con validación nativa:** Tablas accesibles con `caption` y `scope`; formulario con validaciones HTML5 (`required`, `pattern`, `minlength`, `maxlength`, `min`, `max`).
- **Identidad visual y WCAG AA:** Variables CSS (`:root`), paleta con contraste verificado (Verde Ruta `#1e7a4f`, Naranja Pedal `#F39A2B`, Azul Noche `#14213D`, Crema `#FAF6EF`), modelo de caja `border-box`, etiqueta absoluta `Nuevo` y botón flotante de WhatsApp.

### Semana 2 — De v1.5 (Responsive CSS Propio) a v2.0 (Bootstrap 5 Personalizado)
- **Fase 1 (MiniRetos 1–4 | Rueda Libre v1.5):** Diseño *mobile-first* con Flexbox (encabezado, menú, pie y campos cortos), CSS Grid (`auto-fit minmax` en la flota de 7 bicicletas, galería de rutas y layout 2:1 en reservas) y Media Queries para `768px` y `1200px`.
- **Fase 2 (MiniRetos 5–8 | Rueda Libre v2.0-beta):** Prototipado en `pruebas/catalogo-bootstrap.html` y migración completa de las 3 páginas al sistema de grilla (`container`, `row`, `col-*`) y utilidades de Bootstrap 5, reduciendo `css/styles.css` en un **55.3%** (de 392 a 175 líneas).
- **Fase 3 (MiniRetos 9–12 | Rueda Libre v2.0):**
  - **Navbar y botones:** Menú colapsable (`navbar-expand-lg`) con soporte de teclado y llamadas a la acción unificadas (`.btn-primary`, `.btn-outline-primary`, `.btn-pedal`).
  - **Cards y Carrusel:** Flota de 7 bicicletas y galería de 3 rutas convertidas a `.card.h-100`; carrusel automático (`#carruselPromociones`) con las 3 promociones del mes y controles accesibles (`.visually-hidden`).
  - **Reservas interactivas:** Validación visual de Bootstrap (`.needs-validation` + `.invalid-feedback` específicos), alerta descartable (`.alert-dismissible`) y ventana modal (`#modalPoliticas`) con las 5 políticas de alquiler.
  - **Identidad de marca e íconos:** Sobrescritura limpia de variables `--bs-*` y `--bs-btn-*` sin `!important`, 3 clases complementarias (`.portada-hero`, `.titulo-seccion`, `.pie-marca`) e integración de **Bootstrap Icons** con atributos `aria-hidden` y `aria-label`.

---

##  Estructura del repositorio

```text
rueda-libre/
├── index.html                        # Página de inicio (Navbar, Hero, Carrusel, Flota y Rutas en Cards, Beneficios)
├── README.md                         # Documentación general del proyecto
├── bitacora.txt                      # Registro técnico de decisiones, pruebas, comparativas y resolución de conflictos
├── css/
│   └── styles.css                    # Personalización de variables Bootstrap (--bs-*), clases propias y tablas
├── img/
│   ├── portada.jpeg                  # Imagen hero y promoción 1
│   ├── bici.jpeg                     # Imagen de flota y promoción 2
│   ├── ruta.jpeg                     # Imagen de rutas y promoción 3
│   └── capturas/                     # Capturas comparativas antes y después de personalizar Bootstrap
├── paginas/
│   ├── tarifas.html                  # Tablas de alquiler y recorridos en grilla 8/4 desde lg
│   └── reservas.html                 # Formulario con validación visual, alerta descartable y modal de políticas
└── pruebas/
    └── catalogo-bootstrap.html       # Entorno de prueba de grilla y utilidades (MiniRetos 5 y 6)