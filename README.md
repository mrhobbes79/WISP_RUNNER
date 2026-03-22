# 🗼 WISP Runner 2 — Build the Network. Conquer the City.

**WISP Runner 2** es un juego isométrico de estrategia-acción donde juegas como un técnico WISP instalando antenas en azoteas reales a lo largo de 10 ciudades en América Latina y Estados Unidos.

Está diseñado como una carta de amor a la industria de fixed wireless — y como una herramienta divertida para **WISPs, asociaciones y ferias** (WISPA, WISPMX, ABRINT y más).

- 🎮 **Juego 100% en el navegador** — un solo archivo HTML, sin dependencias
- 🌎 **10 ciudades reales · 30 niveles** con landmarks icónicos
- 📡 **Conceptos RF reales** (dBm, señal, clima, interferencia)
- 🌐 **Trilingüe**: Español / English / Português
- 🏢 **Perfecto para stands de feria y páginas de ISP**

---

## 🎮 Cómo jugar

1. Descarga o clona el repositorio.
2. Abre `wisp_runner_2.html` en cualquier navegador moderno.
3. Listo — no se requiere instalación, servidor ni dependencias.

### Controles

- **Flechas**: Mover al técnico
- **Space**: Subir/bajar, instalar antena, interactuar
- **Q / E**: Rotar la cámara
- **H**: Mostrar ayuda en pantalla
- **P / ESC**: Pausa
- **L**: Cambiar idioma (EN / ES / PT)

---

## 🌎 Ciudades y progresión

WISP Runner 2 recorre 10 ciudades reales, cada una con 3 niveles y retos distintos:

1. Monterrey, México 🏔️ Cerro de la Silla · Faro del Comercio  
2. Ciudad de México, México 🌆 Torre Latinoamericana  
3. Guadalajara, México ⛪ Centro histórico y hubs tech  
4. Rio de Janeiro, Brasil 🗿 Cristo Redentor · playa y morros  
5. São Paulo, Brasil 🏙️ Skyline denso y helicópteros  
6. Dallas, Texas, USA 🗼 Reunion Tower · suburbios  
7. Bogotá, Colombia ⛰️ Andes y altura  
8. Buenos Aires, Argentina 🗽 Obelisco · La Boca  
9. Miami, Florida, USA 🌴 Art Deco · huracanes  
10. Grand Finale 🌎 Conecta toda la red

Cada ciudad incrementa la dificultad con:
- Más interferencia
- Clima más agresivo
- Competidores más rápidos y agresivos

---

## 📡 Fixed Wireless convertido en juego

WISP Runner 2 convierte el trabajo diario de un técnico WISP en un juego arcade:

- **Alineación de antenas**  
  Mini-juego de azimuth/elevación con feedback de señal (dBm, barras de intensidad).
- **Clima dinámico**  
  Lluvia, viento, tormentas eléctricas y olas de calor impactan la señal.
- **Competidores**  
  Vans de cable, cuadrillas de fibra y jammers de interferencia pelean por las azoteas.
- **Progresión de carrera**  
  De Técnico Jr a Senior, Ingeniero RF y finalmente dueño del WISP.

Todo con un tono ligero, humor y muchos guiños a la comunidad WISP.

---

## 🧩 Pensado para stands de feria y páginas de ISP

WISP Runner 2 está diseñado para ser:

- **Fácil de desplegar**
  - Un solo archivo `wisp_runner_2.html`.
  - Se puede hostear en cualquier web estática.
  - Funciona offline una vez cargado.

- **Ideal para stands en eventos**
  - Se puede poner en modo “kiosk” (demo) para pantallas de stands.
  - Loop de juego corto (sesiones de 3–5 minutos).
  - Excelente para:
    - WISPA
    - WISPMX
    - ABRINT
    - Eventos regionales WISP

- **Personalizable para tu ISP** (v2+)
  - Colores y branding configurables.
  - Mensajes de “Powered by <tu ISP>”.
  - Hooks opcionales de telemetría.

