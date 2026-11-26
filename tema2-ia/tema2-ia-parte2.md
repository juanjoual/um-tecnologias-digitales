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

<style>
.credito { bottom: 74px; }
.barras.grandes.modelos .barra { grid-template-columns: 340px 1fr 70px; }
.barras.grandes.modelos .barra small { display: block; font-size: 20px; font-weight: 600; color: var(--texto-suave); margin-top: -2px; }
.barras.ranking { gap: 1px; margin-top: 0; }
.barras.ranking .barra { grid-template-columns: 450px 1fr 56px; font-size: 22px; line-height: 1.2; }
.barras.ranking .barra .pista { height: 15px; }
.miniaturas { display: flex; gap: 16px; justify-content: center; margin-top: 6px; }
.miniaturas figure { flex: 1; margin: 0; text-align: center; }
.miniaturas img { height: 255px; width: auto; max-width: 100%; object-fit: contain; border: 1px solid #c9d3de; box-shadow: 0 2px 6px rgba(0,0,0,.12); }
.miniaturas figcaption { font-size: 24px; font-weight: 800; color: var(--ual-tinta); margin-top: 8px; }
.medallas { display: grid; grid-template-columns: repeat(3, 1fr); gap: 22px; margin-top: 8px; }
.medalla { background: #fff; border-radius: 18px; padding: 20px 22px 18px; box-shadow: 0 2px 10px rgba(0,0,0,.08); border-top: 8px solid var(--ual); text-align: center; }
.medalla .puesto { font-size: 84px; font-weight: 900; line-height: 1; color: var(--ual-tinta); }
.medalla .puesto small { font-size: 34px; }
.medalla b { display: block; font-size: 30px; margin-top: 8px; color: var(--ual-tinta); }
.medalla span { display: block; font-size: 23px; color: var(--texto-suave); margin-top: 4px; line-height: 1.25; }
.medalla.oro { border-top-color: var(--sol); }
.medalla.gris { border-top-color: #9aa7b4; }
.medalla.gris .puesto { color: #7d8a97; }
.trozos { position: relative; display: inline-block; justify-self: center; width: fit-content; }
.trozos img { display: block; height: 330px; border-radius: 10px; }
.trozos::after { content: ""; position: absolute; inset: 0; border-radius: 10px;
  background-image: linear-gradient(rgba(255,255,255,.9) 2px, transparent 2px), linear-gradient(90deg, rgba(255,255,255,.9) 2px, transparent 2px);
  background-size: 55px 55px; }
.receta .pieza { font-weight: 800; padding: 1px 0; border-radius: 4px; }
.p1 { background: #dfe9f5; } .p2 { background: #fbe9c8; } .p3 { background: #e3efe4; } .p4 { background: #f6dcd5; }
.leyenda { display: flex; gap: 14px; justify-content: center; margin-top: 14px; font-size: 22px; font-weight: 700; }
.leyenda span { padding: 3px 12px; border-radius: 8px; }
</style>

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

# Ojo con la etiqueta «con IA»

<div class="rejilla-3">
<div class="tarjeta"><span class="ico">🧺</span><b>En casa</b>A veces, «con IA» solo quiere decir que la lavadora pesa la ropa y elige un programa, como hace años.</div>
<div class="tarjeta sol"><span class="ico">☎️</span><b>Contestadores</b>«Pulse 1 para…» es un menú con reglas fijas, no una IA.</div>
<div class="tarjeta alerta"><span class="ico">💸</span><b>Inversiones</b>En 2024, el regulador de la bolsa de EE. UU. multó con 400.000&nbsp;$ a dos asesoras que decían usar IA y no la usaban.</div>
</div>
<div class="aviso">🔎 Si aprende de ejemplos, es IA. Si solo sigue reglas fijas, es un programa de siempre.</div>

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
<div class="tarjeta sol"><b>Grok</b>SpaceXAI, antes xAI · dentro de X</div>
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

<!-- _class: pregunta -->

# ¿Alguien tiene DeepSeek o alguna app china en el móvil?

¿Para qué la usáis? ¿Sabíais dónde van vuestros datos?

---

# Modelos cerrados y modelos abiertos

<div class="rejilla-2">
<div class="tarjeta tinta"><span class="ico">🔒</span><b>Cerrados</b>Solo se usan a través de la empresa, en su web o en su app. No sabemos ni cuántos pesos tienen.<span style="display:block;margin-top:12px;color:var(--ual);font-weight:800">Ej.: ChatGPT, Gemini, Claude</span></div>
<div class="tarjeta sol"><span class="ico">📖</span><b>Abiertos</b>Publican los pesos: cualquiera puede descargarlos y usarlos en su propio ordenador.<span style="display:block;margin-top:12px;color:var(--ual);font-weight:800">Ej.: Mistral, DeepSeek, Qwen, Kimi, ALIA</span></div>
</div>
<div class="aviso">⚖️ Recordad: los <strong>pesos</strong> son los miles de millones de números que la IA ajusta mientras aprende. En ellos está todo lo que «sabe».</div>

---

<!-- _class: pasos -->

# ¿Occidente o China? Cuatro preguntas

1. ¿**Dónde** se guardan mis datos?
2. ¿Cumple las **normas europeas**?
3. ¿Qué **temas evita** o contesta a medias?
4. ¿**Quién** lo pone en marcha: la empresa o un tercero?

---

# 1 · ¿Dónde se guardan mis datos?

<div class="rejilla-3">
<div class="tarjeta tinta"><span class="ico">🇺🇸</span><b>ChatGPT, Gemini, Claude</b>Sobre todo en Estados Unidos, con sus leyes.</div>
<div class="tarjeta sol"><span class="ico">🇪🇺</span><b>Mistral</b>En Europa, con las leyes europeas de protección de datos.</div>
<div class="tarjeta alerta"><span class="ico">🇨🇳</span><b>DeepSeek y las apps chinas</b>En China, donde la ley obliga a las empresas a colaborar con el Estado si se lo pide.</div>
</div>
<div class="aviso">🚫 En 2025, Italia bloqueó la app de DeepSeek: no supo explicar qué datos guardaba ni dónde.</div>

---

<!-- _class: pregunta -->

# ¿Os preocupa dónde acaban vuestras conversaciones?

Levantad la mano: mucho, poco o nada.

---

# 2 · ¿Cumple las normas europeas?

<div class="rejilla-3">
<div class="tarjeta"><span class="ico">🔐</span><b>Vuestros datos</b>El Reglamento de Protección de Datos los protege desde 2018, venga de donde venga la app.</div>
<div class="tarjeta sol"><span class="ico">⚖️</span><b>La ley de IA</b>Desde agosto de 2025, los grandes modelos tienen que explicar cómo se han hecho.</div>
<div class="tarjeta tinta"><span class="ico">✍️</span><b>El código europeo</b>Lo firmaron OpenAI, Anthropic, Google, Microsoft y Mistral. Meta no; Grok, solo en parte.</div>
</div>
<div class="aviso">🇮🇹 DeepSeek le dijo a Italia que las leyes europeas no iban con ella. Italia le cerró la puerta.</div>

---

# 3 · ¿Qué temas evita?

<div class="dos" style="align-items:center">
<div class="chat">
<div class="burbuja yo">¿Qué pasó en la plaza de Tiananmen en 1989?</div>
<div class="burbuja ia mal">Lo siento, eso está fuera de mi alcance. Hablemos de otra cosa.</div>
</div>
<div class="tarjeta alerta"><span class="ico">🤐</span><b>Lo que contestó DeepSeek</b>Las apps chinas esquivan los temas incómodos para su Gobierno: Tiananmen, Taiwán, las minorías…</div>
</div>
<div class="aviso">🔎 Las occidentales también tienen sus normas. En política, comparad siempre con otra fuente.</div>

---

# 4 · ¿Quién lo pone en marcha?

<div class="cadena">
<div class="tarjeta"><span class="ico">📖</span><b>Un modelo abierto</b>Por ejemplo, Kimi o DeepSeek: sus pesos se pueden descargar</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🏢</span><b>Una empresa europea</b>Lo descarga y lo pone en marcha en sus propios ordenadores</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">🇪🇺</span><b>Vuestros datos</b>No salen de Europa, aunque el modelo sea chino</div>
</div>
<div class="aviso">⚠️ La app oficial china y el mismo modelo en Europa no son lo mismo. Eso sí: lo que el modelo calla, lo sigue callando.</div>

---

<!-- _class: pregunta -->

# ¿Alguien paga ya por alguna IA?

¿Cuál? ¿Cuánto? ¿Para qué la usáis?

---

# ¿Gratis o de pago?

<div class="rejilla-3">
<div class="tarjeta velo"><span class="ico">🆓</span><b>Gratis</b>Todas tienen versión gratis, con límites al día y a veces un modelo más pequeño.</div>
<div class="tarjeta sol"><span class="ico">🪙</span><b>De 5 a 10&nbsp;€ al mes</b>Google AI Plus: 4,99&nbsp;€. ChatGPT Go: unos 8–10&nbsp;€. Más uso y mejores modelos.</div>
<div class="tarjeta tinta"><span class="ico">💎</span><b>Unos 20&nbsp;€ al mes</b>Google AI Pro: 21,99&nbsp;€. Claude Pro: unos 22&nbsp;€. ChatGPT Plus: 23&nbsp;€. Lo más nuevo.</div>
</div>
<div class="aviso">💡 Para preguntar, escribir o traducir, la versión gratis suele bastar.</div>

---

# ¿Cuál es la más lista? Las clasificaciones

<div class="cadena">
<div class="tarjeta"><span class="ico">📝</span><b>Mismo examen</b>Una empresa independiente, Artificial Analysis, pone las mismas pruebas a todas</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🧮</span><b>Una nota</b>Razonar, ciencia, programar, leer documentos largos…</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">🏆</span><b>Un ranking</b>Público y gratuito, en artificialanalysis.ai</div>
</div>
<div class="aviso">⚠️ Mide exámenes, no si os entiende a vosotros. La mejor es la que os sirve.</div>

---

# Cada empresa tiene una familia de modelos

<div class="rejilla-3">
<div class="tarjeta tinta"><span class="ico">🐘</span><b>El grande</b>El más listo. Más lento y más caro: a veces solo está en la versión de pago.</div>
<div class="tarjeta sol"><span class="ico">🐎</span><b>El mediano</b>Para el día a día: bastante listo y bastante rápido.</div>
<div class="tarjeta"><span class="ico">🐇</span><b>El pequeño</b>Rápido y barato. Algunos caben en el móvil.</div>
</div>
<div class="aviso">🎚️ A casi todos se les puede pedir que piensen más: sacan mejor nota, pero tardan más.</div>

---

<!-- _class: pregunta -->

# Calculad de cabeza: 17 × 24

¿Y con un papel? A la IA le pasa lo mismo.

---

# ¿Qué es «pensar» para una IA?

<div class="cadena">
<div class="tarjeta"><span class="ico">❓</span><b>1 · Lee la pregunta</b>«17 × 24, ¿cuánto es?»</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">📝</span><b>2 · Escribe un borrador</b>«17 × 20 = 340; 17 × 4 = 68; 340 + 68 = 408. Lo compruebo…»</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">✅</span><b>3 · Contesta</b>Con lo que ha sacado en limpio: «408»</div>
</div>
<div class="aviso">💡 No piensa como nosotros: sigue escribiendo palabras, pero primero para sí misma, como quien hace la cuenta en un papel.</div>

---

# Modelos que piensan antes de hablar

<div class="dos">
<div class="tarjeta"><span class="ico">⚡</span><b>Modo rápido</b>Contesta de corrido, palabra a palabra. Ideal para charlar, escribir o traducir.</div>
<div class="tarjeta sol"><span class="ico">🧠</span><b>Modo razonamiento</b>Antes de responder escribe un borrador paso a paso, y a veces nos deja verlo. Tarda más, pero se equivoca menos con problemas y cuentas.</div>
</div>
<div class="aviso">🎚️ En las apps aparece como «Pensar» o «Thinking». Cuanto más esfuerzo, más borrador: mejor respuesta, pero tarda más.</div>

---

# ¿Dónde funcionan? Depende del tamaño

<div class="rejilla-3">
<div class="tarjeta con-foto contener"><img src="img/fotos/iphone4s.jpg" style="height:130px"><b>En el móvil</b><p>Modelos pequeños. Funcionan sin internet.</p></div>
<div class="tarjeta con-foto contener sol"><img src="img/fotos/portatil.jpg" style="height:130px"><b>En un ordenador</b><p>Medianos. Lo que preguntáis no sale de casa.</p></div>
<div class="tarjeta con-foto tinta"><img src="img/fotos/centrodatos.jpg" style="height:130px"><b>En un centro de datos</b><p>Los grandes: más de un billón de pesos.</p></div>
</div>
<div class="aviso">📚 El grande sabe más, pero es más lento, más caro y gasta más energía.</div>
<div class="credito">Fotos: Zach Vega (CC BY-SA 3.0) · André Karwath (CC BY-SA 4.0) · BalticServers.com (CC BY-SA 3.0) · Wikimedia Commons</div>

---

<!-- _class: pregunta -->

# ¿Sabéis qué modelo hay detrás de vuestra app?

Abridla y mirad arriba, junto al nombre: suele poner cuál es y deja cambiarlo.

---

# Anthropic · Claude

<div class="barras grandes modelos">
<div class="barra top"><span>Claude Fable 5.2<small>El más potente · noviembre</small></span><span class="pista"><i style="width:93%"></i></span><span class="pc">65</span></div>
<div class="barra"><span>Claude Opus 5.5<small>El grande</small></span><span class="pista"><i style="width:84%"></i></span><span class="pc">59</span></div>
<div class="barra"><span>Claude Sonnet 5.5<small>El mediano</small></span><span class="pista"><i style="width:79%"></i></span><span class="pc">55</span></div>
<div class="barra"><span>Claude Haiku 5.5<small>El pequeño y rápido</small></span><span class="pista"><i style="width:53%"></i></span><span class="pc">37</span></div>
</div>
<div class="aviso">🔒 Fable tiene un gemelo, Mythos: el mismo modelo, con otras normas de uso. Ahora vemos por qué.</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

# Fable y Mythos: dos puertas

<div class="rejilla-3">
<div class="tarjeta alerta"><span class="ico">💻</span><b>Por qué la informática</b>Encontró miles de fallos graves que nadie conocía, uno de ellos escondido 27 años. Lo que sirve para tapar un agujero sirve para colarse por él.</div>
<div class="tarjeta"><span class="ico">🧬</span><b>Por qué la biología</b>En algunas tareas de laboratorio supera a los expertos. En malas manos, podría ayudar a fabricar un arma biológica.</div>
<div class="tarjeta tinta"><span class="ico">🔑</span><b>Dos puertas</b><strong>Fable</strong>, para todos: en esos temas pasa la pregunta a otro modelo. <strong>Mythos</strong>, sin esos frenos, solo para quien defiende sistemas.</div>
</div>
<div class="aviso">🩺 Las preguntas de salud del día a día, Fable las contesta con normalidad.</div>

---

# OpenAI · ChatGPT

<div class="barras grandes modelos">
<div class="barra top"><span>GPT-6.2 Astra<small>El grande · para lo más difícil</small></span><span class="pista"><i style="width:89%"></i></span><span class="pc">62</span></div>
<div class="barra"><span>GPT-6.2 Sol<small>El mediano · rápido y capaz</small></span><span class="pista"><i style="width:81%"></i></span><span class="pc">57</span></div>
<div class="barra"><span>GPT-6.1 Terra<small>Más rápido y barato · de octubre</small></span><span class="pista"><i style="width:73%"></i></span><span class="pc">51</span></div>
<div class="barra"><span>GPT-6 Luna<small>El pequeño · el de la cuenta gratis</small></span><span class="pista"><i style="width:40%"></i></span><span class="pc">28</span></div>
</div>
<div class="aviso">🗓️ Astra y Sol se estrenaron el 17 de noviembre; Terra, el 26 de octubre. Los nombres cambian cada pocos meses.</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

# Google · Gemini

<div class="barras grandes modelos">
<div class="barra top"><span>Gemini 4 Neon<small>El mediano, pensando a tope</small></span><span class="pista"><i style="width:89%"></i></span><span class="pc">62</span></div>
<div class="barra"><span>Gemini 4 Carbon<small>El más potente · solo en el plan Ultra</small></span><span class="pista"><i style="width:86%"></i></span><span class="pc">60</span></div>
<div class="barra"><span>Gemini 4 Hydrogen<small>El rápido, para el día a día</small></span><span class="pista"><i style="width:77%"></i></span><span class="pc">54</span></div>
<div class="barra"><span>Gemini 4 Argon<small>El más ligero de los grandes</small></span><span class="pista"><i style="width:73%"></i></span><span class="pc">51</span></div>
</div>
<div class="aviso">🎚️ Neon es el mediano, pero si se le deja pensar más que a Carbon, saca más nota.</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

<!-- _class: pregunta -->

# Para entender la carta del banco, ¿hace falta el modelo más grande?

¿Grande, mediano o pequeño? Votad y lo probamos.

---

# Meta y Grok

<div class="barras grandes modelos">
<div class="barra top"><span>Muse Wonder Full<small>Meta · el grande, de octubre</small></span><span class="pista"><i style="width:71%"></i></span><span class="pc">50</span></div>
<div class="barra"><span>Muse Wonder<small>Meta · su hermano menor</small></span><span class="pista"><i style="width:63%"></i></span><span class="pc">44</span></div>
<div class="barra"><span>Grok 4.7<small>SpaceXAI · la empresa de Elon Musk</small></span><span class="pista"><i style="width:50%"></i></span><span class="pc">35</span></div>
</div>
<div class="aviso">🚀 xAI, la empresa de Grok, forma parte de SpaceX desde mayo y ahora se llama SpaceXAI.</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

# Europa y China

<div class="barras grandes modelos" style="gap:0">
<div class="barra top"><span>Kimi K3.1 Pro<small>Moonshot · China · abierto</small></span><span class="pista"><i style="width:67%"></i></span><span class="pc">47</span></div>
<div class="barra"><span>Qwen4-Max<small>Alibaba · China · cerrado</small></span><span class="pista"><i style="width:61%"></i></span><span class="pc">43</span></div>
<div class="barra"><span>Hy4<small>Tencent · China · abierto</small></span><span class="pista"><i style="width:50%"></i></span><span class="pc">35</span></div>
<div class="barra"><span>DeepSeek V4.1 Flash<small>China · abierto y muy barato</small></span><span class="pista"><i style="width:46%"></i></span><span class="pc">32</span></div>
<div class="barra"><span>Mistral Large 4<small>Francia · abierto</small></span><span class="pista"><i style="width:37%"></i></span><span class="pc">26</span></div>
</div>
<div class="aviso">🌍 De los abiertos, el mejor es chino. El mejor europeo, Mistral, va bastante más atrás.</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

<!-- _class: pregunta -->

# ¿Quién creéis que va primero en la clasificación general?

Anthropic, OpenAI, Google o los chinos: votad antes de verla.

---

# La clasificación general · del 1 al 12

<div class="barras ranking">
<div class="barra top"><span>1. Claude Fable 5.2 · Anthropic</span><span class="pista"><i style="width:93%;background:var(--sol)"></i></span><span class="pc">65</span></div>
<div class="barra"><span>2. GPT-6.2 Astra · OpenAI</span><span class="pista"><i style="width:89%;background:var(--ual-tinta)"></i></span><span class="pc">62</span></div>
<div class="barra"><span>3. Gemini 4 Neon · Google</span><span class="pista"><i style="width:89%;background:var(--ual)"></i></span><span class="pc">62</span></div>
<div class="barra"><span>4. Gemini 4 Carbon · Google</span><span class="pista"><i style="width:86%;background:var(--ual)"></i></span><span class="pc">60</span></div>
<div class="barra"><span>5. Claude Opus 5.5 · Anthropic</span><span class="pista"><i style="width:84%;background:var(--sol)"></i></span><span class="pc">59</span></div>
<div class="barra"><span>6. GPT-6.2 Sol · OpenAI</span><span class="pista"><i style="width:81%;background:var(--ual-tinta)"></i></span><span class="pc">57</span></div>
<div class="barra"><span>7. Claude Sonnet 5.5 · Anthropic</span><span class="pista"><i style="width:79%;background:var(--sol)"></i></span><span class="pc">55</span></div>
<div class="barra"><span>8. Gemini 4 Hydrogen · Google</span><span class="pista"><i style="width:77%;background:var(--ual)"></i></span><span class="pc">54</span></div>
<div class="barra"><span>9. GPT-6.1 Terra · OpenAI</span><span class="pista"><i style="width:73%;background:var(--ual-tinta)"></i></span><span class="pc">51</span></div>
<div class="barra"><span>10. Gemini 4 Argon · Google</span><span class="pista"><i style="width:73%;background:var(--ual)"></i></span><span class="pc">51</span></div>
<div class="barra"><span>11. Muse Wonder Full · Meta</span><span class="pista"><i style="width:71%;background:#8a9bb0"></i></span><span class="pc">50</span></div>
<div class="barra"><span>12. Kimi K3.1 Pro · China, abierto</span><span class="pista"><i style="width:67%;background:var(--alerta)"></i></span><span class="pc">47</span></div>
</div>
<div class="credito">Artificial Analysis Intelligence Index v5 · cada modelo con su mejor ajuste · 25 de noviembre de 2026</div>

---

# La clasificación general · del 13 al 24

<div class="barras ranking">
<div class="barra"><span>13. Muse Wonder · Meta</span><span class="pista"><i style="width:63%;background:#8a9bb0"></i></span><span class="pc">44</span></div>
<div class="barra"><span>14. Qwen4-Max · Alibaba, China</span><span class="pista"><i style="width:61%;background:var(--alerta)"></i></span><span class="pc">43</span></div>
<div class="barra"><span>15. Claude Haiku 5.5 · Anthropic</span><span class="pista"><i style="width:53%;background:var(--sol)"></i></span><span class="pc">37</span></div>
<div class="barra"><span>16. Muse Ember · Meta</span><span class="pista"><i style="width:51%;background:#8a9bb0"></i></span><span class="pc">36</span></div>
<div class="barra"><span>17. Grok 4.7 · SpaceXAI</span><span class="pista"><i style="width:50%;background:#6f8f7a"></i></span><span class="pc">35</span></div>
<div class="barra"><span>18. Hy4 · Tencent, China</span><span class="pista"><i style="width:50%;background:var(--alerta)"></i></span><span class="pc">35</span></div>
<div class="barra"><span>19. DeepSeek V4.1 Flash · China</span><span class="pista"><i style="width:46%;background:var(--alerta)"></i></span><span class="pc">32</span></div>
<div class="barra"><span>20. GLM-5.3 · Z.ai, China</span><span class="pista"><i style="width:46%;background:var(--alerta)"></i></span><span class="pc">32</span></div>
<div class="barra"><span>21. Inkling 2 Small · Thinking Machines</span><span class="pista"><i style="width:44%;background:#6f8f7a"></i></span><span class="pc">31</span></div>
<div class="barra"><span>22. MiMo-V2.6-Pro · Xiaomi, China</span><span class="pista"><i style="width:43%;background:var(--alerta)"></i></span><span class="pc">30</span></div>
<div class="barra"><span>23. Ling 3.1 Flash · Ant Group, China</span><span class="pista"><i style="width:43%;background:var(--alerta)"></i></span><span class="pc">30</span></div>
<div class="barra"><span>24. MiniMax-M3.1-Flash · China</span><span class="pista"><i style="width:41%;background:var(--alerta)"></i></span><span class="pc">29</span></div>
</div>
<div class="aviso" style="margin-top:6px;padding-top:6px;padding-bottom:6px">⬇️ Más abajo: 28.º GPT-6 Luna (OpenAI) · 31.º Mistral Large 4, el mejor europeo</div>
<div class="credito">Artificial Analysis Intelligence Index v5 · cada modelo con su mejor ajuste · 25 de noviembre de 2026</div>

---

# Lo que nos dice la clasificación

<div class="rejilla-4">
<div class="tarjeta"><span class="ico">🇺🇸</span><b>Tres en cabeza</b>Anthropic, OpenAI y Google, separadas por pocos puntos</div>
<div class="tarjeta alerta"><span class="ico">🇨🇳</span><b>El mejor abierto</b>Es chino, Kimi K3.1 Pro: 12.º, a 18 puntos del primero</div>
<div class="tarjeta sol"><span class="ico">🎚️</span><b>Pensar sube la nota</b>Claude Fable 5.2 saca 56 con esfuerzo medio y 65 a tope</div>
<div class="tarjeta tinta"><span class="ico">🐇</span><b>Los pequeños</b>Sacan menos nota, pero son rápidos y baratos, y a menudo bastan</div>
</div>
<div class="aviso">📏 En octubre cambió el examen: las notas de antes no se pueden comparar con las de ahora.</div>

---

# El primer puesto cambia cada pocas semanas

<div class="rejilla-4">
<div class="tarjeta"><b>9 de septiembre</b>GPT-6 Astra empata<br><small>OpenAI</small></div>
<div class="tarjeta sol"><b>22 de septiembre</b>Claude Opus 5.5<br><small>Anthropic</small></div>
<div class="tarjeta tinta"><b>28 de octubre</b>Gemini 4 Carbon<br><small>Google</small></div>
<div class="tarjeta alerta"><b>9 de noviembre</b>Claude Fable 5.2<br><small>Anthropic</small></div>
</div>
<div class="aviso">⏱️ Cuatro cambios en dos meses. Y el 17 de noviembre llegó GPT-6.2 Astra, a solo 3 puntos.</div>

---

# Con vuestra cuenta de la UAL, Gemini gratis

<div class="medallas" style="grid-template-columns:repeat(2,1fr);width:820px;align-self:center">
<div class="medalla oro"><div class="puesto">3.<small>º</small></div><b>Gemini 4 Neon</b><span>El que más piensa. A 3 puntos del primero del mundo</span></div>
<div class="medalla"><div class="puesto">8.<small>º</small></div><b>Gemini 4 Hydrogen</b><span>El rápido, para el día a día</span></div>
</div>
<div class="aviso">🔑 Entrad en gemini.google.com con vuestra cuenta <strong>@inlumine.ual.es</strong>: es privada y no se usa para entrenar la IA.</div>
<div class="credito">Puestos en el índice de Artificial Analysis (v5), un modelo por fila · 25 de noviembre de 2026</div>

---

# ¿Y gratis en otras apps?

<div class="medallas">
<div class="medalla oro"><div class="puesto">7.<small>º</small></div><b>Claude · Sonnet 5.5</b><span>Con cuenta gratis de Claude, con un límite cada cinco horas</span></div>
<div class="medalla gris"><div class="puesto">28.<small>º</small></div><b>ChatGPT · GPT-6 Luna</b><span>El pequeño de OpenAI. Con el botón «Pensar», mejora</span></div>
<div class="medalla gris"><div class="puesto" style="font-size:60px;line-height:84px">+35.<small>º</small></div><b>Mistral · Medium 3.5</b><span>El de la app Vibe gratis. Va muy por detrás</span></div>
</div>
<div class="aviso">💡 Gratis no es lo mismo en todas: el modelo que os toca cambia mucho de una app a otra.</div>
<div class="credito">Puestos en el índice de Artificial Analysis (v5), un modelo por fila · 25 de noviembre de 2026</div>

---

# Lo que tenéis gratis, frente al primero

<div class="barras grandes modelos">
<div class="barra"><span>Claude Fable 5.2<small>El primero del mundo · de pago</small></span><span class="pista"><i style="width:93%;background:#c9d3de"></i></span><span class="pc">65</span></div>
<div class="barra top"><span>Gemini 4 Neon<small>Gratis con la cuenta de la UAL</small></span><span class="pista"><i style="width:89%;background:var(--ual)"></i></span><span class="pc">62</span></div>
<div class="barra"><span>Claude Sonnet 5.5<small>Gratis en Claude</small></span><span class="pista"><i style="width:79%;background:var(--sol)"></i></span><span class="pc">55</span></div>
<div class="barra"><span>Gemini 4 Hydrogen<small>Gratis con la cuenta de la UAL</small></span><span class="pista"><i style="width:77%;background:var(--ual)"></i></span><span class="pc">54</span></div>
<div class="barra"><span>GPT-6 Luna<small>Gratis en ChatGPT</small></span><span class="pista"><i style="width:40%;background:var(--ual-tinta)"></i></span><span class="pc">28</span></div>
<div class="barra"><span>Mistral Medium 3.5<small>Gratis en Vibe</small></span><span class="pista"><i style="width:7%;background:var(--alerta)"></i></span><span class="pc">5</span></div>
</div>
<div class="credito">Nota en el índice de Artificial Analysis (v5), con el máximo esfuerzo · 25 de noviembre de 2026</div>

---

<!-- _class: pregunta -->

# ¿Qué modelo utilizáis en el día a día?

¿Y para qué lo usáis?

---

# El contexto: la memoria de una conversación

![w:900](img/s2-contexto.svg)

<div class="aviso">💡 El <strong>contexto</strong> es todo lo que hay en la conversación: lo que escribís, lo que contesta, las fotos y los documentos.</div>

---

# Cada vez que escribís, lo relee todo

<div class="cadena">
<div class="tarjeta"><span class="ico">📜</span><b>1 · Lo junta todo</b>La conversación entera, desde el primer mensaje, más vuestra pregunta nueva</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🔁</span><b>2 · Lo vuelve a leer</b>Entre un mensaje y otro no recuerda nada: lo relee cada vez desde el principio</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">💬</span><b>3 · Contesta</b>Y su respuesta se suma al contexto para la vez siguiente</div>
</div>
<div class="aviso">🐢 Por eso una conversación muy larga va más lenta, gasta antes el límite gratis y atiende peor a lo que quedó en medio.</div>

---

# Una conversación para cada cosa

<div class="dos" style="align-items:stretch">
<div class="tarjeta velo"><span class="ico">🍝</span><b>Una para todo</b>La receta, la hipoteca y el viaje en la misma conversación: una cosa se cuela en la otra, y un error del principio se arrastra hasta el final.</div>
<div class="tarjeta sol"><span class="ico">🗂️</span><b>Una para cada cosa</b>«Viaje a Asturias», «Papeles del banco», «Recetas», «Inglés»… Cada una con su tema, y volvéis a ella cuando sigáis con él.</div>
</div>
<div class="aviso">🧠 Algunas apps guardan además una «memoria» con datos vuestros entre conversaciones. Se puede ver y borrar en los ajustes.</div>

---

# Ve, oye y lee: todo son fragmentos

![w:1110](img/s2-multimodal.svg)

---

# Así ve una foto: en parches de píxeles

<div class="dos" style="align-items:center">
<div class="trozos"><img src="img/fotos/difusion-4.jpg"></div>
<div class="pasos-mini" style="font-size:24px">
<div class="tarjeta"><b>✂️ 1 · La divide en parches</b>De 14 × 14 o 16 × 16 píxeles: miles por foto</div>
<div class="tarjeta sol" style="margin-top:10px"><b>🔢 2 · Cada parche, números</b>Cientos, como con cada palabra</div>
<div class="tarjeta tinta" style="margin-top:10px"><b>🔗 3 · Los relaciona</b>Entre sí y con vuestra pregunta</div>
</div>
</div>
<div class="credito">Foto: Jebulon · CC0 · Wikimedia Commons · Cuadrícula ampliada para que se vea</div>

---

<!-- _class: pregunta -->

# Probad: hacedle una foto a algo de clase

Y preguntad: «¿Qué es esto? Explícamelo». ¿Ha acertado?

---

# Así oye y habla

<div class="cadena">
<div class="tarjeta"><span class="ico">🎙️</span><b>1 · Mide la onda</b>16.000 veces por segundo, y la corta en fragmentos de centésimas de segundo</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🔢</span><b>2 · A números</b>Cada fragmento, una lista de números, como una palabra. Así prepara la respuesta</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">🔊</span><b>3 · A voz</b>Un decodificador vuelve a convertir la respuesta en onda: una voz sintética</div>
</div>
<div class="aviso">⏱️ Contesta en unas tres décimas de segundo, como una persona.</div>

---

# ¿Para qué os sirve que vea y oiga?

<div class="rejilla-3 compacta">
<div class="tarjeta"><span class="ico">🌿</span><b>¿Qué planta es?</b>Una foto y os dice cuál es y cómo cuidarla</div>
<div class="tarjeta sol"><span class="ico">🍽️</span><b>Menús y carteles</b>Os los traduce apuntando con la cámara</div>
<div class="tarjeta tinta"><span class="ico">📄</span><b>Papeles</b>Una foto a una carta y os la explica, como haremos luego</div>
<div class="tarjeta alerta"><span class="ico">🪑</span><b>Instrucciones</b>«¿Qué pieza va aquí?» con una foto del mueble a medio montar</div>
<div class="tarjeta"><span class="ico">👓</span><b>Para quien ve poco</b>Describe fotos y lee en voz alta</div>
<div class="tarjeta sol"><span class="ico">🌍</span><b>Conversar</b>Habla con vosotros en inglés para practicar</div>
</div>
<div class="aviso">⚠️ Setas y medicinas, nunca solo con la IA: puede equivocarse. Preguntad al experto o al farmacéutico.</div>

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

# Por dentro: tres piezas

<div class="cadena">
<div class="tarjeta"><span class="ico">🔤</span><b>1 · El lector</b>Convierte vuestra frase en números que resumen lo que pedís</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🧹</span><b>2 · El limpiador</b>En cada paso predice qué es ruido y lo quita, guiado por esos números: de 20 a 50 pasos</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">🔍</span><b>3 · El ampliador</b>Todo pasa en una versión pequeña y comprimida. Al final, la amplía a tamaño real</div>
</div>
<div class="aviso">⏳ Por eso tarda unos segundos: son decenas de pasadas por un modelo enorme.</div>

---

# Trabaja en pequeño y luego amplía

<div class="dos" style="align-items:center">
<figure class="foto"><img src="img/fotos/alcazaba-pequena.png" style="height:290px"><figcaption>Lo que limpia: un resumen de 64 × 48</figcaption></figure>
<figure class="foto"><img src="img/fotos/difusion-4.jpg" style="height:290px"><figcaption><span class="ok">Lo que veis, a tamaño real</span></figcaption></figure>
</div>
<div class="aviso">💡 Limpiar en pequeño es mucho más rápido: luego solo hay que ampliar.</div>
<div class="credito">Foto: Jebulon · CC0 · Wikimedia Commons · Reducción hecha para ilustrar</div>

---

<!-- _class: pregunta -->

# Pidámosle una imagen en directo

«Un gato tomando café en la Alcazaba, en acuarela». ¿Qué le pedimos después?

---

# ¿Cómo sabe qué dibujar?

<div class="cadena">
<div class="tarjeta"><span class="ico">🖼️</span><b>Aprendió con descripciones</b>Millones de fotos, cada una con su frase: «un gato negro en una ventana»</div>
<div class="flecha">➜</div>
<div class="tarjeta sol"><span class="ico">🧭</span><b>Vuestra frase hace de brújula</b>En cada paso de limpieza le dice hacia dónde ir</div>
<div class="flecha">➜</div>
<div class="tarjeta tinta"><span class="ico">🎨</span><b>Cuanto más detalle, mejor</b>Estilo, colores, luz, de cerca o de lejos</div>
</div>
<div class="aviso">🎲 Si se lo pedís dos veces, sale distinto: cada vez parte de un ruido diferente.</div>

---

# Ejemplo · una felicitación de Navidad

<div class="dos" style="align-items:stretch">
<div class="tarjeta velo"><b>😕 Pobre</b>«Un dibujo de Navidad»</div>
<div class="tarjeta sol receta"><b>😃 Rica</b>«<span class="pieza p1">Una felicitación de Navidad:</span> <span class="pieza p2">la Alcazaba de Almería nevada al atardecer, con luces cálidas en las ventanas,</span> <span class="pieza p3">en acuarela y con colores suaves.</span> <span class="pieza p4">Plano general, formato horizontal y sin texto.</span>»</div>
</div>
<div class="leyenda"><span class="p1">Qué</span><span class="p2">Escena</span><span class="p3">Estilo</span><span class="p4">Encuadre</span></div>

---

# Lo que todavía le cuesta

<div class="rejilla-4">
<div class="tarjeta"><span class="ico">⛪</span><b>Lo poco conocido</b>Pedid la iglesia de vuestro pueblo: os dibuja una iglesia, no la vuestra.</div>
<div class="tarjeta sol"><span class="ico">🔢</span><b>Contar</b>Pedid siete globos: a veces salen seis u ocho.</div>
<div class="tarjeta tinta"><span class="ico">👥</span><b>Repetir a alguien</b>La misma cara en varias imágenes sale parecida, pero no igual.</div>
<div class="tarjeta alerta"><span class="ico">✋</span><b>Los detalles</b>Manos, letras pequeñas, relojes: cada vez menos, pero aún pasa.</div>
</div>
<div class="aviso">🎨 Si sale mal, no empecéis de cero: decidle qué cambiar.</div>

---

# También retoca fotos y hace vídeos

<div class="rejilla-4">
<div class="tarjeta"><span class="ico">🧹</span><b>Quitar</b>Un cable, un cartel o a alguien del fondo</div>
<div class="tarjeta sol"><span class="ico">🎨</span><b>Colorear</b>Fotos en blanco y negro</div>
<div class="tarjeta tinta"><span class="ico">🔍</span><b>Ampliar</b>Una foto pequeña o borrosa</div>
<div class="tarjeta alerta"><span class="ico">🎬</span><b>Vídeo</b>Unos segundos de vídeo, con sonido, a partir de una frase</div>
</div>
<div class="aviso">📌 Una foto retocada así ya no es un documento: si la compartís, decid que está retocada.</div>

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

<!-- _class: pregunta -->

# ¿Qué pregunta saldrá mejor?

**A:** «Qué ver en Granada» · **B:** «Actúa como un guía paciente. Recomiéndame qué ver en Granada en un día con mi marido, que usa bastón. Dámelo en una lista con horarios»

---

# La fórmula: cuatro piezas

<div class="rejilla-4">
<div class="tarjeta"><b>1 · Quién</b>El papel que le dais: «Actúa como un cocinero con experiencia…»</div>
<div class="tarjeta sol"><b>2 · Qué</b>Lo que queréis: «…organízame la comida del domingo…»</div>
<div class="tarjeta tinta"><b>3 · Contexto</b>Para quién y con qué límites: «…seremos 12, dos son vegetarianos y no quiero gastar más de 80&nbsp;€…»</div>
<div class="tarjeta alerta"><b>4 · Formato</b>Cómo lo queréis: «…el menú y la lista de la compra»</div>
</div>
<div class="aviso">🎯 Cuanto más contexto, más pistas para acertar. Y si no os gusta, pedidle que lo cambie.</div>

---

# Ejemplo · la comida del domingo

<div class="dos" style="align-items:stretch">
<div class="tarjeta velo"><b>😕 Pobre</b>«Menú para el domingo»</div>
<div class="tarjeta sol receta"><b>😃 Rica</b>«<span class="pieza p1">Actúa como un cocinero con experiencia.</span> <span class="pieza p2">Organízame la comida familiar del domingo:</span> <span class="pieza p3">seremos 12, dos son vegetarianos, a los niños no les gusta el pescado y no quiero gastar más de 80&nbsp;€.</span> <span class="pieza p4">Dame el menú y la lista de la compra por secciones del súper.</span>»</div>
</div>
<div class="leyenda"><span class="p1">Quién</span><span class="p2">Qué</span><span class="p3">Contexto</span><span class="p4">Formato</span></div>

---

# Ejemplo · una reclamación

<div class="dos" style="align-items:stretch">
<div class="tarjeta velo"><b>😕 Pobre</b>«Reclamación a la compañía de la luz»</div>
<div class="tarjeta sol receta"><b>😃 Rica</b>«<span class="pieza p1">Eres un experto en consumo.</span> <span class="pieza p2">Escríbeme una reclamación</span> <span class="pieza p3">a mi compañía de la luz: este mes me cobran 393&nbsp;€ cuando suelo pagar 50, y la lectura era “estimada”.</span> <span class="pieza p4">Que sea educada, corta y con los datos que tengo que rellenar entre corchetes.</span>»</div>
</div>
<div class="leyenda"><span class="p1">Quién</span><span class="p2">Qué</span><span class="p3">Contexto</span><span class="p4">Formato</span></div>

---

# Ejemplo · aprender algo nuevo

<div class="dos" style="align-items:stretch">
<div class="tarjeta velo"><b>😕 Pobre</b>«Cómo funciona WhatsApp»</div>
<div class="tarjeta sol receta"><b>😃 Rica</b>«<span class="pieza p1">Actúa como un profesor paciente.</span> <span class="pieza p2">Enséñame a mandar una foto por WhatsApp</span> <span class="pieza p3">a mi nieta. Tengo un móvil Samsung y es la primera vez que lo hago.</span> <span class="pieza p4">Paso a paso, numerado, con frases cortas.</span>»</div>
</div>
<div class="leyenda"><span class="p1">Quién</span><span class="p2">Qué</span><span class="p3">Contexto</span><span class="p4">Formato</span></div>

---

# 🎬 Demostración en directo

<div class="dos" style="align-items:start">
<div style="font-size:28px">
<ol><li>«Tengo huevos y patatas: ¿qué ceno?»</li><li>«Explícame el IBI con un ejemplo»</li><li>«Un poema para unas bodas de oro»</li><li>«¿Cómo se dice farmacia en inglés?»</li><li><strong>La vuestra</strong>: la más votada</li></ol>
</div>
<div class="tarjeta alerta"><span class="ico">👀</span><b>Para terminar</b>Le preguntaremos por la historia de un pueblo pequeño de Almería… y veremos si se inventa cosas.</div>
</div>

---

# Ejercicio: cinco cartas difíciles

<div class="miniaturas">
<figure><img src="img/fotos/carta-1.png"><figcaption>La hipoteca</figcaption></figure>
<figure><img src="img/fotos/carta-2.png"><figcaption>En chino</figcaption></figure>
<figure><img src="img/fotos/carta-3.png"><figcaption>Reintegros</figcaption></figure>
<figure><img src="img/fotos/carta-4.png"><figcaption>La receta</figcaption></figure>
<figure><img src="img/fotos/carta-5.png"><figcaption>La luz</figcaption></figure>
</div>
<div class="aviso">📸 Una carta para cada uno: foto, que la IA os la explique, y buscad lo que pide el reverso. Luego, cambiadla.</div>

---

# Las cartas: ¿qué ha pillado la IA?

<div class="rejilla-3 compacta">
<div class="tarjeta"><span class="ico">🏦</span><b>La hipoteca</b>¿Ha visto por qué sube la cuota si el Euríbor baja?</div>
<div class="tarjeta sol"><span class="ico">🀄</span><b>En chino</b>¿Ha leído bien qué lotes están afectados?</div>
<div class="tarjeta alerta"><span class="ico">🏛️</span><b>Reintegros</b>¿Os ha avisado de que era una estafa?</div>
<div class="tarjeta tinta"><span class="ico">📜</span><b>La receta</b>¿Sabía que «alegría» es el ajonjolí?</div>
<div class="tarjeta"><span class="ico">💡</span><b>La luz</b>¿Ha visto que la lectura era «estimada»?</div>
<div class="tarjeta velo"><span class="ico">🤔</span><b>¿Y vosotros?</b>¿Qué se le ha escapado?</div>
</div>
<div class="aviso">👀 La IA ayuda a leer, pero lo importante lo tiene que mirar una persona.</div>

---

<!-- _class: resumen -->

# Resumen de hoy

1. Hay **muchas IA**, con normas distintas: mirad **quién está detrás**
2. Modelos **grandes y pequeños**, y pueden **pensar** antes de contestar
3. Con la **cuenta de la UAL** tenéis gratis uno de los mejores del mundo
4. **Una conversación para cada cosa**: el contexto importa
5. Preguntar bien: **quién, qué, contexto y formato**

---

<!-- _class: cierre -->
<!-- _header: '' -->
<!-- _footer: '' -->

Tema 2 · Inteligencia artificial

# ¡Gracias!

## En la parte 3: los riesgos, y cómo defendernos

**Para casa:** entrad en Gemini con vuestra cuenta de la UAL y pedidle ayuda con un papel de casa.
