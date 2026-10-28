# GDD — SHIFTBOUND

## 0. Estado del documento

- **Decisiones definitivas**: mecánica central de posesión/SHIFT, perspectiva top-down, vertical slice único, IA basada en FSM + adaptación simple.
- **Hipótesis a validar temprano**: si la posesión se siente divertida en menos de 30 segundos; si la lectura visual de dos planos (digital/físico) es clara.
- **Ampliaciones opcionales**: tercer tipo de robot, mini-boss, mutadores de dificultad.

---

## 1) Brainstorming — 8 conceptos diferenciados

La lluvia de ideas completa se ha extraído a:

- `/home/runner/work/SHIFT/SHIFT/lluvia-de-ideas.md`

Resumen: se evaluaron 8 direcciones distintas y se eligió **Rogue Operator** por equilibrio entre originalidad, integración de SHIFT y viabilidad en 6 semanas.

## 2) Evaluación comparativa

| # | Concepto | Orig. | SHIFT | Diversión inmediata | Decisiones | Prototipo rápido | Viab. 6 sem. | Viab. 4 pers. | Demo 5 min | Teaser | IA natural | Total |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 1 | Overclock Drift | 7 | 9 | 8 | 6 | 5 | 5 | 5 | 8 | 9 | 6 | 68 |
| 2 | Polarity Cleric | 6 | 8 | 7 | 7 | 8 | 8 | 8 | 8 | 7 | 6 | 73 |
| 3 | Echo Persona | 8 | 8 | 6 | 8 | 5 | 5 | 6 | 6 | 7 | 8 | 67 |
| 4 | Rogue Operator | 9 | 9 | 8 | 8 | 7 | 8 | 8 | 9 | 9 | 9 | 84 |
| 5 | Shiftline Tactics | 8 | 8 | 5 | 9 | 4 | 4 | 5 | 6 | 7 | 8 | 64 |
| 6 | Key:SHIFT | 8 | 10 | 8 | 7 | 6 | 6 | 6 | 9 | 9 | 7 | 76 |
| 7 | Fracture Lens | 9 | 9 | 7 | 8 | 6 | 6 | 6 | 8 | 8 | 8 | 75 |
| 8 | Morph Siege | 7 | 8 | 8 | 7 | 7 | 7 | 7 | 8 | 8 | 8 | 75 |

### Lectura crítica
- **Rogue Operator** lidera por equilibrio entre originalidad, claridad temática y viabilidad real.
- **Key:SHIFT** es muy potente en pitch y teaser, pero más arriesgado en balance global de reglas.
- **Fracture Lens** es atractivo, pero la persistencia entre planos aumenta riesgo técnico.

### Top 3 y sacrificios
1. **Rogue Operator (ganador)**: sacrificamos parte de complejidad narrativa para asegurar loop jugable fuerte.
2. **Key:SHIFT**: sacrificaríamos robustez técnica por un gimmick muy vistoso.
3. **Fracture Lens**: sacrificaríamos velocidad de prototipado por diseño de puzle más complejo.

---

## 3) Propuesta ganadora — Rogue Operator

## A. Identidad del juego
- **Título**: SHIFTBOUND
- **Tagline**: *Hackea, posee y escapa.*
- **Pitch (1 frase)**: Eres un virus consciente que debe poseer robots y alternar entre plano digital y físico para escapar de una instalación que aprende de ti.
- **Descripción**: SHIFTBOUND combina infiltración táctica y acción top-down. El jugador alterna entre forma digital vulnerable y cuerpos robóticos con habilidades especializadas para superar defensas, rutas bloqueadas y enemigos reactivos. La IA del sistema identifica patrones repetidos y reorganiza patrullas, creando partidas cortas pero tensas.
- **Género**: action-stealth top-down.
- **Perspectiva/estilo**: vista cenital, estética sci-fi minimalista con alto contraste.
- **Público objetivo**: jugadores de acción táctica accesible (partidas de 5–10 min).
- **Emoción principal**: “ingenio bajo presión”.
- **Referencias**:
  1. **Heat Signature**: claridad táctica y decisiones rápidas. **No copiar** su escala sistémica masiva.
  2. **Carrion**: fantasía de entidad no humana. **No copiar** su progresión extensa/metroidvania.
  3. **Gunpoint**: resolución creativa de espacios. **No copiar** dependencia fuerte de texto/narrativa.