---

## ⚙️ Roadmap WISP Runner 2 — Versión 2.0

WISP Runner 2 ya es totalmente jugable, pero el foco de la versión 2.0 es dejarlo **listo para evento/feria**.

### 1. Mejor onboarding y tutorial

- [ ] Menú principal con:
  - [ ] **Play**
  - [ ] **Controles**
  - [ ] **Idioma** (EN/ES/PT)
- [ ] Pantalla clara de controles con iconos/teclas.
- [ ] Nivel 0 de entrenamiento:
  - Un solo edificio y antena.
  - Mensajes guiados (“acércate”, “sube”, “instala”, “alinea”).
  - Difícil perder; diseñado para explicar.

### 2. Curva de dificultad y balance

- [ ] Tabla de parámetros por ciudad:
  - Velocidad de competidores.
  - Frecuencia de clima.
  - Tolerancia de error en alineación.
- [ ] Modo “Training”:
  - Más tiempo para alinear.
  - Menos castigo por fallar.
  - Feedback más explícito de señal.
- [ ] Barra de señal más clara:
  - Colores (rojo/amarillo/verde).
  - Mensajes tipo “Señal perfecta / aceptable / mala”.

### 3. Modo stand / demo (kiosk)

- [ ] Modo “kiosk/demo” (activable vía configuración o query string):
  - Auto-demo cuando no hay input por X segundos.
  - Auto-reset tras inactividad prolongada.
  - Mensajes tipo “Presiona cualquier tecla para jugar”.
- [ ] Atract mode:
  - Animaciones ligeras en menú.
  - Posible mini-replay de un run grabado.

### 4. Branding para ISPs y asociaciones

- [ ] Objeto `ISP_CONFIG` con:
  - Nombre del ISP/asociación.
  - Slogan corto.
  - Colores primario/acento.
  - Logo (opcional).
- [ ] UI usa estos colores y textos:
  - HUD, menús, barra de señal.
  - “Powered by <ISP>” en footer.
- [ ] Pantallas finales personalizables:
  - Mensaje de agradecimiento.
  - Llamado a acción (visitar web, escanear QR, etc.).

### 5. Telemetría ligera (opt-in)

- [ ] Almacenar en `localStorage`:
  - Nivel máximo alcanzado.
  - Tiempo total jugado.
  - Idioma elegido.
- [ ] Hook opcional de analytics:
  - Función `reportTelemetry(eventName, data)` que se puede conectar a un endpoint HTTP si el ISP lo desea.
  - Eventos recomendados:
    - `level_completed`
    - `city_unlocked`
    - `game_over`
    - `session_started` / `session_ended`

---

## 🧱 Stack técnico

- **Single HTML file** (`wisp_runner_2.html`)
- **HTML5 Canvas** + JavaScript (ES6+)
- **Web Audio API** (audio sintetizado, sin archivos externos)
- Funciona en cualquier navegador moderno de escritorio
- Sin dependencias ni build-step

---

## ❤️ Comunidad

WISP Runner 2 fue creado como un homenaje a la industria WISP y sus comunidades:

- [WISPA](https://www.wispa.org) — Wireless Internet Service Providers Association  
- [WISPMX](https://wisp.mx) — Comunidad WISP México  
- [ABRINT](https://abrint.com.br) — Associação Brasileira de Provedores de Internet  

Si eres parte de un WISP o asociación y quieres:
- Integrar el juego en tu sitio web,
- Usarlo en un stand de feria,
- O personalizarlo con tu branding,

puedes abrir un issue en este repo o contactar a los maintainers.

---

## 📄 Licencia

MIT — Juega, comparte, fórralo con tu branding (con créditos), y úsalo en tantos stands como quieras.

---

_© 2026 WISP Runner 2 | Hecho con ❤️ para WISPA, WISPMX, ABRINT y toda la comunidad WISP._
