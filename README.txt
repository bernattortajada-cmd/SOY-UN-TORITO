GLASS PULSE — WebAR (Prototype)
=================================

Cómo usar
---------
1) Pon tus audios dentro de assets/ con estos nombres exactos:
   - glass_A_vocal_loop.mp3 (voz/textura)
   - glass_B_beat_loop.mp3 (beat/percusión)

2) Abre index.html **desde un servidor** (HTTPS o local). Por seguridad,
   los navegadores no activan la cámara si abres el archivo directo.
   Opciones simples:
   - Sube la carpeta a Netlify / Vercel / GitHub Pages
   - O en tu compu: usa "Live Server" de VS Code
   - O (si sabes) corre:  python3 -m http.server  (y abre http://localhost:8000)

3) Toca "Iniciar cámara".
   - Cierra los ojos → suena Audio A.
   - Abre la boca → suena Audio B.

Ajustes rápidos
---------------
- Sensibilidad ojos: busca `eyesClosedNow = eyesEMA > 0.62` en index.html
- Sensibilidad boca: `mouthOpenNow = mouthEMA > 0.28`
- Volúmenes: `audioA.volume` y `audioB.volume`

