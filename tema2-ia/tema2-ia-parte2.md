---
marp: true
theme: ual
lang: es
size: 16:9
paginate: true
title: Tema 2 · Inteligencia artificial · Parte 2 · Modelos y manos a la obra
description: Universidad de Mayores · Universidad de Almería · Tecnologías digitales, usos, oportunidades y riesgos
header: 'Tema 2 · Inteligencia artificial · Parte 2'
footer: 'Tecnologías digitales · Universidad de Mayores · UAL'
---

<!-- _class: portada -->
<!-- _header: '' -->
<!-- _footer: '' -->

Tecnologías digitales · Tema 2

# Inteligencia artificial, sin miedo y con cabeza

## Parte 2 · Modelos y manos a la obra

Universidad de Mayores · Universidad de Almería

---

<!-- _class: pregunta -->

# ¿Os acordáis de cómo escribió la felicitación de Lucía?

Entre todos: ¿qué pasos seguía la máquina?

---

<!-- _class: pasos -->

# Lo que ya sabemos

1. **Aprende de ejemplos**: ajusta miles de millones de pesos
2. **Clasifica**: reparte su seguridad entre las palabras posibles
3. **Elige una**, la añade a la frase y vuelve a empezar
4. **Parecer probable no es ser verdad**: a veces se inventa cosas

---

# Una ayuda para el día a día

<div class="rejilla-3 compacta">
<div class="tarjeta"><span class="ico">📄</span><b>Entender papeles</b>«Explícame con palabras sencillas esta carta del banco»</div>
<div class="tarjeta sol"><span class="ico">🍲</span><b>En la cocina</b>«Tengo calabacín, huevos y queso. ¿Qué cocino para dos?»</div>
<div class="tarjeta tinta"><span class="ico">✈️</span><b>Viajes</b>«Planéame tres días por la Alpujarra, sin caminatas largas»</div>
<div class="tarjeta alerta"><span class="ico">🌍</span><b>Idiomas</b>Traducir un menú con la cámara o hablar con alguien en otro idioma</div>
<div class="tarjeta"><span class="ico">📝</span><b>Escribir</b>Una reclamación, un discurso para una boda, una felicitación</div>
<div class="tarjeta sol"><span class="ico">🎓</span><b>Aprender</b>«Explícame la Guerra de la Independencia como si fuera una historia»</div>
</div>
<div class="aviso">✋ Votad: el uso ganador lo probamos en directo.</div>

---

# ¿Quién está detrás? Estados Unidos

<div class="rejilla-4 compacta">
<div class="tarjeta"><b>ChatGPT</b>OpenAI · la más usada del mundo</div>
<div class="tarjeta sol"><b>Gemini</b>Google · dentro de Android y Gmail</div>
<div class="tarjeta tinta"><b>Copilot</b>Microsoft · en Windows, Word y Edge</div>
<div class="tarjeta alerta"><b>Meta AI</b>Meta · el círculo azul de WhatsApp</div>
<div class="tarjeta"><b>Claude</b>Anthropic · fuerte escribiendo y con textos largos</div>
<div class="tarjeta sol"><b>Grok</b>xAI · dentro de X, la antigua Twitter</div>
<div class="tarjeta tinta"><b>Siri</b>Apple · la nueva Siri con IA aún no ha llegado a la UE</div>
<div class="tarjeta velo"><span class="ico">📱</span><b>¿Y vosotros?</b>¿Cuáles tenéis ya en el móvil?</div>
</div>
<div class="aviso">💬 Todas tienen versión gratuita y se pueden usar hablando.</div>

---

# ¿Y en Europa?

<div class="rejilla-3">
<div class="tarjeta"><b>Mistral AI · Francia</b>Su asistente se llamaba Le Chat; desde mayo de 2026 se llama <strong>Vibe</strong>. La empresa vale más de 21.000 millones de euros.</div>
<div class="tarjeta sol"><b>DeepL · Alemania</b>El traductor automático europeo más conocido. Traduce textos, documentos y conversaciones.</div>
<div class="tarjeta tinta"><b>ALIA · España</b>Modelos <strong>públicos y abiertos</strong> del Barcelona Supercomputing Center, en español y en las lenguas cooficiales.</div>
</div>
<div class="aviso">📊 Estados Unidos lidera con mucha diferencia. Mistral es la gran apuesta europea.</div>

---

# Las empresas chinas

<div class="rejilla-3 compacta">
<div class="tarjeta alerta"><b>DeepSeek</b>Sorprendió en 2025 por bueno y barato. Hoy va por la V4.1</div>
<div class="tarjeta"><b>Qwen · Alibaba</b>Dueña de AliExpress. Sus modelos abiertos, de los más descargados</div>
<div class="tarjeta sol"><b>Kimi · Moonshot AI</b>Kimi K3 (2026): 2,8 billones de pesos, el abierto más grande</div>
<div class="tarjeta tinta"><b>Doubao · ByteDance</b>Dueña de TikTok. La app de IA más usada en China</div>
<div class="tarjeta"><b>GLM · Zhipu</b>Empresa joven con modelos abiertos de alto nivel</div>
<div class="tarjeta sol"><b>Ernie y Yuanbao</b>De Baidu y Tencent, gigantes de internet</div>
</div>
<div class="aviso">💡 Dos rasgos: son <strong>mucho más baratos</strong> y casi todos publican sus modelos <strong>en abierto</strong>.</div>

