# Nort voice-first: decisiones de producto, UX y MVP

**Base:** una conversación con una potencial usuaria (estudiante universitaria que viaja en bus) y el caso de prueba de la defensa de John Smith.
**Alcance:** todo es mockup. Nada de esto está construido ni conectado de verdad.
**Mockup de referencia:** `mockups/07-flujo-voz.html` (flujo completo en 12 pasos).

> Una sola entrevista es una señal, no una prueba. Este documento toma la voz como **hipótesis principal** y define cómo validarla (sección 12) antes de construir más.

---

## Concepto en una frase

**Nort es un asistente personal por voz que reúne lo que tienes en tu calendario, tu correo y tus archivos, entiende tu día y te deja consultarlo y organizarlo hablando, sin tener que mirar la pantalla.**

Lo que Nort **no** es:

- No es otro calendario: no compite por ser el lugar donde se guardan los eventos. Los eventos siguen en Google Calendar.
- No es una app de productividad: no mide cuánto trabajas ni te empuja a hacer más.
- No es un chatbot genérico: solo responde sobre tu vida organizada y con tus datos.

La promesa para la usuaria:

> “No necesito abrir cinco aplicaciones para saber qué está pasando con mi vida. Se lo pregunto a Nort.”
> “No necesito sentarme a organizar todo. Se lo digo y él se encarga.”

---

## 1. Nuevo core del producto

El core es **un ciclo de conversación con contexto**:

**Escuchar → entender con tu contexto → responder breve → actuar (con tu permiso) → recordar.**

Todo lo demás existe para servir a tres trabajos:

| Trabajo | Ejemplo | Lo que hace Nort |
|---|---|---|
| **Consultar** | “¿Qué tengo cuando llegue?” | Responde en dos frases con lo que importa. |
| **Pedir** | “Agéndame una reunión con Juan mañana a las 3.” | Crea, mueve o recuerda, y confirma en voz alta. |
| **Ser avisado** | (Nort habla primero) “Tu defensa se adelantó a la 1:30.” | Interrumpe solo si algo importante cambia. |

**Decisión:** la pantalla principal deja de ser una lista o un calendario. Es un botón para hablar más **una sola tarjeta** que responde “¿qué necesito saber ahora?”.

---

## 2. Diferencial frente a un calendario tradicional

| Un calendario | Nort |
|---|---|
| Tú vas a buscar la información. | Le preguntas y te responde. |
| Muestra eventos. | Interpreta: tiempo libre, riesgos, qué preparar, cuándo salir. |
| Cada servicio por separado (calendario, correo, Drive). | Una sola respuesta que cruza las fuentes. |
| Para agregar algo llenas un formulario. | Lo dices como lo dirías a una persona. |
| Avisa a una hora fija. | Avisa según el contexto: si vas en bus, si estás en clase, si el bus se atrasa. |
| Pide mirar y leer. | Funciona con audífonos y sin mirar. |

**El diferencial no es la IA ni la integración. Es la forma de interactuar: hablar y escuchar, con contexto, en los momentos en que una app tradicional estorba.**

---

## 3. Flujo principal de interacción

### Flujo reactivo (la usuaria pregunta o pide)

1. **Disparador:** presionar el botón de los audífonos, tocar el botón de voz de la app o el widget de la pantalla bloqueada.
2. **Escucha:** tono corto de inicio. Subtítulo en vivo de lo que entendió.
3. **Entiende:** intención (consultar, crear, mover, recordar) + datos (quién, cuándo, dónde) + contexto (dónde está, qué tiene después).
4. **Responde:** máximo dos frases por voz. En pantalla, el mismo texto como subtítulo y una tarjeta visual.
5. **Confirma si cambia algo:** lo que solo lee no se confirma; lo que crea se confirma diciendo el resultado; lo que mueve, borra o afecta a otras personas se pregunta antes.
6. **Actúa y recuerda:** escribe en el calendario, programa el recordatorio y guarda la preferencia si aplica.

### Flujo proactivo (Nort habla primero)

1. **Detecta** un cambio o una oportunidad: correo que mueve un evento, conflicto, retraso, hueco libre, entrega cercana.
2. **Clasifica:** importante, útil o puede esperar (ver sección 11).
3. **Elige el momento y el canal:** voz ahora, notificación silenciosa o el siguiente resumen.
4. **Ofrece una sola acción** y espera la respuesta.

### Flujo del día completo

Está en el mockup `07-flujo-voz.html`: configuración, víspera, “¿qué tengo hoy?”, conflicto, hueco libre, cambio de hora, salida, bus, retraso, pendiente de último momento, “todo listo” y cierre del día.

---

## 4. Funcionalidades prioritarias para el MVP

### P0: sin esto no hay producto

