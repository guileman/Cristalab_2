# CristaLab

Simulador de realidad virtual (WebXR, Meta Quest 2) de la UTN FRSN para ver y manipular redes cristalinas metálicas y sus defectos.

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
| Y | Recorrer los planos principales de la red (red perfecta, vacancia, intersticial, sustitucional) |

## Controles en PC

Clic para capturar el mouse · Clic izq.: menú / átomos · Clic der. sostenido: agarrar la red · Rueda: escala · WASD: caminar · ↑↓: τ o θ · Q/E, ←/→, R/F: girar · Espacio: acción · B: reiniciar · Tab: siguiente defecto · 1-4: tipo de red · G: planos principales · T, I, O, P, C, F, E, J, H, M: opciones del menú · Z: resetear todo · Esc: salir.

## Menú

Encabezado con el nombre de la aplicación y el logo de la facultad; secciones **Red cristalina**, **Defecto**, **Opciones** y **Sistema** (recentrar red, resetear todo, controles, sonido y **Salir**).

**Planos principales:** en red perfecta, vacancia, intersticial y sustitucional, el botón recorre los planos más importantes de cada red (CS/BCC/FCC: (100), (110), (111); HCP: basal, prismático y piramidal). Marca el plano que pasa por el centro, colorea las capas según su apilamiento (A, B, C…) y muestra la distancia interplanar y la densidad plana, indicando cuál es el plano más compacto.

## Logo

Para incluir el logo, pegá la imagen como data URI en la constante `LOGO_URI` de `index.html`. Si queda vacía se muestra la sigla "UTN FRSN" como texto.