---

# Modelos cerrados y modelos abiertos

<div class="rejilla-2">
<div class="tarjeta tinta"><span class="ico">🔒</span><b>Cerrados</b>Solo se usan a través de la empresa, en su web o en su app. No sabemos ni cuántos pesos tienen.<span style="display:block;margin-top:12px;color:var(--ual);font-weight:800">Ej.: ChatGPT, Gemini, Claude</span></div>
<div class="tarjeta sol"><span class="ico">📖</span><b>Abiertos</b>Publican los pesos: cualquiera puede descargarlos y usarlos en su propio ordenador.<span style="display:block;margin-top:12px;color:var(--ual);font-weight:800">Ej.: Mistral, DeepSeek, Qwen, Kimi, ALIA</span></div>
</div>
<div class="aviso">🍰 El secreto de la casa frente a la receta publicada… aunque casi nunca publican con qué textos aprendieron.</div>

---

<!-- _class: pasos -->

# ¿Occidente o China? Cuatro preguntas

1. ¿**Dónde** se guardan mis datos?
2. ¿Cumple las **normas europeas**?
3. ¿Qué **temas evita** o contesta a medias?
4. ¿**Quién** lo pone en marcha: la empresa o un tercero?

---

# ¿Dónde funcionan? Depende del tamaño

<div class="rejilla-3">
<div class="tarjeta con-foto contener"><img src="img/fotos/iphone4s.jpg" style="height:130px"><b>En el móvil</b><p>Modelos pequeños. Funcionan sin internet.</p></div>
<div class="tarjeta con-foto contener sol"><img src="img/fotos/portatil.jpg" style="height:130px"><b>En un ordenador</b><p>Medianos. Lo que preguntas no sale de casa.</p></div>
<div class="tarjeta con-foto tinta"><img src="img/fotos/centrodatos.jpg" style="height:130px"><b>En un centro de datos</b><p>Los grandes: más de un billón de pesos.</p></div>
</div>
<div class="aviso">📚 El grande sabe más, pero es más lento, más caro y gasta más luz y agua.</div>
<div class="credito">Fotos: Zach Vega (CC BY-SA 3.0) · André Karwath (CC BY-SA 4.0) · BalticServers.com (CC BY-SA 3.0) · Wikimedia Commons</div>

---

# La memoria de una conversación

![w:900](img/s2-contexto.svg)

<div class="aviso">💡 Si se alarga mucho, olvida el principio: para otro tema, conversación nueva.</div>

---

# Modelos que piensan antes de hablar

<div class="dos">
<div class="tarjeta"><span class="ico">⚡</span><b>Modo rápido</b>Contesta de corrido, palabra a palabra. Ideal para charlar, escribir o traducir.</div>
<div class="tarjeta sol"><span class="ico">🧠</span><b>Modo razonamiento</b>Antes de responder escribe un borrador paso a paso, y a veces nos deja verlo. Tarda más, pero se equivoca menos con problemas y cuentas.</div>
</div>
<div class="aviso">🔎 En las apps aparece como «Pensar», «Razonar» o «Pensamiento profundo».</div>

---

<!-- _class: pregunta -->

# Si 3 gallinas ponen 3 huevos en 3 días, ¿cuántos huevos ponen 6 gallinas en 6 días?

Primero vosotros. Luego, la IA en modo rápido y en modo razonamiento.

---

# Ve, oye y lee: todo son trocitos

![w:1110](img/s2-multimodal.svg)

---

# …y dibuja: de ruido a imagen

<div class="flujo">
<figure class="foto" style="flex:1"><img src="img/fotos/difusion-0.jpg"><figcaption>Ruido</figcaption></figure>
<div class="flecha">➜</div>
<figure class="foto" style="flex:1"><img src="img/fotos/difusion-1.jpg"><figcaption>Paso a paso…</figcaption></figure>
<div class="flecha">➜</div>
<figure class="foto" style="flex:1"><img src="img/fotos/difusion-2.jpg"><figcaption>…limpia…</figcaption></figure>
<div class="flecha">➜</div>
<figure class="foto" style="flex:1"><img src="img/fotos/difusion-3.jpg"><figcaption>…y limpia</figcaption></figure>
<div class="flecha">➜</div>
<figure class="foto" style="flex:1"><img src="img/fotos/difusion-4.jpg"><figcaption><span class="ok">La Alcazaba</span></figcaption></figure>
</div>