1. **Consultas por voz sobre la agenda:** hoy, mañana, “cuando llegue”, “después de clases”, “esta tarde”, “¿cuánto tiempo libre tengo?”.
2. **Crear por voz:** eventos, tareas con fecha límite y recordatorios por hora.
3. **Mover y cancelar por voz** con confirmación.
4. **“¿Qué debería hacer ahora?”:** recomienda una tarea que cabe en el tiempo libre real.
5. **Respuesta hablada breve + subtítulo + una tarjeta.**
6. **Google Calendar:** leer y escribir.
7. **Detección de conflictos y cambios** con aviso y opciones, sin resolver nada solo.
8. **Modo trayecto:** hora de llegada, solo tareas ligeras y aviso antes de la parada.

### P1: para pasar el caso de prueba completo

9. **Gmail en solo lectura:** detectar fechas límite, eventos y cambios de horario, y proponer agregarlos.
10. **Drive (solo nombres, carpetas y fecha de edición):** asociar archivos a un proyecto y saber si están por revisar.
11. **Recordatorios por lugar:** “cuando llegue a la universidad”, “cuando salga del trabajo”, usando lugares guardados.
12. **Avisos proactivos con límite diario** (ver sección 11).
13. **Widget de pantalla bloqueada** con la tarjeta del momento y el botón para hablar.

---

## 5. Funcionalidades que quedan fuera del MVP

| Fuera | Por qué |
|---|---|
| Palabra de activación siempre encendida (“Oye Nort”) | Batería, privacidad y falsos positivos en el bus. Se usa el botón de los audífonos. |
| Redactar y responder correos completos | Riesgo alto de error y mucho texto. Nort solo propone mensajes cortos y pide permiso. |
| Leer correos completos en voz alta | Respuestas largas. Nort resume en una frase y dice de quién es. |
| Reprogramar solo, sin confirmación | Rompe la confianza. Siempre se pregunta. |
| Agenda de equipo y coordinación entre varias personas | Otro producto. |
| Gestión de proyectos (tableros, subtareas, porcentajes) | Lo convierte en una app de productividad. |
| Integraciones con Outlook, Teams, Notion, Waze o sistemas académicos (Moodle, Classroom) | Se agregan después de validar el core con Google. |
| Personalización de voz y de personalidad | No mueve la hipótesis. |
| Historial de chat, estadísticas y paneles | Más texto y más pantalla, lo contrario del concepto. |

---

## 6. Cómo funciona la interacción por voz

**Activación**
- Botón de los audífonos (doble toque) o atajo del asistente del sistema.
- Botón grande de voz en la app y en el widget.
- Sin palabra de activación en el MVP.

**Lenguaje natural, sin comandos**
- Fechas relativas: “mañana”, “el jueves”, “la otra semana”.
- Momentos relativos a la agenda: “después de clases” es el final del último evento de tipo clase; “cuando llegue” es la hora estimada de llegada del trayecto.
- Horas ambiguas: “a las 3” se interpreta como 3:00 p. m. si es horario de actividad, y Nort lo dice: “Lo puse a las 3 de la tarde.”
- Personas y lugares conocidos: “Juan” es el contacto con quien más se reúne; “la universidad” es un lugar guardado.

**Ambigüedad**
- Pregunta **una sola cosa**: “¿La reunión de las 3 con Juan o la de Ana?”
- Si no está seguro y no es grave, decide lo más probable y lo dice para que se pueda corregir.

**Confirmaciones**
- Leer: sin confirmación.
- Crear: confirma diciendo el resultado (“Listo, reunión con Juan mañana a las 3”). Se puede deshacer diciendo “deshaz” durante unos segundos.
- Mover, borrar o escribirle a otra persona: pregunta antes (“¿Lo hago?”).

**Control de la conversación**
- La usuaria puede hablar encima de Nort para cortarlo.
- “Repite”, “más detalle”, “para” y “después” funcionan siempre.

**Cuando no entiende**
- “No te entendí bien, ¿me lo repites?” Una sola vez.
- Si vuelve a fallar: “Lo guardo como nota y lo vemos al llegar.” Nunca deja a la usuaria atascada.

**Privacidad**
- Si no hay audífonos conectados, no habla por el parlante: muestra la respuesta y pregunta “¿te la leo?”.

---

## 7. Cómo responde el asistente

**Reglas de la respuesta**

1. **Primero lo que se preguntó.** Nada de saludos ni introducciones.
2. **Máximo dos frases, unos 8 segundos.** Máximo tres elementos por respuesta.
3. **Lenguaje hablado:** “a las 2”, “unas dos horas”, nunca “14:00–16:00”.
4. **Una sugerencia como máximo**, dicha como oferta: “Si quieres, …”.
5. **Lo que está a salvo antes del riesgo:** “Te queda menos margen, pero alcanza.”
6. **Nunca inventa.** Si no lo sabe: “No lo veo en tu calendario” o “No lo encontré en ningún correo”.
7. **Menciona la fuente solo cuando ayuda:** “según el correo de investigación”.
8. **“Más detalle” amplía**, no la primera respuesta.