## B. Fantasía y experiencia
El jugador se siente una inteligencia invasora que improvisa: no “dispara más”, sino que **elige el cuerpo correcto en el momento correcto**. Rejugar resulta atractivo porque la IA cambia presión por zonas calientes y permite probar rutas, huéspedes y ritmos distintos.

## C. Mecánica central (SHIFT de cuerpo)
1. **Selección objetivo**: apuntado con ratón sobre robot dentro de rango de hackeo y línea de visión.
2. **Condición de activación**: recurso “señal” suficiente + objetivo no blindado + cooldown listo.
3. **Ejecución**: canal corto (0.4–0.8 s). Si se completa, control pasa al huésped.
4. **Cuerpo anterior**:
   - Si estabas en digital: permanece “anclaje” vulnerable en el punto de entrada.
   - Si estabas en robot: queda deshabilitado unos segundos antes de autodestruirse.
5. **Duración**: posesión estable pero drenando señal; al agotarse, expulsión automática.
6. **Límites**: cooldown global + coste creciente por posesiones consecutivas rápidas.
7. **Si el huésped se destruye**: expulsión inmediata a forma digital con breve aturdimiento.
8. **Recuperación de recursos**: nodos de datos, eliminación sigilosa, tiempo sin ser detectado.
9. **Antiabuso**: IA eleva seguridad en zonas de posesión repetida + enemigos con blindaje parcial.
10. **Decisiones emergentes**: ¿usar tanque para abrir paso o dron para hackear sin ruido?

## D. Bucle de gameplay
- **Bucle corto (segundos)**: observar patrulla → hacer SHIFT → ejecutar ventaja → reposicionarse.
- **Bucle de encuentro (1 sala)**: analizar layout → elegir ruta/cuerpo → resolver alarma/combate → abrir siguiente acceso.
- **Bucle de partida**: infiltración por sectores → escalar seguridad → alcanzar núcleo → extracción.
- **Objetivo final**: activar terminal de escape y salir del perímetro.
- **Victoria**: escapar con núcleo infectado.
- **Derrota**: destrucción en forma digital o nivel de alerta máximo sostenido.
- **Progresión**: micro-upgrades (más rango, menor coste, detección temporal de rutas).

**Secuencia ejemplo**: dron patrulla bloquea puerta. Entras en forma digital por conducto, posees dron para abrir acceso, abandonas antes de cruzarte con torreta, posees guardia pesado para absorber fuego y activar interruptor final bajo alarma.

## E. Nivel de demostración (vertical slice)
- **Distribución**: 3 zonas lineales con rutas laterales cortas (Acceso → Seguridad → Núcleo).
- **Objetivo**: infectar núcleo y extraerse por compuerta secundaria.
- **Obstáculos**: torretas, puertas por credencial, campos antivirus.
- **Enemigos**: dron ligero, guardia estándar, guardia blindado.
- **Interactivos**: paneles, nodos de datos, coberturas, conductos digitales.
- **Decisiones**: ruta rápida arriesgada vs ruta larga con más recursos.
- **Clímax**: sala del núcleo con escalada de IA (bloqueo dinámico de flancos).
- **Resolución**: escape contrarreloj de 45–60 s.

## F. Inteligencia artificial
### F.1 Navegación y persecución
- NavMesh/AStar de Godot para unidades físicas.
- Grafo de patrulla por waypoints con prioridades.

### F.2 Combate / decisión
- **FSM por enemigo**: Patrol → Suspicious → Chase → Search → Return.
- Variables: visión, ruido, último avistamiento, cercanía a objetivos críticos.

