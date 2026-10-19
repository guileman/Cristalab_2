# Cristales VR

Simulador de realidad virtual (WebXR, Meta Quest 2) para ver y manipular redes cristalinas metálicas y sus defectos.

- **Redes:** cúbica simple (CS), BCC, FCC y HCP.
- **Defectos:** vacancias (con salto difusivo y par de Frenkel), intersticiales (sitios octaédricos y tetraédricos), sustitucionales (soluto grande/chico), dislocación de borde, dislocación de tornillo (en FCC, disociables en parciales de Shockley con falla de apilamiento), maclas (crecimiento capa por capa bajo corte) y límites de grano de inclinación (bajo y alto ángulo).
- **Esfuerzo de corte τ:** por debajo de τc solo hay deformación elástica; por encima la dislocación se desliza por los valles de Peierls y al salir del cristal deja un escalón de tamaño b. Cada red tiene su τc y su τ de maclado.

Todo está en `index.html` (Three.js 0.169 desde jsDelivr). Sin build ni dependencias.

## Publicar

1. Subí estos archivos a un repo de GitHub (rama `main`).
2. En **Settings → Pages**, elegí como fuente **GitHub Actions**.
3. Cada push a `main` publica el sitio. Abrí la URL en el navegador de la Quest y tocá **ENTER VR**.

## Controles en la Quest

| Mando | Acción |
|---|---|
| Gatillo | Botones del menú, barra de τ (sostenido), acción sobre átomos |
| Agarre | Agarrar la red; con las dos manos: girar y escalar |
| Stick derecho ↕ | Esfuerzo de corte τ (o ángulo θ en límite de grano, o escala) |
| Stick izquierdo / derecho ↔ | Girar la red |
| A | Acción del defecto (salto de vacancia, salto intersticial, parciales, ángulo típico…) |
| B | Reiniciar defecto |
| X | Átomos reducidos / compactos |
| Y | Mostrar u ocultar guías y planos |

## Controles en PC

Clic para capturar el mouse · Clic izq.: menú / átomos · Clic der. sostenido: agarrar la red · Rueda: escala · WASD: caminar · ↑↓: τ o θ · Q/E, ←/→, R/F: girar · Espacio: acción · B: reiniciar · Tab: siguiente defecto · 1-4: tipo de red · T, G, I, O, P, C, F, J, H, M: opciones del menú.
