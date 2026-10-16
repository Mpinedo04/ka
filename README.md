# Transcripción MIDI de piano: «Sogni appesi» (Ultimo)

Fuente: `Sogni appesi Ultimo Karaoke version UltraHD Instrumental.wav` (3:37, 48 kHz, 16 bit, estéreo).

## Actualización: dos versiones nuevas

| Archivo | Qué es |
|---|---|
| **`Sogni_appesi_piano_64bpm_pedal_corregido.mid`** | **Sustituye al archivo principal.** Mismas notas y velocidades que la transcripción, con el pedal y las duraciones corregidos. |
| **`Sogni_appesi_piano_version_mejorada.mid`** | Mi versión arreglada. Es una interpretación propia: se aparta de la grabación a propósito. |

La versión anterior con pedal tenía 16 huecos de silencio (5,9 s en total) en momentos en que el original seguía sonando, y 15 de sus 50 notas agudas sonaban menos de medio segundo. El archivo `..._sin_pedal.mid` arrastra el mismo problema, porque sus duraciones salían de aquel pedal.

### Pedal corregido: qué ha cambiado
- **Pedal legato por acorde.** El pedal se levanta justo al entrar un bajo o un acorde nuevo y se vuelve a pisar 0,1 s después. Así no se corta nada entre acordes y tampoco se mezclan armonías.
- **Cambio de pedal en cada acorde re-atacado** (3 notas o más). El acorde nuevo ya está sonando cuando se levanta el pedal, así que no aparecen silencios.
- **Al cambiar de acorde se sueltan las notas del acorde anterior**, salvo las comunes a los dos. Afectó a 19 notas que la transcripción dejaba pulsadas de más y que, con pedal, se arrastraban sobre la armonía siguiente.
- **Duración mínima de tecla de 0,15 s**, para que ninguna nota se pierda en un cambio de pedal.
- **Compases 48–50 (estribillo final):** ahí se mantiene el pedal anterior. En esos compases la versión anterior no tenía ningún problema y se parecía más al original, que suena más articulado.
- **Resultado:** 0 silencios, 0 notas agudas por debajo de 0,5 s y el mejor parecido espectral con el audio de todas las variantes (0,457, frente a 0,456 antes). Recuerda que esta comparación es por resíntesis; no he escuchado el resultado.

### Versión mejorada: mis decisiones
1. **Notas confirmadas por la repetición.** Añadí 10 notas del archivo de dudosas que aparecen en la misma posición en la mayoría de repeticiones del patrón, como el Fa#3 del c. 18 (presente en 5 de 5 repeticiones), el Fa#3 de los c. 26 y 28 o el La4 de los c. 10, 12 y 14.
2. **Notas graves aisladas eliminadas.** Quité 5 notas de baja confianza que no aparecen en ninguna repetición y que probablemente son armónicos (c. 33, 48, 49, 51 y 52).
3. **Octavas de la mano izquierda coherentes.** En las secciones donde el pianista toca el bajo en octavas (c. 18–33 y 38–53), añadí la octava superior en 7 bajos que no la tenían.
4. **Equilibrio de voces.** La voz superior (la melodía) sube unos +7 de velocidad y las voces interiores bajan −4, para que la melodía cante por encima del acompañamiento, ahora que no hay voz.
5. **Dinámica por secciones.** La dinámica transcrita se suavizó (sin picos sueltos) y se mezcló al 50 % con este arco:
   - introducción en mp-mf;
   - estrofas suaves;
   - crescendo en la subida y el puente (c. 41–45);
   - clímax en el estribillo final (c. 46–52);
   - final tranquilo con diminuendo.
   Encima van acentos métricos suaves: tiempo 1 +3, tiempo 3 +1 y corcheas a contratiempo −2.
6. **Legato.** Cada nota de la melodía se sostiene hasta la siguiente, y los bajos y las voces interiores hasta el cambio de acorde. Así la versión funciona bien incluso si quitas el pedal.
7. **Pedal legato.** En el estribillo final cambia en cada acorde re-atacado, para que el clímax suene claro.
8. **Final.** El último acorde (La add9) se deja sonar 6 tiempos, como un calderón.

No he añadido la melodía de la voz. No la puedo extraer de este audio y no quiero inventarla.

### Armonía (cifrado por secciones, tonalidad de La mayor)

| Compases | Sección | Acordes |
|---|---|---|
| 2–5 | Introducción | Fa#m – Mi – Re – La |
| 6–17 | Estrofa | \| Fa#m La \| Re \| (en bucle) |
| 18–25 | Estrofa grave | \| Fa#m La \| Re \|, bajo en octavas graves |
| 26–33 | Estribillo | \| Fa#m La \| Re Mi \| alternando con \| Fa#m La \| Re \| |
| 34–37 | Interludio | \| Fa#m La \| Re \| |
| 38–42 | Subida | \| Fa#m La \| Re \| |
| 43–45 | Puente | \| Mi Do#m \| Re Mi \| Do# \| |
| 46–53 | Estribillo final | \| Fa#m La \| Re Mi \|, bajo Fa#–Sol#–La en los c. 48 y 50 |
| 54–57 | Final | Fa#m – Mi – Re – La (add9), reprise de la introducción |