### F.3 Adaptación al jugador (sin ML)
- Sistema de “heat zones”: el juego registra zonas con posesiones/repeticiones frecuentes.
- Al superar umbral: más revisitas de patrulla, torretas temporales activadas y mayor tiempo en estado Search.
- Adaptación transparente: feedback visual en minimapa/luces para evitar sensación injusta.

### F.4 Anti-frustración
- Límites de adaptación por sector (cap de dificultad).
- Ventanas de recuperación (baja de presión tras buen sigilo).
- Reglas consistentes y comunicadas (iconos de alerta y rutas reforzadas).

## G. Dirección artística y sonido
- **Paleta**: cian/magenta para plano digital, gris/ámbar para físico.
- **Siluetas**: formas muy distintas por tipo de robot (ligero, estándar, blindado).
- **FX SHIFT**: glitch radial breve + estela de datos.
- **Animaciones prioritarias**: posesión, expulsión, detección, alarma.
- **SFX**: pulso digital, confirmación de hackeo, ruido de alerta escalable.
- **Música**: base ambiental + capas percusivas en alerta.
- **Feedback crítico**: retícula cambia color por validez de posesión; barra de señal visible.

## H. Controles e interfaz (PC)
- **Movimiento**: WASD
- **Apuntar**: ratón
- **Acción/ataque**: clic izquierdo
- **SHIFT/poseer**: clic derecho (mantener para canalizar)
- **Interacción paneles**: E
- **Impulso/evade**: Shift teclado (si no colisiona con accesibilidad)
- **UI mínima**: salud huésped, señal, cooldown SHIFT, nivel alerta, objetivo actual.

## I. Arquitectura técnica (Godot)
### Escenas principales
- `Main.tscn`: bootstrap y managers globales.
- `Level_VS1.tscn`: layout vertical slice.
- `PlayerDigital.tscn`: control en forma digital.
- `HostRobot_*.tscn`: variantes de robots poseíbles.
- `EnemyAI.tscn`: enemigos no poseíbles.
- `UI_HUD.tscn`: HUD y estados.

### Sistemas
- `ShiftSystem.gd`: validación de objetivos, coste, cooldown, transferencia de control.
- `AISystem.gd`: FSM + heat zones.
- `AlertSystem.gd`: nivel global de alerta y eventos.
- `SignalSystem.gd`: recurso de posesión.

### Estados y comunicación
- Señales: `shift_started`, `shift_completed`, `host_destroyed`, `alert_changed`.
- FSM desacoplada por componente (`AIStateMachine.gd` + estados por script).

### Carpetas
- `/scenes`, `/scripts`, `/ai`, `/systems`, `/ui`, `/audio`, `/art`, `/levels`.

### Riesgos técnicos
1. Transferencia limpia de control entre cuerpos.
2. Consistencia de colisiones/cámaras en cada huésped.
3. Legibilidad de plano digital vs físico.

### Pseudocódigo orientativo
```text
if can_shift(target):
  consume_signal(cost)
  emit shift_started
  if channel_success:
    transfer_control(player, target)
    start_cooldown()
    emit shift_completed
```

---

## 4) Alcance y priorización

### MUST HAVE
- SHIFT digital↔huésped funcional.
- 2 tipos de huésped con habilidades distintas.
- IA FSM (patrulla/alerta/búsqueda).
- 1 vertical slice completo con victoria/derrota.
- HUD con señal, cooldown y alerta.

### SHOULD HAVE
- Adaptación por heat zones.
- Ruta alternativa en nivel.
- Teaser capturado in-engine con overlay mínimo.

### COULD HAVE
- Tercer huésped.
- Evento mini-boss final.
- Mutador opcional de dificultad.

### Si hay retraso, recortar primero
1. Tercer huésped (si existiera).
2. Complejidad de rutas secundarias.
3. Adaptación avanzada (mantener FSM base).