**Ejemplos**

| Pregunta | Mal | Bien |
|---|---|---|
| “¿Qué tengo hoy?” | “Hoy tienes 6 eventos: a las 8:00 Daily Stand-up de 30 minutos, a las 8:30…” | “A las 10 tienes Contabilidad y a las 2 una reunión. Después tienes unas dos horas libres.” |
| “¿Tengo algo pendiente para mañana?” | “Tienes una tarea.” | “La tarea de Contabilidad es para mañana. Esta tarde tienes tiempo libre para avanzarla.” |
| “Tengo una hora libre, ¿qué hago?” | Lista de cinco tareas. | “Te alcanza para avanzar Contabilidad. ¿Te pongo un aviso a las 4 para parar?” |

**Formato en pantalla:** el mismo texto de la voz como subtítulo, más una tarjeta visual. Nunca más de una tarjeta a la vez.

---

## 8. Qué debe conocer Nort sobre la usuaria

| Dato | De dónde sale | Para qué | MVP |
|---|---|---|---|
| Eventos, clases y reuniones | Google Calendar | Responder qué tiene y detectar conflictos | Sí |
| Tareas y fechas límite | Voz, Gmail | Priorizar y recomendar | Sí |
| Lugares frecuentes (casa, universidad, trabajo) | Se dicen una vez al configurar | “Cuando llegue”, recordatorios por lugar | Sí |
| Rutina de viaje (medio, duración, hora de salida) | Se dice una vez, se ajusta con el uso | Saber cuándo salir y qué se puede hacer en el camino | Sí |
| Tiempo de preparación habitual | Preferencia (por defecto, 30 min antes de algo importante) | Bloquear preparación y margen | Sí |
| Preferencias de aviso (cuánto, cuándo no molestar) | Configuración por voz | Saber cuándo hablar primero | Sí |
| Personas frecuentes | Calendario y correo | Entender “la reunión con Juan” | Sí |
| Archivos de cada proyecto | Drive (solo nombre, carpeta y fecha de edición) | Saber qué falta revisar | P1 |
| Carga del día | Calculada (eventos y minutos libres) | Ajustar el tono (sección 10) | Sí |
| Ubicación continua, salud, finanzas | No | Fuera del producto | No |

**Transparencia:** “¿Qué sabes de mí?” responde en voz qué fuentes usa. “Olvida eso” borra una preferencia.

---

## 9. Integraciones prioritarias

1. **Google Calendar (leer y escribir):** P0. Es la base de casi todas las respuestas.
2. **Gmail (solo lectura):** P1. Detecta fechas, cambios e invitaciones y **propone**; nunca agrega solo.
3. **Google Drive (solo metadatos):** P1. Nombre, carpeta y fecha de edición. No lee el contenido de los archivos en el MVP.
4. **Ubicación del teléfono y lugares guardados:** P1, para “cuando llegue” y los recordatorios por lugar. Solo durante un trayecto y con permiso.
5. **Después del MVP:** tráfico en vivo (Waze), Outlook y Teams, sistemas académicos (Moodle, Classroom).

**Decisión:** empezar solo con Google porque cubre a la usuaria entrevistada y al caso de prueba. En los mockups todo está simulado.

---

## 10. Cómo usar la empatía en las respuestas

La empatía no es un tono simpático. Son **reglas de qué decir primero y qué callar**:

| Situación | Señal | Cómo responde |
|---|---|---|
| Día cargado | Más de 4 compromisos o menos de 1 h libre | Lo reconoce y ofrece ayuda: “Hoy tienes bastante. Si quieres, te ayudo a acomodar la tarde.” |
| Tiempo libre | Hueco de 30 min o más | Ofrece, no ordena: “Podrías avanzar Contabilidad.” |
| Entrega cercana | Fecha límite en menos de 24 h | Tranquiliza con datos: “Todavía tienes tiempo para avanzarla.” |
| Retraso o imprevisto | El bus se atrasa, cambia un evento | Primero lo que está a salvo; nunca culpa: “No depende de ti.” |
| Quiere descansar | “Quiero descansar”, “ahora no” | Guarda silencio hasta su parada, salvo algo importante. |
| Después de algo difícil | Termina un evento importante | Pregunta “¿cómo te fue?” una vez y sigue. |

**Lo que no hace:** emojis, frases motivacionales (“¡Tú puedes!”), falsa intimidad, sermones sobre productividad ni dramatizar un retraso.

---