<div class="dos" style="margin-top:22px;font-size:27px;align-items:start">
<div class="tarjeta velo"><b>Para aprender</b>A millones de fotos se les añade ruido, y el modelo aprende a quitarlo.</div>
<div class="tarjeta sol"><b>Para crear</b>Parte de puro ruido y lo limpia poco a poco, guiado por lo que le pedimos.</div>
</div>
<div class="credito">Foto: Jebulon · CC0 · Wikimedia Commons · Ruido añadido para ilustrar el proceso</div>

---

# Una ayuda que llega más lejos

<div class="rejilla-4">
<div class="tarjeta con-foto" ><img src="img/fotos/radiografia.jpg"><b>Salud</b><p>Lee radiografías. Ayuda al médico, no lo sustituye.</p></div>
<div class="tarjeta con-foto sol" ><div class="emoji-foto">🔊</div><b>Accesibilidad</b><p>Lee en voz alta, subtitula y describe fotos.</p></div>
<div class="tarjeta con-foto tinta" ><img src="img/fotos/invernaderos.jpg"><b>Invernaderos</b><p>Riego justo y plagas a tiempo. ¡Aquí al lado!</p></div>
<div class="tarjeta con-foto alerta" ><div class="emoji-foto">📸</div><b>Recuerdos</b><p>Restaurar fotos antiguas y escribir memorias.</p></div>
</div>
<div class="credito">Fotos: Stillwaterising (CC0) · Carlosjvives (CC BY 4.0) · Wikimedia Commons</div>

---

# Cómo pedirle las cosas: la fórmula

<div class="rejilla-4">
<div class="tarjeta"><b>1 · Quién</b>«Actúa como un guía turístico paciente…»</div>
<div class="tarjeta sol"><b>2 · Qué</b>«…recomiéndame qué visitar en Granada…»</div>
<div class="tarjeta tinta"><b>3 · Contexto</b>«…voy un día con mi marido, que usa bastón…»</div>
<div class="tarjeta alerta"><b>4 · Formato</b>«…dámelo en una lista corta, con horarios»</div>
</div>

<div class="dos" style="margin-top:24px">
<div class="tarjeta velo"><b>😕 Pregunta pobre</b>«Qué ver en Granada»</div>
<div class="tarjeta destacada"><b>😃 Pregunta rica</b>Cuanto más contexto, más pistas para predecir bien. Y se le puede pedir que lo cambie.</div>
</div>

---

# 🎬 Demostración en directo

<div class="dos" style="align-items:start">
<div style="font-size:28px">
<ol><li>«Tengo huevos y patatas: ¿qué ceno?»</li><li>«Explícame el IBI con un ejemplo»</li><li>«Un poema para unas bodas de oro»</li><li>«¿Cómo se dice farmacia en inglés?»</li><li><strong>La vuestra</strong>: la más votada</li></ol>
</div>
<div class="tarjeta alerta"><span class="ico">👀</span><b>Para terminar</b>Le preguntaremos por la historia de un pueblo pequeño de Almería… y veremos si se inventa cosas.</div>
</div>

---

# Ahora vosotros: tareas por parejas

<div class="rejilla-3">
<div class="tarjeta"><b>Nivel 1 · Empezar</b><ul><li>Abrid Gemini, ChatGPT o Meta AI</li><li>Por voz: «¿Qué es un LLM?»</li><li>Foto a algo: «¿Qué es?»</li></ul></div>
<div class="tarjeta sol"><b>Nivel 2 · Usarla</b><ul><li>La carta: «Explícamela fácil»</li><li>Cabo de Gata, sin fórmula y con ella</li><li>«¿Cómo agrando la letra?»</li></ul></div>
<div class="tarjeta tinta"><b>Nivel 3 · Pillarla</b><ul><li>Caza una alucinación sobre tu pueblo</li><li>Misma pregunta a dos IA</li><li>«Hazme 3 preguntas tipo test»</li></ul></div>
</div>
<div class="aviso">📄 Las tareas completas están en la hoja. Quien acabe un nivel, ayuda a su pareja.</div>

---

<!-- _class: pregunta -->

# ¿Qué os ha funcionado? ¿Dónde se ha equivocado?

Apuntad las alucinaciones que hayáis cazado: con ellas empieza la parte 3.

---

<!-- _class: resumen -->

# Resumen de hoy

1. Hay **muchas IA y muchas empresas**: EE. UU., Europa y China
2. **Abiertas o cerradas**, pequeñas o enormes: cada una tiene su sitio
3. Ven, oyen y dibujan: **todo son trocitos**
4. Preguntar bien es **la mitad del trabajo**… y aun así **se equivoca**

**Para casa:** terminad dos tareas de la hoja que no os haya dado tiempo.

---

<!-- _class: cierre -->
<!-- _header: '' -->
<!-- _footer: '' -->

Tema 2 · Inteligencia artificial

# ¡Gracias!

## En la parte 3: los riesgos, y cómo no dejarse engañar
