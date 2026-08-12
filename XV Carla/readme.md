# Invitación Mis XV - Carla

Sitio web de invitación para los 15 de Carla. Web **estática** de una sola página (HTML + CSS + JS), con secciones a pantalla completa y estética *glassmorphism* / cuento de hadas. Lista para alojar en cualquier hosting y apuntarle un **dominio propio**.

---

## Estructura

```text
XV Carla/
├── readme.md               <- documentación
├── index.html              <- página completa (todas las secciones)
├── css/style.css           <- estilos de la página
├── fondo-cortinas.jpg      <- imagen de fondo (cortinas nude/beige con luces)
├── Veo en ti la luz.mp3    <- canción del reproductor
└── telas/                  <- texturas del dress code
    ├── 1.png               <- Champagne
    ├── 2.png               <- Rosa Dust
    └── 4.png               <- Tono XV
```

---

## Diseño

- **Fondo**: foto de cortinas de tela nude/beige con guirnaldas de luces cálidas, fija a pantalla completa (`background-attachment: fixed`).
- **Glassmorphism**: cada sección ocupa el 100% de la pantalla con el contenido centrado dentro de una **tarjeta de vidrio esmerilado** (blanco translúcido al 50% + blur), borde fino **oro rosa `#E0A899`** y sombra suave.
- **Tipografía**:
  - Títulos y nombres: caligráfica (*Pinyon Script*, *Great Vibes*).
  - Datos secundarios (dirección, horario, fecha, dress code): *Cinzel* en mayúsculas con espaciado amplio.
  - Frases y textos: *Cormorant Garamond* en cursiva.
- **Paleta de texto**: marrón cálido oscuro (`#4A2E2B` / `#5E3A35`), coordinada con los tonos nude del fondo.
- **Brillos de fondo**: `canvas` con partículas rosadas→blancas (estrellas y rombos) cayendo detrás de las tarjetas (`z-index: 1`), sin interferir con el texto.

---

## Secciones

| # | Sección | Contenido |
| :- | :--- | :--- |
| 1 | Portada | MIS XV · **Carla** + frase de bienvenida |
| 2 | Cuenta regresiva | Faltan **Días : Horas : Minutos** (sin segundos) → **20/11/2026 21:30** |
| 3 | La Fiesta | **Casa Praga** · Leandro N. Alem 345, Ramos Mejía (B1704) · 21:30 a 05:30 hs · botón **Ver Mapa** |
| 4 | Código de Vestimenta | **Etiqueta Elegante** · texturas en círculo reservadas para la quinceañera (Champagne, Rosa Dust, Tono XV) |
| 5 | Asistencia & Música | Formulario único (asistencia + restricciones alimentarias + sugerencia de canciones) |
| 6 | Nuestros Momentos | Álbum de fotos compartido |
| 7 | Sugerencia de Regalo | Alias **`holis.mi.sol`** en desplegable con botón **Copiar** + espacio para CBU/CVU |
| 8 | Cierre | Frase final + firma **Carla** |

**Reproductor de música**: botón flotante redondo (triángulo play → barras de pausa) que reproduce en loop la canción **"Veo en ti la luz"**.

---

## Vínculos

- Mapa (Google Maps): https://maps.app.goo.gl/P2sSq1vg4Mo1LZybA
- Álbum de fotos: https://photos.app.goo.gl/KrNS84Rc8kzWaV568
- Formulario (asistencia + comida + canciones): https://forms.gle/iZHhxgtPRguizocL7

---

## Probar localmente

```bash
cd "XV Carla"
python3 -m http.server 8000
```

Abrir `http://localhost:8000`.

---

## Publicar en dominio propio

1. Subí la carpeta completa (`index.html`, `css/`, `fondo-cortinas.jpg`, `Veo en ti la luz.mp3`, `telas/`) a cualquier hosting.
2. Apuntá el dominio en el hosting (o usá GitHub Pages / Netlify / Vercel con "custom domain" y HTTPS gratis).

---

## Pendientes / notas

1. **CBU / CVU**: completar el comentario `<!-- ... -->` dentro del desplegable de alias en `index.html`.
2. **Texturas**: verificar el orden en `telas/` (Champagne, Rosa Dust, Tono XV) — el modelo no pudo verlas al generarlas.
3. Fecha de la cuenta regresiva: cambiar en `index.html` (línea `const eventDate = new Date("2026-11-20T21:30:00")`) si corresponde.
4. Archivos sobrantes en la raíz que NO se usan y pueden borrarse: `fondo1.jpeg`, `fondomesa.jpg`, `fondox.jpg`, `fondox1.jpg`.