## 11. Comportamiento cuando está ocupada, desplazándose o sin mirar

### Modos según el contexto

| Modo | Cómo lo detecta | Cómo se comporta |
|---|---|---|
| **En trayecto** | Hora de salida de su rutina o “voy en el bus” | Solo voz y pantalla bloqueada. Propone únicamente tareas ligeras (escuchar, confirmar). Avisa antes de la parada. |
| **En una actividad** | Hay un evento en curso (clase, reunión) | Silencio. Solo interrumpe si algo crítico pasa antes del próximo compromiso. Lo demás espera a que termine. |
| **Manos ocupadas** | Audífonos puestos y app en segundo plano | Conversación completa por voz, igual de breve. |
| **Sin audífonos en público** | No hay audífonos conectados | No habla por el parlante. Muestra la tarjeta con un botón grande y pregunta “¿te lo leo?”. |

### Política de interrupciones

| Nivel | Qué entra | Qué hace Nort |
|---|---|---|
| **Importante** | Cambio de hora o lugar de algo de hoy, conflicto, riesgo de llegar tarde | Habla ya si hay audífonos; si no, notificación con sonido. |
| **Útil** | Hueco libre, entrega mañana, sugerencia de preparación | Una vez, en un momento de transición (al subir al bus, al terminar un evento). Máximo 3 al día. |
| **Puede esperar** | Correos informativos, tareas sin fecha | Se guarda para el siguiente resumen o para cuando pregunte. |

---

## 12. Casos de uso para validar con usuarios reales

**Método:** “Mago de Oz”. Una persona del equipo hace de Nort por una llamada con audífonos (o con el mockup 07 y su voz) mientras la participante está en un trayecto real. De 5 a 8 participantes, con estudiantes y trabajadores que viajan en bus.

| # | Situación | Lo que dice la participante | Éxito |
|---|---|---|---|
| 1 | En el bus, con audífonos | “¿Qué tengo cuando llegue?” | Repite la respuesta correctamente sin mirar la pantalla. |
| 2 | Caminando | “Agéndame una reunión con Juan mañana a las 3.” | Lo logra al primer intento y sin pensar en un formato. |
| 3 | Entre actividades | “Mueve la reunión de las 3 para las 4.” | Entiende la confirmación y siente que tuvo el control. |
| 4 | Con una hora libre | “Tengo una hora libre, ¿qué puedo hacer?” | Acepta o ajusta la sugerencia; la tarea cabe en el tiempo. |
| 5 | Caminando | “Recuérdame comprar leche cuando salga de la universidad.” | El aviso llega en el momento correcto. |
| 6 | Escuchando música | Nort interrumpe con un conflicto | Califica la interrupción como útil (4 o 5 de 5), no molesta. |
| 7 | Cambio de último momento | Nort avisa que un evento se adelantó | Explica qué cambió y qué sigue igual sin mirar. |
| 8 | Día cargado | “¿Qué tengo hoy?” | Siente que la ayuda le baja la carga, no que la sermonean. |
| 9 | Cocinando | “¿Qué tengo mañana?” | Usa la respuesta sin tocar el teléfono. |

**Qué medir**
- Porcentaje de tareas completadas sin mirar la pantalla.
- Cuántas veces mira la pantalla por tarea.
- Intentos por pedido.
- Duración de las respuestas que escuchó completas versus las que cortó.
- Preferencia entre hablar, escuchar y tocar.
- Carga mental al llegar, del 1 al 5 (la misma escala del cuadernillo).
- Incomodidad de hablar en voz alta en público, del 1 al 5.

**Qué nos haría cambiar**
- Si la mayoría **no quiere hablar en un bus lleno**, el modelo pasa a “Nort habla, la usuaria toca”: escuchar con audífonos y responder con toques en los audífonos o botones grandes.
- Si las respuestas de dos frases se sienten incompletas, se prueba un formato de “respuesta + ¿quieres el detalle?”.
- Si los avisos proactivos se califican como molestos, se bajan a uno al día y solo de nivel importante.

---

## Qué cambia en el cuadernillo

Estos puntos chocan con lo que dice hoy el cuadernillo y hay que decidir antes de la próxima entrega:

- **E2** dice que mirar poco la pantalla “no es una prueba automática de que la voz es la respuesta”. Ahora la voz es la hipótesis principal, respaldada por una entrevista.
- **E4** dice que Nort no es un “unificador total” y deja fuera la “automatización mágica de toda la agenda corporativa”. Ahora Nort es la capa central de consulta, aunque el MVP limita las integraciones a Google y siempre pide permiso para actuar.
- **Persona:** la usuaria entrevistada es estudiante universitaria; el caso de prueba es John, ingeniero. Conviene sumar una persona secundaria (estudiante) o explicar por qué John sigue siendo el actor principal.