---

## 5) Planificación realista (6 nov → 18 dic)

## Semana 1 (6–12 nov)
- **Entregables**: GDD cerrado, arquitectura base, graybox del nivel.
- **Dependencias**: definición exacta de SHIFT.
- **Riesgos**: scope creep.
- **Done**: documento aprobado + escena jugable vacía con movimiento.

## Semana 2 (13–19 nov)
- **Entregables**: SHIFT básico, posesión de 1 huésped, IA patrulla.
- **Riesgos**: bugs de transferencia de control.
- **Done**: loop mínimo “poseer y avanzar”.

## Semana 3 (20–26 nov)
- **Entregables**: segundo huésped, alerta global, UI base.
- **Riesgos**: UX confusa.
- **Done**: partida completa de inicio a fin sin pulido.

## Semana 4 (27 nov–4 dic) — Hito prototipo
- **Entregables**: vertical slice funcional + IA búsqueda + audio base.
- **Riesgos**: estabilidad.
- **Done hito 4 dic**: demo jugable 4–7 min repetible.

## Semana 5 (5–11 dic)
- **Entregables**: pulido de controles, legibilidad, balance, captura teaser.
- **Riesgos**: sobrepulido visual.
- **Done**: build estable para ensayo de presentación.

## Semana 6 (12–18 dic) — Presentación
- **Entregables**: teaser final, guion 5 min, plan B de demo.
- **Riesgos**: fallo técnico en directo.
- **Done hito 18 dic**: presentación ensayada y demo robusta.

### Distribución de responsabilidades (4 personas)
1. **Gameplay & controles**: movimiento, combate/interacción, sensación de juego.
2. **IA & sistemas**: FSM, alertas, heat zones, balance de presión.
3. **Nivel & diseño**: graybox, pacing del vertical slice, test de decisiones.
4. **Arte/UI/audio & build**: legibilidad visual, HUD, sonido, capturas teaser, integración final.

### Prototipo de riesgo (primeros días)
Objetivo: validar en 48–72 h si “poseer y abandonar cuerpo” es divertido.
- Escena mínima con 1 pasillo, 1 dron, 1 puerta bloqueada.
- Métrica cualitativa: ¿en 30–60 s el jugador entiende por qué poseer es interesante?

---

## 6) Presentación de 5 minutos

### Guion
1. **Hook (10 s)**: “¿Y si para escapar tu mejor arma fuera robar el cuerpo del enemigo?”
2. **Premisa (30 s)**: virus consciente atrapado en instalación adaptable.
3. **Mecánica SHIFT (45 s)**: digital↔huésped, coste y riesgo.
4. **Gameplay clave (2 min)**: secuencia de posesión encadenada con respuesta de IA.
5. **IA e impacto (45 s)**: cómo el sistema cambia patrullas según decisiones del jugador.
6. **Cierre (30 s)**: valor diferencial + estado del proyecto.

### Teaser breve (20–35 s)
- Plano 1: infiltración digital silenciosa.
- Plano 2: posesión explosiva de guardia.
- Plano 3: clímax con alerta y escape.
- Texto final: “SHIFTBOUND — Hackea. Posee. Escapa.”

### Momento “quiero probarlo”
Cadena rápida de 2 posesiones en sala final para convertir una situación perdida en escape exitoso.

### Plan alternativo demo
- Build backup local + video de respaldo de 90 s.
- Ruta de demostración fija ensayada (sin depender de RNG).
- Si falla input/PC: reproducir video y narrar decisiones clave.

---

## 7) Criterios de aceptación del diseño
- SHIFT es obligatorio y comprensible en menos de 2 minutos.
- El vertical slice ofrece decisiones tácticas reales (no solo reflejos).
- La IA muestra al menos 2 cambios de comportamiento observables por partida.
- La demo de 5 minutos es repetible sin depender de contenido no implementado.
- El alcance queda dentro de MUST HAVE antes de añadir extras.
