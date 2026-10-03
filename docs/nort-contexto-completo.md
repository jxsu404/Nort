# Nort: contexto completo del proyecto

**Para qué sirve este documento:** reúne en un solo lugar todo lo que se ha decidido sobre Nort: el reto, el usuario, el concepto, la interfaz, el caso de prueba y lo que queda pendiente. Sirve para retomar el trabajo o para dárselo como contexto a otra persona o a otro asistente de IA.

**Estado:** todo es mockup e hipótesis. Nada está construido ni conectado de verdad a Google, Waze ni ningún otro servicio. Todos los datos de los mockups son de ejemplo.

---

## 1. El reto y el equipo

- **Competencia:** Reto iTEC 2026.
- **Equipo:** N.° 7, "Nort": Josu, Kendall y Esteban.
- **AP/zona:** Sebastián Torres.
- **Reto:** 1, "Cómo podríamos devolver el valor al tiempo".
- **Repositorio:** [jxsu404/Nort](https://github.com/jxsu404/Nort). En `main` solo hay un `README.md` vacío; el trabajo está en la rama `cursor/redaccion-empatia-nort-3a1e`. Todo lo de este documento está solo en local, sin commit ni push.
- **Regla de trabajo:** nada de programación real. Se perfecciona el documento (cuadernillo) y se diseñan mockups en HTML.

### El cuadernillo (7 entregables)

Archivo: `docs/cuadernillo-nort-redaccion-empatia.md`. Sigue el formato oficial de la plantilla del Reto iTEC.

| Entregable | Estado |
|---|---|
| E1. Mapa de experiencia y fricción | Completo |
| Respuestas obvias y supuestos | Completo |
| E2. Reformulación | Completo |
| E3. Contrato de hipótesis | Completo |
| E4. MVP v1 | Completo |
| Red Team, evidencia de E1 | Pendiente: solo con evidencia real |
| Preparación del Banco de Contraste | Completo |
| E5. Matriz de evidencia | Pendiente: solo con evidencia real |
| E6. De MVP v1 a MVP v2 | Pendiente: solo con evidencia real |
| E7. Pitch final (5 slides) | Completo salvo el Slide 4, que depende del Banco de Contraste |
| Tarjetas colchón 01, 02 y 03 | Completas |

El AP valida E1 a E6; E7 es control técnico. Hay que conservar todas las versiones. Los checkpoints digitales son solo C1, C2 y C3.

---

## 2. El usuario principal: John Smith

- 29 años, ingeniero de software en **TechSolutions**, San José. Modalidad híbrida, horario de 8:00 a 5:00, zona horaria UTC-6.
- Vive en **La Lima de Cartago**. Los días que va a la oficina toma el **bus de Lumaca**.
- Antes el viaje duraba 10 a 15 minutos. Hoy se alarga, y con un accidente o un retraso puede perder hasta una hora más. Por eso sale con **una hora de colchón**.
- Tiene reuniones, entregas semanales y una bandeja de correo que no deja de crecer.
- En el bus no puede abrir la laptop y la pantalla del celular lo marea. Termina scrolleando o con música, pero sin poder apagar la cabeza.
- Al llegar gasta **otra hora** reorganizando su agenda en 3 o 4 apps distintas. Llega cansado y con la sensación de que "bajó igual de perdido".

> Versiones viejas: el prompt para Grok que se hizo antes decía "John Mitch, 32 años". El perfil correcto es **John Smith, 29 años**, el del caso de prueba.

### Persona secundaria (nueva)

Una **potencial usuaria entrevistada**: estudiante universitaria que viaja en bus. De esa conversación salió el giro a voz (sección 4). Todavía no se decide si se suma como persona secundaria en el cuadernillo o si John sigue siendo el único actor.

---

## 3. El problema (lo que dice el cuadernillo)

- **El dolor no es solo el tiempo perdido.** Es la preocupación por lo pendiente durante el viaje y la hora de reorganizar después.
- **Descansar en el bus es válido.** La solución no puede exigirle esfuerzo a alguien que ya viene cansado.
- **Mirar la pantalla en movimiento marea.** Se diseña para poca o ninguna mirada.
- **Capturar con las manos ocupadas y sin hablar en voz alta** (privacidad, ruido) pesa tanto como la idea del producto.
- **Pregunta "¿Cómo podríamos…?":** ¿Cómo podríamos ayudar a quien viaja a diario a llegar a su destino con la cabeza más liviana y el día más claro, sin exigirle esfuerzo extra ni quitarle el descanso que necesita en el trayecto?
- **Hipótesis (E3):** si durante el viaje John puede sacar de la cabeza lo más urgente, rápido y casi sin mirar, bajará con menos ansiedad y necesitará menos tiempo reagendando al llegar.
- **Cómo se mide:** minutos que la persona dice que pasó reorganizando al llegar, y qué tan "cargada" llegó, del 1 al 5.
- **Cambiaríamos la propuesta si:** la mayoría solo quiere desconectar en el bus, prefiere seguir con Calendar y notas de voz, o la restricción de no mirar y no hablar hace imposible cualquier interacción útil.

---

## 4. Cómo evolucionó el concepto

1. **MVP v1 del cuadernillo (E4):** una captura mínima en el trayecto y un resumen corto al llegar (lo urgente, lo que se puede mover y lo que quedó de ayer). Tres formas de captura por contrastar: botones grandes de un toque, nota de voz en voz baja con audífonos, o frase corta escrita.
2. **Seis mockups de interfaz** inspirados en Flow (sección 10): un toque, susurro, llegada, ruta, pantalla bloqueada y modo descanso.
3. **Se eligió el widget de pantalla bloqueada** (opción 5) como dirección y se fue iterando: notificaciones conversacionales ordenadas por prioridad, después línea de tiempo visual, después enlaces por proyecto, después escalera por tema, y al final el viaje en vivo con Waze.
4. **Llegó el caso de prueba MVP** (sección 8): la defensa de John el viernes 9 de octubre.
5. **Entrevista con una potencial usuaria:** quiere usar la app **sin leer ni escribir**, sobre todo en el bus. Nort pasa a ser **voice-first**.
6. **La app completa con tres pestañas** (Hoy, Nort, Tú), con un "cerebro" navegable en el centro.

---

## 5. Concepto actual

**Nort es un asistente personal por voz que reúne lo que tienes en tu calendario, tu correo y tus archivos, entiende tu día y te deja consultarlo y organizarlo hablando, sin tener que mirar la pantalla.**

Lo que Nort **no** es:

- **No es otro calendario.** Los eventos siguen en Google Calendar.
- **No es una app de productividad.** No mide cuánto trabajas ni te empuja a hacer más.
- **No es un chatbot genérico.** Solo responde sobre tu vida organizada y con tus datos.

La promesa para la usuaria:

> "No necesito abrir cinco aplicaciones para saber qué está pasando con mi vida. Se lo pregunto a Nort."
>
> "No necesito sentarme a organizar todo. Se lo digo y él se encarga."

**El diferencial no es la IA ni la integración. Es la forma de interactuar:** hablar y escuchar, con contexto, en los momentos en que una app tradicional estorba (en el bus, caminando, cocinando, entre actividades).

### El core

Un ciclo de conversación con contexto: **escuchar → entender con tu contexto → responder breve → actuar (con tu permiso) → recordar.**

Sirve a tres trabajos:

| Trabajo | Ejemplo | Lo que hace Nort |
|---|---|---|
| Consultar | "¿Qué tengo cuando llegue?" | Responde en dos frases con lo que importa. |
| Pedir | "Agéndame una reunión con Juan mañana a las 3." | Crea, mueve o recuerda, y confirma en voz alta. |
| Ser avisado | (Nort habla primero) "Tu defensa se adelantó a la 1:30." | Interrumpe solo si algo importante cambia. |

### Ejemplos de lo que la usuaria debería poder decir

"¿Qué tengo hoy?", "¿Qué tengo después de clases?", "¿Tengo algo pendiente para mañana?", "Recuérdame enviar el informe cuando llegue a la universidad", "Mueve la reunión de las 3 para las 4", "¿Cuánto tiempo libre tengo esta tarde?", "¿Qué debería hacer ahora?", "Agrega estudiar contabilidad el jueves de 7 a 9 de la noche". Sin comandos aprendidos: lenguaje natural.

---

## 6. Reglas de interacción y de respuesta

### Cómo responde Nort

1. Primero lo que se preguntó. Nada de saludos ni introducciones.
2. Máximo dos frases, unos 8 segundos, máximo tres elementos.
3. Lenguaje hablado: "a las 2", "unas dos horas", nunca "14:00–16:00".
4. Una sugerencia como máximo, dicha como oferta: "Si quieres, …".
5. Lo que está a salvo antes del riesgo: "Te queda menos margen, pero alcanza."
6. Nunca inventa. Si no lo sabe: "No lo veo en tu calendario."
7. Menciona la fuente solo cuando ayuda.
8. "Más detalle" amplía; la primera respuesta no.
9. En pantalla: el mismo texto como subtítulo y **una sola tarjeta** visual.

Ejemplo: a "¿Qué tengo hoy?" no responde "Hoy tienes 6 eventos: a las 8:00 Daily Stand-up de 30 minutos…", sino "A las 10 tienes Contabilidad y a las 2 una reunión. Después tienes unas dos horas libres."

### Confirmaciones

- **Leer:** sin confirmación.
- **Crear:** confirma diciendo el resultado ("Listo, reunión con Juan mañana a las 3"). Se puede deshacer diciendo "deshaz".
- **Mover, borrar o escribirle a otra persona:** pregunta antes ("¿Lo hago?").
- **Nunca resuelve un conflicto importante solo.**

### Voz

- **Activación:** botón de los audífonos (doble toque), botón grande en la app y en el widget. Sin "Oye Nort" en el MVP.
- **Ambigüedad:** pregunta una sola cosa. Si no es grave, decide lo más probable y lo dice.
- **Control:** se le puede hablar encima para cortarlo. "Repite", "más detalle", "para" y "después" funcionan siempre.
- **Si no entiende:** lo pide una vez; si vuelve a fallar, lo guarda como nota.
- **Privacidad:** sin audífonos no habla por el parlante; muestra la respuesta y pregunta "¿te la leo?".

### Empatía

La empatía no es un tono simpático: son reglas de qué decir primero y qué callar.

| Situación | Cómo responde |
|---|---|
| Día cargado | Lo reconoce y ofrece ayuda: "Hoy tienes bastante. Si quieres, te ayudo a acomodar la tarde." |
| Tiempo libre | Ofrece, no ordena: "Podrías avanzar Contabilidad." |
| Entrega cercana | Tranquiliza con datos: "Todavía tienes tiempo para avanzarla." |
| Retraso o imprevisto | Primero lo que está a salvo; nunca culpa: "No depende de ti." |
| Quiere descansar | Se calla hasta su parada, salvo algo importante. |
| Después de algo difícil | Pregunta "¿cómo te fue?" una vez y sigue. |

**Lo que no hace:** emojis, frases motivacionales ("¡Tú puedes!"), falsa intimidad, sermones de productividad ni dramatizar un retraso.

### Interrupciones (proactivo, pero no molesto)

| Nivel | Qué entra | Qué hace Nort |
|---|---|---|
| Importante | Cambio de hora o lugar de algo de hoy, conflicto, riesgo de llegar tarde | Habla ya si hay audífonos; si no, notificación con sonido. |
| Útil | Hueco libre, entrega mañana, sugerencia de preparación | Una vez, en un momento de transición. Máximo 3 al día. |
| Puede esperar | Correos informativos, tareas sin fecha | Se guarda para el siguiente resumen. |

### Modos según el contexto

- **En trayecto:** solo voz y pantalla bloqueada. Solo tareas ligeras. Avisa antes de la parada.
- **En una actividad** (clase, reunión): silencio salvo algo crítico.
- **Manos ocupadas** (audífonos, app en segundo plano): conversación completa por voz.
- **Sin audífonos en público:** no habla; muestra la tarjeta y pregunta "¿te lo leo?".

---

## 7. Integraciones

| Integración | Uso | Prioridad |
|---|---|---|
| Google Calendar | Leer y escribir. Base de casi todas las respuestas. | P0 |
| Gmail | Solo lectura. Detecta fechas, cambios e invitaciones y **propone**; nunca agrega solo. | P1 |
| Google Drive | Solo nombre, carpeta y fecha de edición. No lee el contenido en el MVP. | P1 |
| Ubicación y lugares guardados | "Cuando llegue", recordatorios por lugar. Solo en trayecto y con permiso. | P1 |
| **Waze** | Estado del viaje en vivo en la pantalla bloqueada (ver abajo). | Decidido por el equipo; ver tensión en sección 12 |
| Outlook, Teams, Notion, Moodle, Classroom, otras APIs | Después de validar el core con Google. En la app aparecen como "Conectar". | Después |

### Waze

Decisión del equipo: **Nort tiene integración con Waze.** Cada vez que John hace un viaje, la pantalla bloqueada muestra el estado del viaje y, a partir de él, Nort despliega notificaciones empáticas sobre sus compromisos y entregables.

Suposición de diseño: como John va en bus y Waze es para manejar, Waze se usa como **fuente del tráfico de la ruta** (choques, tramos lentos, hora de llegada), no como navegación. Si se muestra con alguien que maneja, las notificaciones no deberían pedir que se lean mientras maneja.

### Qué sabe Nort de la usuaria

Eventos y clases (Calendar), tareas y fechas límite (voz y Gmail), lugares frecuentes, rutina de viaje, tiempo de preparación habitual (por defecto 30 min), preferencias de aviso, personas frecuentes, archivos por proyecto (Drive, P1) y la carga del día. **No:** ubicación continua, salud ni finanzas.

Transparencia: "¿Qué sabes de mí?" responde qué fuentes usa; "Olvida eso" borra una preferencia.

---

## 8. Caso de prueba MVP: la defensa de John

Objetivo: comprobar que Nort entiende el día como **eventos + tareas + deadlines + documentos + desplazamientos + tiempo disponible + prioridades**, y no como una lista de tareas. El resultado ideal es que pueda decir: *"Ahora haz esto, después esto, a esta hora debes salir, cuando llegues prepara esto, a las 2:00 tienes tu defensa."*

### Datos del caso

- **Cuenta:** `john.smith@techsolutions.com` (Calendar y Gmail).
- **Drive:** `/Trabajo/Investigacion_Laboratorio/Defensa_Final` con `Informe_Final_Laboratorio.docx`, `Resultados_Minitab.mtw` y `Presentacion_Defensa.pptx`.
- **Proyecto:** Defensa de proyecto de investigación en laboratorio. **Viernes 9 de octubre de 2026, 2:00 p. m.**, 1 hora, presencial, Laboratorio de Investigación Tecnológica. Los tres archivos deben estar listos **30 minutos antes**.

### Calendario del viernes

| Hora | Evento |
|---|---|
| 8:00 – 8:30 | Daily Stand-up |
| 8:30 – 9:00 | Revisión de correos |
| 9:00 – 10:00 | Desarrollo, sprint actual |
| 10:00 – 10:30 | Reunión con equipo de investigación |
| 10:30 – 11:00 | Preparación para viaje (libre) |
| 11:00 – 12:30 | Viaje en bus (solo tareas ligeras) |
| 12:30 – 1:00 | Preparación para la defensa |
| 1:00 – 1:30 | Revisión final (informe, Minitab, PowerPoint) |
| 1:30 – 2:00 | Traslado y preparación final (libre) |
| 2:00 – 3:00 | **Defensa** (máxima prioridad) |

### Tareas

| Tarea | Duración | Fecha límite | Prioridad |
|---|---|---|---|
| Finalizar informe | 90 min | Jueves 8, 6:00 p. m. | Alta |
| Revisar Minitab | 45 min | Viernes 9, 12:00 p. m. | Alta |
| Finalizar PowerPoint | 60 min | Viernes 9, 11:00 a. m. | Crítica |
| Ensayar presentación | 30 min | Antes del viernes 9, 1:00 p. m. | Alta |
| Revisar correo | 20 min | Diaria, en la mañana | — |
| Enviar avance semanal al jefe | 30 min | Viernes 9, 4:00 p. m. | Media |

### Correos que debe detectar

- **jefe@techsolutions.com**, "Avance semanal - viernes": crear la tarea de enviar el avance antes de las 4:00 p. m. del viernes.
- **investigacion@techsolutions.com**, "Defensa proyecto laboratorio": asociar la defensa al proyecto.

### Escenarios de prueba

1. **Pantalla de las 8:00:** responder en menos de 10 segundos qué tengo hoy, qué es urgente, cuánto tiempo tengo, cuándo salgo, qué preparo, si hay conflicto y qué hago ahora.
2. **Recomendación:** la presentación existe pero se editó ayer a las 6:00 p. m., así que falta una revisión final.
3. **Conflicto:** reunión con cliente de 11:30 a 12:30, durante el viaje. Mostrar tres opciones (reprogramar reunión, modificar viaje, ver conflicto) sin resolver solo.
4. **Cambio de último momento:** a las 10:15 llega un correo; la defensa pasa a la 1:30. Recalcular salida, preparación, revisión y margen.
5. **Retraso del bus:** a las 11:45, 20 minutos de retraso. Nueva llegada 12:50 y alerta de margen reducido.
6. **Tarea incompleta:** a la 1:00, Minitab sin revisar. Recomendar hacerlo de inmediato.
7. **Espacio libre:** se cancela la reunión de 10:00. Recomendar algo que quepa en 30 minutos, nunca una tarea de 60.
8. **Crear el evento** de la defensa en Google Calendar con sus archivos.
9. **Recordatorios:** jueves 6:00 p. m., y el viernes a las 10:00, 10:45, 11:00, 12:30, 1:30 y 2:00.
10. **Prueba extrema:** todo a la vez (reunión 9:30–10:30, viaje, defensa, presentación y Minitab incompletos, cambio de horario y retraso), sin perder deadlines ni crear actividades imposibles.

### Problemas del propio caso (conviene corregirlos antes de probar)

- La presentación dura 60 minutos y debe estar antes de las 11:00, pero de 8:00 a 11:00 todo está ocupado. Lo correcto es que Nort avise que no cabe.
- Minitab dura 45 minutos en la lista de tareas y 15 en el escenario de la 1:00. Además, a la 1:00 su fecha límite (12:00) ya pasó.
- Los recordatorios siguen calculados para las 2:00 aunque la defensa se adelante a la 1:30.

---

## 9. La interfaz

### La app: tres pestañas abajo (`mockups/08-app.html`)

Ambientada el viernes a las 11:20: John va en el bus y la defensa ya se adelantó a la 1:30. Se puede abrir una pestaña directamente con `08-app.html?tab=nort` o `?tab=tu`.

**1. Hoy:** el estado del viaje y toda la información condensada en bloques.
- Una sola conclusión arriba: "Vas bien: llegas 12:30 y tu defensa es a la 1:30".
- Tarjeta del viaje con Waze: llegada estimada, avance de la ruta y tráfico.
- Cuatro bloques de resumen: lo próximo, el margen, los pendientes y los avisos.
- El flujo del día en escalera, con la línea de "ahora".
- Pendientes que se marcan con un toque.
- Notificaciones con un punto de color según importancia y el ícono de su fuente.

**2. Nort (el cerebro):** una red de nodos que representa al asistente pensando.
- Nort en el centro y 7 categorías: Agenda, Pendientes, Viaje, Proyectos, Personas, Fuentes y Preferencias. Líneas punteadas cruzan entre ellas (por ejemplo, Waze → Tráfico → Llegada → Defensa).
- **Frases que rotan según el contexto** cada 4,5 segundos ("Waze no reporta atrasos en tu ruta"), mientras se enciende el camino de nodos que la justifica.
- **Navegable:** arrastrar, zoom con pellizco o rueda, botones +, − y "ver todo". Al tocar un nodo se centra, se atenúa lo demás y se abre una hoja con la ruta (Nort › Agenda › Defensa), su información, chips para saltar a nodos conectados y "Preguntarle a Nort sobre esto".
- **Modo llamada:** pantalla propia con un orbe, temporizador, subtítulos, silenciar, oír la voz, pasar al chat y colgar. La llamada sigue con la pantalla bloqueada.
- **Chat:** sugerencias rápidas, campo de texto y micrófono que pasa a la llamada. Si no encuentra algo: "No lo encontré en tu calendario, tu correo ni tu Drive".

**3. Tú:** el usuario y la configuración.
- Perfil (John Smith, TechSolutions).
- Conexiones: Google Calendar, Gmail, Drive y Waze con interruptores; Outlook, Teams y Notion con "Conectar"; "Otra API" con nombre, URL y clave.
- Personalización de Nort: voz, trato (tú, usted o vos), largo de las respuestas, cuándo habla primero, velocidad de la voz y si reconoce cómo te sientes.
- Cómo se llama a Nort, rutina y lugares, No molestar, y "Lo que Nort sabe de ti" con recuerdos que se borran uno por uno.

### Pantalla bloqueada: viaje en vivo con Waze (`mockups/05-v2-widget-asistente.html`)

De arriba a abajo:
1. **Viaje en vivo:** ícono de Waze, ruta (Lumaca), retraso y hora de llegada en grande, con una barra de casa a oficina, el tramo lento y la alerta del incidente.
2. **Notificación de Nort "con datos de Waze":** título, una frase y como mucho dos botones.
3. **Escalera del día "Hoy":** cada tema en su propia fila, un escalón más abajo y a la derecha que el anterior, con ícono, nombre de una palabra y hora. Los tres pendientes prioritarios llevan su número de color. Si un compromiso empieza antes de la llegada real del bus, se marca en rojo y late.
4. **Tarjetas de proyecto con enlaces** que elige el usuario, como íconos de app (PowerPoint, Teams, Outlook, Notion, Excel, Colab, Word, WhatsApp…), con un botón "+ Agregar".

Las cuatro fases del viaje:

| Hora | Momento | Qué dice Nort |
|---|---|---|
| 6:40 | Salida | "Llegas 7:30, una hora antes del stand-up. Puedes descansar." |
| 7:03 | Choque | "No depende de ti. Llegas 7:48 y el stand-up sigue a salvo." |
| 7:24 | Detenido | "Cinco minutos tarde al stand-up. La presentación de las 10:00 sigue a salvo." Botones: Avisar al equipo, Unirme por Teams. |
| 8:30 | Llegando | "Fue un viaje pesado. Lo primero: presentación 10:00, tienes hora y media." Botón: Abrir guion. |

Lo que pidió el equipo para el widget: notificaciones ordenadas por prioridad, con el asistente teniendo el contexto completo de cada entregable, y **llamadas interactivas y naturales directamente desde el widget** ("¿Cómo te sientes para tu presentación de hoy? ¿Quieres practicar?"), igual con otros compromisos, todo integrado con Calendar y Gmail. En una iteración posterior, las sugerencias de texto de las tarjetas se cambiaron por enlaces; el asistente conversacional volvió en la app 08 (llamada y chat desde la pestaña Nort).

### Flujo completo por voz (`mockups/07-flujo-voz.html`)

El caso de prueba de principio a fin en 12 pasos, con el teléfono al centro (botón de voz, subtítulos y una tarjeta), los pasos a la izquierda y notas para el equipo a la derecha. Se avanza con las flechas; "Escuchar a Nort" lee las respuestas con la voz del navegador.

1. Configuración: conectar Calendar, Gmail y Drive; detectar la defensa en el correo.
2. Jueves en la noche: la presentación no cabe antes de las 11; propone hacerla de 9 a 10.
3. 8:00, "¿Qué tengo hoy?".
4. Conflicto con la reunión del cliente: espera a que termine el stand-up y ofrece tres opciones.
5. 30 minutos libres: solo tareas que caben.
6. La defensa se adelanta a la 1:30.
7. Faltan 15 minutos para salir.
8. En el bus: John quiere descansar y Nort se calla.
9. El bus se atrasa 20 minutos: el margen baja a 5 minutos.
10. Minitab pendiente (sin audífonos en el laboratorio, Nort escribe en vez de hablar).
11. Todo listo antes de la defensa.
12. Cierre: "¿Cómo te fue?" y el avance semanal.

### Mockups anteriores (siguen en la galería)

| Mockup | Qué es |
|---|---|
| `01-un-toque.html` | Tres botones grandes (Trabajo, Personal, "No se me olvide"). |
| `02-susurro.html` | Mantener presionado y hablar bajito con audífonos. |
| `03-llegada.html` | Resumen al bajar del bus: lo urgente, lo movible y lo de ayer. |
| `04-ruta.html` | Trayecto parada por parada; deja listo el aviso de retraso al equipo. |
| `05-pantalla-bloqueada.html` | Primera versión del widget: llegada y tres botones de captura. |
| `06-modo-descanso.html` | Nort dice que puede descansar y avisa antes de la parada. |

Galería: `mockups/index.html` (abrir con doble clic). Estilos compartidos en `nort.css` e íconos en `icons.js`.

---

## 10. Inspiración: Flow

[Flow](https://github.com/jxsu404/Flow) es otro proyecto del equipo: un asistente en español que organiza la vida académica, interpreta el momento y responde "¿qué sería bueno hacer ahora?". Ciclo: hablar → entiende → organiza → sincroniza → recuerda.

Reglas que Nort hereda:
- Una frase con la conclusión del momento, no datos crudos.
- Las obligaciones van primero; el contexto (clima, hora) solo enriquece.
- Nunca inventar: si no hay dato, no se menciona.
- Tono calmado, sin coach agresivo ni emojis.

Estética: azul noche, acento turquesa, tipografía Geist, tarjetas redondeadas. Colores de estado: verde (en calma), ámbar (atención), rosa (actuar). Las reuniones van en violeta para no confundirse con la zona oscura de lo que ya pasó. Los textos de la interfaz usan tuteo, como Flow; el Banco de Contraste usa voseo.

---

## 11. MVP

### P0: sin esto no hay producto

1. Consultas por voz sobre la agenda (hoy, mañana, "cuando llegue", "después de clases", tiempo libre).
2. Crear por voz eventos, tareas con fecha límite y recordatorios.
3. Mover y cancelar por voz, con confirmación.
4. "¿Qué debería hacer ahora?": una tarea que cabe en el tiempo libre real.
5. Respuesta hablada breve, subtítulo y una tarjeta.
6. Google Calendar, leer y escribir.
7. Detección de conflictos y cambios, con opciones, sin resolver solo.
8. Modo trayecto: hora de llegada, solo tareas ligeras y aviso antes de la parada.

### P1: para pasar el caso de prueba completo

9. Gmail en solo lectura.
10. Drive con solo metadatos.
11. Recordatorios por lugar.
12. Avisos proactivos con límite diario.
13. Widget de pantalla bloqueada.

### Fuera del MVP

Palabra de activación siempre encendida, redactar o leer correos completos, reprogramar sin confirmación, agenda de equipo, gestión de proyectos (tableros, porcentajes), integraciones con Outlook, Teams, Notion o sistemas académicos, personalización de voz y personalidad, historial de chat y estadísticas.

---

## 12. Validación con usuarios reales

**Método "Mago de Oz":** una persona del equipo hace de Nort por llamada con audífonos (o con el mockup 07) mientras la participante va en un trayecto real. De 5 a 8 participantes, estudiantes y trabajadores que viajan en bus.

| # | Situación | Lo que dice la participante | Éxito |
|---|---|---|---|
| 1 | En el bus | "¿Qué tengo cuando llegue?" | Repite la respuesta sin mirar la pantalla. |
| 2 | Caminando | "Agéndame una reunión con Juan mañana a las 3." | Lo logra al primer intento. |
| 3 | Entre actividades | "Mueve la reunión de las 3 para las 4." | Entiende la confirmación y siente control. |
| 4 | Con una hora libre | "¿Qué puedo hacer?" | La tarea sugerida cabe en el tiempo. |
| 5 | Caminando | "Recuérdame comprar leche cuando salga de la universidad." | El aviso llega a tiempo. |
| 6 | Escuchando música | Nort interrumpe con un conflicto | Califica la interrupción como útil (4 o 5 de 5). |
| 7 | Cambio de último momento | Nort avisa que un evento se adelantó | Explica qué cambió sin mirar. |
| 8 | Día cargado | "¿Qué tengo hoy?" | Siente que le baja la carga. |
| 9 | Cocinando | "¿Qué tengo mañana?" | Usa la respuesta sin tocar el teléfono. |

**Qué medir:** tareas completadas sin mirar, miradas por tarea, intentos por pedido, respuestas escuchadas completas versus cortadas, preferencia entre hablar, escuchar y tocar, carga mental al llegar (1 a 5) e incomodidad de hablar en público (1 a 5).

**Qué nos haría cambiar:**
- Si la mayoría no quiere hablar en un bus lleno: "Nort habla, la usuaria toca".
- Si dos frases se sienten incompletas: "respuesta + ¿quieres el detalle?".
- Si los avisos molestan: uno al día y solo de nivel importante.

---

## 13. Tensiones y decisiones pendientes

1. **E2 contra voice-first.** E2 dice que mirar poco la pantalla "no es una prueba automática de que la voz es la respuesta". Ahora la voz es la hipótesis principal, respaldada por una entrevista. Hay que actualizar E2.
2. **E4 contra "capa central".** E4 dice que Nort no es un "unificador total" ni "automatización mágica de la agenda". Ahora Nort es la capa central de consulta conectada a Calendar, Gmail, Drive y Waze. Opciones: cambiar E4, o reconciliarlo diciendo que Nort lee esas fuentes solo para decidir qué decir y preguntar, y siempre pide permiso para actuar.
3. **Waze.** El equipo decidió integrarlo y ya está en los mockups 05 v2 y 08, pero el documento de decisiones voice-first lo deja fuera del MVP y el cuadernillo no lo menciona. Hay que alinear los tres (por ejemplo, agregarlo como supuesto en E3 y E4).
4. **Persona.** La usuaria entrevistada es estudiante; el actor del cuadernillo y del caso de prueba es John, ingeniero. Decidir si se suma una persona secundaria.
5. **Una sola entrevista es una señal, no una prueba.** La voz es hipótesis hasta validarla con los 9 casos de la sección 12.
6. **Evidencia pendiente.** Red Team, E5, E6 y el Slide 4 solo se llenan con lo que salga del Red Team y del Banco de Contraste. No inventar.
7. **Prompt para Grok desactualizado.** Dice "John Mitch, 32 años" y no incluye voice-first, Waze ni la app de tres pestañas. Si se vuelve a usar, conviene reemplazarlo por este documento.

---

## 14. Archivos

| Archivo | Contenido |
|---|---|
| `docs/cuadernillo-nort-redaccion-empatia.md` | Cuadernillo con los 7 entregables. |
| `docs/nort-voice-first-decisiones.md` | Las 12 decisiones de producto, UX y MVP voice-first. |
| `docs/nort-contexto-completo.md` | Este documento. |
| `mockups/index.html` | Galería de todos los mockups. |
| `mockups/08-app.html` | La app con las pestañas Hoy, Nort y Tú. |
| `mockups/07-flujo-voz.html` | El caso de prueba completo por voz, en 12 pasos. |
| `mockups/05-v2-widget-asistente.html` | Pantalla bloqueada con viaje en vivo de Waze. |
| `mockups/01` a `06` | Opciones de interfaz anteriores. |
| `mockups/nort.css`, `mockups/icons.js` | Estilos e íconos compartidos. |
