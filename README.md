# 🏎️ Carreritas 3D

Mini juego de carreras 3D en el navegador. **Three.js puro, sin build tools.**

Modelos de carros cortesía de [codimexa.com](https://codimexa.com/demos/lancer/) (Lancer Evo, Supra MK4, GT-R R35, Mustang GT).

## 🎮 Cómo jugar

1. **Elige tu carro** — cada uno tiene stats diferentes (velocidad, aceleración, manejo)
2. **Acelera, gira, da drift** con el handbrake
3. **Completa 3 vueltas** lo más rápido posible
4. **Mejor tiempo** se guarda en `localStorage`

## 🎯 Controles

### Teclado
- `W` / `↑` — Acelerar
- `S` / `↓` — Frenar / reversa
- `A` / `←` — Girar izquierda
- `D` / `→` — Girar derecha
- `Espacio` — Handbrake (drift)

### Mobile (touch)
- Botones en pantalla (auto-detect)

## 🚗 Los carros

| Carro | Velocidad | Aceleración | Manejo | Estilo |
|---|---|---|---|---|
| Lancer Evo | 200 | 1.0 | 0.95 | Balance total |
| Supra MK4 | 220 | 0.95 | 0.85 | Velocidad pura |
| GT-R R35 | 230 | 1.05 | 1.0 | Tracción total |
| Mustang GT | 215 | 1.1 | 0.78 | Muscle, drifts largos |

## ✨ Características

- **4 carros 3D** (.glb) con stats diferenciados
- **Pista cerrada** con curvas, chicanes, curvas suaves
- **Sistema de checkpoints** invisible + validación de vuelta
- **Física arcade** con aceleración, fricción, drift con handbrake
- **Cámara chase** que sigue al carro con suavizado
- **Minimapa** con posición y dirección del carro
- **3 vueltas cronometradas** + high score persistente
- **Controles touch** para mobile
- **Skybox procedural**, montañas, árboles, barreras

## 🛠️ Stack

- **Three.js 0.160** vía CDN (importmap)
- **GLTFLoader** para los modelos .glb
- **HTML5 Canvas** para minimapa
- **CSS3** para UI
- **0 dependencias npm**

## 🚀 Demo

👉 [aguitech.github.io/carreritas3d](https://aguitech.github.io/carreritas3d/)

## 📂 Estructura

```
carreritas3d/
├── index.html          # Layout + HUD + screens
├── styles.css          # Estilos
├── game.js             # Motor del juego
├── favicon.svg
├── README.md
└── cars/
    ├── lancer.glb      # 3.9 MB (optimizado)
    ├── supra.glb       # 7.3 MB
    ├── gtr.glb         # 8.7 MB
    └── mustang.glb     # 2.0 MB
```

Total assets: **~22 MB** (los .glb originales pesaban 105 MB; fueron optimizados con gltf-transform).

## 🏃 Desarrollo local

```bash
git clone https://github.com/aguitech/carreritas3d.git
cd carreritas3d
# Necesitas un servidor estático (los .glb no cargan con file://)
python3 -m http.server 8000
# Abre http://localhost:8000
```

## 📜 Créditos

- Modelos 3D: [codimexa.com/demos/lancer](https://codimexa.com/demos/lancer/) (descargados, optimizados y reutilizados con fines educativos/demostrativos)
- Three.js: [threejs.org](https://threejs.org/)
- Optimización: [@gltf-transform/cli](https://gltf-transform.dev/)

## ⚖️ Licencia

MIT — Hecho con 💜 para la cultura racing.

---

**🏁 ¡A correr!**