## Archivos de la primera versión

| Archivo | Qué es |
|---|---|
| **`Sogni_appesi_piano_64bpm.mid`** | **Archivo principal.** 564 notas en una sola pista de piano, cada una con su velocidad, más el pedal de sustain (CC64) estimado. 64 BPM, 4/4. |
| `Sogni_appesi_piano_64bpm_sin_pedal.mid` | Las mismas notas sin CC64. Cada nota dura lo que suena (tecla + pedal estimado). Útil si prefieres dibujar tu propio pedal. |
| `Sogni_appesi_notas_dudosas_NO_incluidas.mid` | 49 notas que algún modelo detectó pero que no pasaron la votación. **No forman parte de la transcripción.** Sirven para escucharlas en una pista aparte o silenciada y decidir. |

## Uso en la DAW

- Tempo fijo de **64 BPM** y compás de **4/4**. El compás 1 está vacío y la música empieza en el **compás 2, tiempo 1**.
- Para sincronizar con el WAV original: el compás 2 del MIDI corresponde al segundo **6,168** del WAV. Recorta **2,418 s** del principio del WAV y colócalo en el 0 del proyecto, o adelanta el WAV 2,418 s.
- Metadato de tonalidad: La mayor (progresión principal Fa#m – Mi – Re – La).

## Qué se ha hecho

1. **Inspección del audio.** El audio casi no tiene contenido por encima de unos 2,5 kHz (está muy filtrado). La zona de 160–640 Hz domina. Los canales L y R están poco correlados, con unos 11 ms de desfase. En cada pulso aparece un golpe grave no afinado, en torno a 70 Hz (la "resonancia" de graves).
2. **Tres sistemas de transcripción independientes**: Transkun v2, ByteDance (Kong et al., *High-resolution piano transcription*) y Aria-AMT. Cada uno se ejecutó sobre varias versiones del audio (estéreo, canal izquierdo, canal derecho y mezcla), lo que da 8 transcripciones.
3. **Calibración.** Hubo 105 s en los que los tres modelos funcionaban bien. Ahí Transkun y Aria coincidieron en el 91 % de las notas. En cambio, las notas que sólo detectaba ByteDance resultaron falsas en el 96 % de los casos: re-ataques inexistentes, armónicos y los golpes graves. Aria-AMT entraba en bucles en las estrofas suaves, así que en esas zonas no se usó su voto.
4. **Votación.** Una nota entra si la respaldan al menos dos de las tres familias de modelos. Así se recuperan octavas graves que Transkun confundía con armónicos (p. ej. Fa#2 + Fa#3).
5. **Revisión con espectrogramas** de la intro, las estrofas y el clímax. Se corrigió 1 nota omitida (Fa#3 re-atacado en el compás 21) y se eliminaron 2 notas falsas del bajo (Re1 y Re2) causadas por los golpes graves.
6. **Tempo.** El seguimiento de pulsos da **64,0 BPM estables** (entre 63,9 y 64,1 en cada compás), con una deriva de menos de 25 ms en toda la canción. El 93 % de los ataques cae a ±10 ms de la rejilla de corcheas (mediana: 2 ms), así que la parte de piano se grabó con claqueta o está secuenciada. Los ataques a 30 ms o menos de la rejilla (535 de 564) se alinearon a ella. Se conservaron las 16 notas con desviación expresiva (el rubato del final, compases 52–57). **Las duraciones no se han cuantizado.**
7. **Velocidades.** Los tres modelos estiman la velocidad de cada nota y sus estimaciones se parecen bastante (correlación 0,80–0,86). Se fusionaron en una escala común, con más peso para Transkun. El rango dinámico se amplió un 20 % porque, sin agudos, el audio comprime las pistas de dinámica. Resultado: 18–102, mediana 51, 70 valores distintos.
8. **Pedal.** En 38 momentos "limpios" en que se suelta una tecla se midió si el sonido se corta (pedal arriba) o sigue sonando (pedal abajo). Ningún modelo acierta más de un 65–70 % de esos casos. Transkun y Aria infravaloran mucho el pedal y ByteDance es el que mejor encaja. El pedal final combina por votación las tres entradas de ByteDance y se levanta siempre en cada cambio de acorde o de bajo, para no emborronar las armonías. Resultado: 145 pisadas, con el pedal abajo un 54 % del tiempo.
9. **Verificación del MIDI.** Se volvieron a leer los archivos generados: 0 notas duplicadas, 0 solapes de la misma tecla, tempo de 64 BPM y nota más larga de 6,7 s. Además se hizo una **comparación espectral por resíntesis**: el MIDI se resintetiza con un modelo de piano muy simple y se compara con el espectrograma original. La versión final obtiene 0,456, igual que Transkun solo (0,456) y por encima de ByteDance solo (0,416). Quitar el pedal o añadir las notas dudosas empeora el ajuste. **No es una escucha real: no he podido escuchar el resultado.**

## Limitaciones

- **Octavas graves de la mano izquierda.** Es la principal fuente de duda. El 2.º armónico de una nota grave coincide con su octava, y los modelos discrepan sobre si se toca Fa#2 solo o Fa#2 + Fa#3 (lo mismo pasa con La2/La3 y Re2/Re3). Se ha decidido por mayoría; la tabla de abajo indica dónde mirar.
- **El pedal es una estimación, no una medida.** Revísalo a oído. Para eso está la versión sin pedal.
- **Las velocidades son relativas.** Con un audio sin agudos y tan ecualizado no se pueden recuperar valores absolutos. Ajusta la curva de velocidad del plugin a tu gusto.
- **El final de cada nota es menos preciso que su ataque.** Es más fiable el tiempo total que suena cada nota (tecla + pedal) que el reparto exacto entre tecla y pedal.
- **No hay notas por encima de Si5.** Las líneas agudas del espectrograma son armónicos; el audio no tiene información útil por encima de unos 2,5 kHz.
- **Los golpes graves de cada pulso se han ignorado a propósito.** No son notas de piano.

## Dónde conviene revisar a oído

- **Compases 52–57 (3:11–3:36 del MIDI):** el final, tocado con rubato. Se ha mantenido el tiempo libre del pianista.
- **Compases 6–16 y 26–43:** concentran casi todas las decisiones dudosas. En gran parte de esas zonas sólo votaron dos modelos.
- Tabla de notas concretas (t. = tiempo dentro del compás):

| Compás | Tiempo en el MIDI | Incluidas por mayoría (menos seguras) | Plausibles NO incluidas (archivo de dudosas) |
|---|---|---|---|
| 6 | 0:18.8 | — | La2 (t.3), Fa#4 (t.1) |
| 7 | 0:22.5 | — | Mi4 (t.1) |
| 8 | 0:26.2 | — | Fa#4 (t.1) |
| 9 | 0:30.0 | Re4 (t.1) | La3 (t.1) |
| 10 | 0:33.8 | Do#5 (t.4) | La2 (t.3), Fa#4 (t.1), La4 (t.3) |
| 11 | 0:37.5 | — | La3 (t.3) |
| 12 | 0:41.2 | — | La4 (t.3) |
| 13 | 0:45.0 | — | La3 (t.2) |
| 14 | 0:48.8 | Do#5 (t.3) | La2 (t.3), La3 (t.2), La4 (t.3) |
| 15 | 0:52.5 | Re4 (t.1) | — |
| 16 | 0:56.2 | Mi4 (t.3) | La2 (t.3) |
| 18 | 1:03.8 | — | Fa#3 (t.1) |
| 20 | 1:11.2 | Fa#3 (t.1), Do#4 (t.1) | — |
| 21 | 1:15.0 | Fa#3 (t.1) | — |
| 22 | 1:18.8 | La3 (t.3), Do#4 (t.3) | — |
| 26 | 1:33.8 | Do#4 (t.1), Fa#4 (t.2) | Fa#3 (t.1), La3 (t.3), Mi5 (t.4) |
| 27 | 1:37.5 | Re4 (t.3) | La3 (t.2.5) |
| 28 | 1:41.2 | — | Fa#3 (t.1) |
| 29 | 1:45.0 | — | Re3 (t.2), Mi5 (t.3) |
| 30 | 1:48.8 | — | Sol#3 (t.2.5), Mi5 (t.4) |
| 31 | 1:52.5 | — | Re3 (t.1), Re3 (t.2) |
| 33 | 2:00.0 | Re3 (t.1), Re4 (t.3) | Re5 (t.4) |
| 34 | 2:03.8 | — | Do#5 (t.3), Mi5 (t.3) |
| 35 | 2:07.5 | La3 (t.1.5), Re3 (t.2) | — |
| 38 | 2:18.8 | La3 (t.3) | — |
| 39 | 2:22.5 | Re3 (t.1) | Re5 (t.1) |
| 40 | 2:26.2 | Fa#3 (t.1), La3 (t.1) | — |
| 41 | 2:30.0 | — | Re5 (t.2), Re5 (t.4), Fa#5 (t.4) |
| 42 | 2:33.8 | Do#4 (t.3) | Do#4 (t.4), La4 (t.3), Mi5 (t.3), Mi5 (t.4) |
| 43 | 2:37.5 | Si3 (t.1) | Si3 (t.1.5), Mi5 (t.1), Mi5 (t.2), Mi5 (t.3), Mi5 (t.4) |
| 47 | 2:52.5 | La4 (t.2.5), Mi4 (t.3) | — |
| 48 | 2:56.2 | La2 (t.4.5) | — |
| 49 | 3:00.0 | Fa#3 (t.1.5) | Mi4 (t.4.5), La4 (t.2), La4 (t.4) |
| 51 | 3:07.5 | La3 (t.1) | — |
| 52 | 3:11.2 | La3 (t.1), Fa#3 (t.1.5), Mi5 (t.3) | — |
| 53 | 3:15.0 | — | Mi4 (t.1) |
| 54 | 3:18.8 | — | Mi6 (t.2) |
| 56 | 3:26.2 | Fa#5 (t.2.5) | La4 (t.1) |
