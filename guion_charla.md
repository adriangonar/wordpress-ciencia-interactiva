# Guión — WordPress como laboratorio científico
**WordPress Valladolid · 20/05/2026 · Adrián González Naranjo · ~35–40 min**

---

## ANTES DE EMPEZAR

- Presentación en navegador, pantalla completa (F11)
- Navega con ← → o teclas de flecha
- Animaciones y simulaciones se lanzan solas al llegar a cada slide
- Demo (slide 9): empieza en 🌍 Tierra, ve pulsando los escenarios en orden

---

## S1 — PORTADA (1 min)

"Buenas tardes. Lo que veis en pantalla no es una imagen ni un vídeo de YouTube. Es una simulación de física espacial real corriendo ahora mismo en vuestro navegador.

Y está publicada en WordPress. Con el bloque HTML que ya tenéis. Sin plugins de pago.

Eso es lo que os cuento hoy."

---

## S2 — DE QUÉ VA ESTO (3 min)

"¿Cuántos habéis publicado contenido científico o técnico en WordPress?"

> *Esperar respuestas.*

"El patrón habitual es este: texto, imagen estática, quizás un vídeo de YouTube incrustado. Si hay una fórmula, hay una captura de pantalla de la fórmula. El lector lo hojea y se va.

Ahora pensad en lo contrario: el lector llega a vuestro artículo y puede interactuar con la ciencia directamente. Cambiar parámetros. Ver cómo cambia el resultado. Entender algo que con texto puro nunca entendería.

Eso existe. Funciona en WordPress. Y no necesita ningún plugin de pago.

WordPress tiene un bloque HTML que ejecuta JavaScript directamente en el navegador del lector. Y JavaScript puede hacer todo eso.

Os lo voy a demostrar con un ejemplo real."

---

## S3 — QUIÉN SOY (2 min)

"Contexto rápido.

Soy matemático. Trabajo con informática. Pasé meses calculando trayectorias de satélites con Python, generando simulaciones que solo yo podía ver en mi ordenador.

El salto a WordPress fue absurdamente simple: reescribí ese código en JavaScript, abrí el editor de bloques, inserté un bloque HTML, pegué el canvas y el script, y guardé. Funcionó a la primera. La simulación apareció en la previsualización.

Ese momento es lo que os traigo hoy."

---

## S4 — EL CONTENIDO: EL PROBLEMA (3 min)

> *La animación del canvas se lanza sola. Señalad la pantalla.*

"El ejemplo que vamos a publicar en WordPress: el Problema de los Tres Cuerpos.

Tres objetos en el espacio que se atraen por gravedad. Tierra, Luna, satélite. ¿Puedes predecir exactamente dónde estará el satélite dentro de un año?

Con dos cuerpos, sí. Kepler lo resolvió en 1609.

Con tres cuerpos, en general no. El sistema es caótico: una diferencia mínima en las condiciones iniciales produce trayectorias completamente distintas.

Lo que veis en pantalla es esa simulación corriendo en el navegador. Cada vez que un lector abre nuestro artículo de WordPress, el navegador la recalcula en tiempo real."

---

## S5 — LA FÍSICA, LO JUSTO (3 min)

"Para publicar esto en WordPress no necesitáis entender la física. Pero hay tres datos que ayudan a entender el código.

Uno: simplificamos. La Tierra y la Luna giran en círculos fijos. Solo estudiamos el satélite. Esto nos da una ecuación con solución numérica.

Dos: todo el sistema depende de un único número — mu, la fracción de masa de la Luna. Para Tierra-Luna vale 0.012. Una línea de código. Cambiar ese número cambia todo el sistema planetario.

Tres: existen cinco puntos especiales donde las fuerzas se cancelan exactamente. Los Puntos de Lagrange. El James Webb orbita en uno de ellos desde 2022.

Tres datos. Suficiente para entender lo que viene y para escribir un artículo de divulgación que enganche."

---

## S6 — LOS PUNTOS DE LAGRANGE (3 min)

"Los cinco Puntos de Lagrange.

L1, L2 y L3 están en la línea Tierra-Luna. Son inestables — cualquier pequeño empujón expulsa al satélite. Pero son muy útiles porque se alcanzan con muy poco combustible.

L4 y L5 forman triángulos equiláteros con la Tierra y la Luna. Son estables. Hay más de siete mil asteroides que llevan miles de millones de años atrapados en L4 y L5 del sistema Júpiter-Sol sin que nadie los haya puesto ahí.

El James Webb orbita en L2 del sistema Sol-Tierra, a 1.5 millones de kilómetros de aquí. Siempre en la sombra de la Tierra, a –233 grados. Funciona gracias a estas matemáticas.

Y este dato — el James Webb — es el hook de vuestro artículo WordPress. No la fórmula: el contexto real. Eso es lo que hace que el lector siga leyendo."

---

## S7 — LA VISUALIZACIÓN PRINCIPAL (4 min)

> *La imagen de Hill se genera en el canvas al llegar aquí.*

"Esta imagen la genera JavaScript en vuestro navegador en menos de un segundo. Píxel a píxel. Sin servidor.

Lo que veis son las Regiones de Hill: las zonas del espacio a las que puede ir el satélite según la energía que tiene. Las zonas oscuras están prohibidas. Las claras son accesibles. Los puntos de colores son los cinco Lagrange.

Cuando la energía sube hasta el nivel de L1, se abre un cuello entre la Tierra y la Luna. Cuando llega a L2, puede escapar.

En un artículo de WordPress, esta visualización hace algo que ningún texto puede hacer: el lector entiende de un vistazo por qué el satélite no puede ir a cualquier sitio. Y es generada en tiempo real, no es una imagen estática.

Esto es lo que separa un artículo de divulgación memorable de uno que se olvida."

---

## S8 — EL CÓDIGO EN WORDPRESS (4 min)

"Aquí está el núcleo. Esta función calcula dónde va el satélite en cada instante. Son treinta líneas de JavaScript."

> *Señalad el bloque de código.*

"No necesitáis entender la física para usar esto. Necesitáis entender el flujo de WordPress:

Uno: nuevo artículo o página.
Dos: añadir bloque HTML personalizado — Ctrl+Alt+H o buscáis 'HTML' en el selector.
Tres: dentro del bloque, un canvas y este script.
Cuatro: guardar. La simulación aparece en la previsualización del editor exactamente como la verá el lector.

WordPress no toca el contenido del bloque HTML. El navegador del lector ejecuta el JavaScript directamente. Sin intermediarios, sin APIs externas, sin plugins.

El artículo funciona igual en cualquier hosting de WordPress. No depende de nada externo."

---

## S9 — DEMO EN VIVO (5 min)

> *La simulación se lanza al llegar aquí. Pulsar los escenarios en orden, dejando correr cada uno unos segundos.*

"Esto es lo que ve el lector cuando abre el artículo. Cuatro escenarios, cada uno con un mensaje distinto."

**🌍 Tierra** — pulsar, esperar 5 segundos:
"Órbita circular alrededor de la Tierra. Las zonas oscuras son regiones prohibidas: con esta energía, el satélite no puede llegar a la Luna. El lector lo ve de inmediato. Ningún texto explica esto tan rápido."

**🚀 Artemis** — pulsar:
"La energía sube justo lo necesario para abrir el cuello de L1. El satélite cruza entre Tierra y Luna, pero no puede escapar al espacio. Esta es la ventana de energía de las misiones Artemis reales. El lector está viendo física de la NASA."

**🔭 Webb** — pulsar:
"Órbita en la zona del punto L2. El James Webb vive exactamente aquí desde 2022. El lector que llega a este punto del artículo ya entiende por qué ese punto fue elegido."

**🌀 Caos** — pulsar:
"La diferencia respecto a Artemis es de 0.010 en la posición inicial. La energía es casi idéntica. Pero la trayectoria es completamente distinta. Eso es el caos determinista. Este es el momento que hace que el lector comparta el artículo."

> *Pausar aquí. Si hay preguntas, este es el momento ideal.*

---

## S10 — POR QUÉ FUNCIONA COMO CONTENIDO (3 min)

"¿Por qué este tipo de contenido funciona en WordPress?

Tres razones.

Primera: el gancho es universal. El James Webb, las misiones Artemis, los asteroides Troyanos. Son temas que cualquier lector ha oído. La simulación los conecta con la física real que hay detrás.

Segunda: el lector hace algo. No solo lee. Pulsa un botón y ve cómo cambia la trayectoria. Eso genera un recuerdo que el texto no genera.

Tercera: es compartible. El lector que ve el efecto del caos con sus propios ojos quiere enseñárselo a alguien. Eso es lo que hace que un artículo de WordPress tenga vida propia."

---

## S11 — CÓMO MONTARLO HOY (4 min)

"Paso a paso, desde cero.

**El bloque HTML:** nuevo artículo, Ctrl+Alt+H, canvas más script dentro. Guardar. Listo. La simulación corre en la previsualización.

**Las fórmulas:** MathJax o KaTeX. Los dos tienen plugins gratuitos para WordPress. Renderizan notación LaTeX directamente en el frontend. Vuestros lectores verán las ecuaciones bien formateadas sin ningún esfuerzo extra.

**Interactividad:** un input range HTML dentro del mismo bloque. Diez líneas de JavaScript adicionales. El lector mueve un slider y la simulación cambia en tiempo real.

**Datos externos:** la API de la NASA es pública y gratuita. Podéis traer datos reales de posición de satélites directamente a vuestro artículo. La API REST de WordPress os permite guardar configuraciones por usuario.

Todo esto funciona en cualquier instalación de WordPress. Sin plugins de pago. Sin cambios en el servidor."

> *Si hay tiempo: abrir el inspector del navegador y mostrar el bloque HTML de esta presentación.*

---

## S12 — MÁS ALLÁ DE LA FÍSICA (2 min)

"Lo que hemos visto no es solo para matemáticos o físicos.

El mismo patrón funciona para cualquier disciplina que tenga datos o modelos que visualizar.

Biología: modelos de propagación de epidemias, crecimiento de poblaciones, redes neuronales.
Economía: simulaciones de mercado, distribuciones estadísticas, modelos de riesgo.
Geografía: datos climáticos de la NASA, mapas interactivos con Leaflet, visualización de terremotos en tiempo real.
Música: visualización de ondas sonoras, síntesis de audio con la Web Audio API.

El patrón es siempre el mismo: modelo o datos, JavaScript, canvas o SVG, bloque HTML de WordPress. El resultado: contenido que el lector recuerda."

---

## S13 — CIERRE (2 min)

"WordPress tiene el 43% del mercado web mundial. Es la plataforma de publicación más usada. Y tiene un bloque HTML que ejecuta cualquier simulación científica que se os ocurra.

La diferencia entre un artículo que se olvida y uno que se comparte a veces es un canvas y treinta líneas de JavaScript.

Tenemos las herramientas. El bloque HTML ya está en vuestro WordPress. Lo que os lleváis hoy es saber que existe y lo que puede hacer.

Gracias. El código de esta presentación está disponible."

---

## PREGUNTAS QUE PUEDEN HACER — Y CÓMO RESPONDERLAS

**"¿Hay riesgos de seguridad al poner código JavaScript en el bloque HTML?"**
El JavaScript del bloque HTML corre en el navegador del lector, no en vuestro servidor. No tiene acceso a la base de datos de WordPress ni al backend. El riesgo es exactamente el mismo que el de cualquier tema o plugin que ya tenéis instalado. WordPress ya ejecuta JavaScript en el frontend constantemente.

**"¿Funciona en móvil?"**
Sí. Canvas y requestAnimationFrame son estándar en todos los navegadores móviles modernos. La simulación de esta presentación funciona en móvil. Puede ser algo más lenta en dispositivos de gama baja, pero es completamente funcional.

**"¿Qué pasa si el lector tiene JavaScript desactivado?"**
El mismo problema que con cualquier tema moderno de WordPress: nada funciona. En la práctica, menos del 0.2% de usuarios desactiva JavaScript. No es un problema real para este tipo de contenido.

**"¿Necesito saber programar para hacer esto?"**
Para reproducir exactamente lo que hemos visto hoy, sí necesitáis poder leer y modificar JavaScript básico. Para publicar una simulación copiada y adaptada, no. El código es open source y comentado — se puede usar sin entender la física subyacente.

**"¿Cómo hago que el lector pueda guardar sus configuraciones?"**
Dos opciones: localStorage del navegador para guardar en el dispositivo del lector sin tocar WordPress, o la API REST de WordPress con un plugin de usuarios para guardar en base de datos. La primera opción tarda diez líneas de JavaScript. La segunda requiere algo más de trabajo pero permite que el usuario acceda a sus datos desde cualquier dispositivo.

**"¿Esto afecta al rendimiento de la página?"**
El script se ejecuta en un Web Worker o en el hilo principal del navegador según lo implementéis. La simulación de esta charla usa requestAnimationFrame y no bloquea el hilo principal. El impacto en el tiempo de carga inicial es mínimo — el script es pequeño y no tiene dependencias externas.

**"¿Se puede hacer esto con Gutenberg o solo con el editor clásico?"**
Con Gutenberg es exactamente como lo hemos visto: bloque HTML personalizado. Con el editor clásico también funciona, en modo HTML. Incluso podéis crear un bloque Gutenberg personalizado que encapsule la simulación si queréis reutilizarla en varios artículos.

**"¿Y con WooCommerce? ¿Tiene sentido esto en un e-commerce?"**
Depende del producto. Si vendéis formación científica o técnica, una simulación interactiva como demostración del contenido del curso es exactamente esto. Si vendéis telescopios, una simulación de trayectorias orbitales como contenido de blog puede diferenciaros completamente.

**"¿La NASA tiene APIs públicas para esto?"**
Sí. La NASA tiene varias APIs públicas y gratuitas: datos de posición de satélites (Horizons de JPL), imágenes del día (APOD), datos de asteroides cercanos (NeoWs), clima espacial. Todas documentadas en api.nasa.gov. Se pueden consumir desde JavaScript en el mismo bloque HTML.

---

## TABLA DE TIEMPOS

| Slide | Contenido | Tiempo |
|-------|-----------|--------|
| 1 | Portada | 1 min |
| 2 | De qué va esto | 3 min |
| 3 | Quién soy | 2 min |
| 4 | El problema | 3 min |
| 5 | La física, lo justo | 3 min |
| 6 | Puntos de Lagrange | 3 min |
| 7 | La visualización principal | 4 min |
| 8 | El código en WordPress | 4 min |
| 9 | Demo en vivo | 5 min |
| 10 | Por qué funciona como contenido | 3 min |
| 11 | Cómo montarlo hoy | 4 min |
| 12 | Más allá de la física | 2 min |
| 13 | Cierre | 2 min |
| **Total** | | **~39 min** |

**Para recortar a 30 min:** quita slide 3, reduce slide 6 a 1.5 min, demo a 3 min.

---

## SECUENCIA DE LA DEMO — guía rápida

| Botón | Lo que se ve | Lo que dices |
|-------|--------------|--------------|
| 🌍 Tierra | Órbita circular, zona prohibida visible | "El lector ve de inmediato por qué no puede llegar a la Luna" |
| 🚀 Artemis | Cruza L1, orbita entre Tierra y Luna | "La ventana de energía de las misiones Artemis reales" |
| 🔭 Webb | Órbita en zona L2 | "El James Webb vive exactamente aquí desde 2022" |
| 🌀 Caos | Trayectoria completamente distinta | "0.010 de diferencia — eso es el caos — esto es lo que se comparte" |

---

## S14 — TURNO DE PREGUNTAS — cómo arrancarlo

> *Al llegar aquí, leer en voz alta:*

"Antes de abrir el turno libre, hay algunas preguntas que suelen venir a la cabeza y que he preparado. Si alguna es la vuestra, me la podéis cortar cuando llegue.

¿Cómo funciona el bloque HTML exactamente? ¿Necesito PHP? ¿Por qué WordPress y no otra cosa? ¿Por qué este tema científico?

Arrancamos."

---

## PREGUNTAS COMPLETAS — respuestas preparadas

---

### SOBRE WORDPRESS Y EL BLOQUE HTML

**¿Cómo funciona exactamente el bloque HTML de WordPress?**
El bloque HTML personalizado del editor de bloques (Gutenberg) sirve el contenido tal cual al navegador del lector, sin procesarlo. WordPress lo trata como texto opaco. El navegador del lector recibe el HTML, el CSS y el JavaScript y los ejecuta directamente. Es exactamente igual que si pusierais ese código en cualquier página web estática.

**¿Necesito saber PHP para hacer esto?**
No. Todo lo que hemos visto hoy es HTML, CSS y JavaScript puro. PHP solo entra en juego si queréis crear un plugin de WordPress, modificar el tema a nivel de código, o guardar datos en la base de datos de WordPress. Para publicar simulaciones interactivas en una entrada o página, el bloque HTML es suficiente y no requiere PHP.

**¿Y si quiero hacer algo más avanzado con PHP?**
PHP os da acceso al backend de WordPress: podéis crear shortcodes, endpoints personalizados en la API REST, guardar datos por usuario, o encapsular la simulación en un bloque Gutenberg reutilizable. Pero eso es un paso siguiente — lo que hemos visto hoy funciona sin tocar PHP en ningún momento.

**¿Funciona con el editor clásico (TinyMCE)?**
Sí. En el editor clásico cambiáis a la pestaña "Texto" (HTML) y pegáis el código directamente. El resultado para el lector es idéntico.

**¿Se puede convertir en un bloque Gutenberg personalizado?**
Sí. Si queréis reutilizar la simulación en varios artículos sin copiar el código cada vez, podéis encapsularla en un bloque Gutenberg con `@wordpress/create-block`. Eso ya requiere JavaScript y algo de Node.js, pero la simulación en sí no cambia.

**¿Funciona en cualquier tema de WordPress?**
Sí. El bloque HTML es independiente del tema. La simulación funciona igual en Astra, GeneratePress, Divi, Twenty Twenty-Four o cualquier otro. El único requisito es que el tema no bloquee la ejecución de scripts en el contenido, lo cual no hace ningún tema estándar.

---

### SOBRE RENDIMIENTO Y COMPATIBILIDAD

**¿Afecta al rendimiento de la página?**
El script de la simulación es pequeño y sin dependencias externas — no carga ninguna librería de terceros. La animación usa `requestAnimationFrame`, que el navegador pausa automáticamente cuando la pestaña no está visible. El impacto en el tiempo de carga inicial es mínimo. Para páginas muy orientadas a SEO y velocidad, podéis cargar el script de forma diferida con `defer`.

**¿Funciona en móvil?**
Sí. `Canvas` y `requestAnimationFrame` son estándar en todos los navegadores móviles modernos — Chrome, Safari, Firefox. La simulación de esta presentación funciona en móvil ahora mismo. En dispositivos de gama muy baja puede ir algo más lento, pero es completamente funcional.

**¿Qué pasa si el lector tiene JavaScript desactivado?**
La simulación no funciona. El mismo problema que con cualquier tema moderno de WordPress — los menús desplegables, los sliders de imágenes, los formularios de contacto tampoco funcionarían. En la práctica, menos del 0.2% de usuarios tiene JavaScript desactivado. No es un problema real.

**¿Funciona con caché de WordPress (WP Rocket, W3 Total Cache)?**
Sí. Los plugins de caché sirven el HTML estático al lector, y el JavaScript se ejecuta en el navegador después. No hay conflicto. Si usáis minificación agresiva de JavaScript, aseguraos de excluir vuestro script de simulación.

---

### SOBRE SEGURIDAD

**¿Es seguro poner JavaScript en el bloque HTML?**
El JavaScript del bloque corre en el navegador del lector, en el contexto de vuestra página. No tiene acceso al servidor, a la base de datos de WordPress, ni a las credenciales de administrador. El riesgo es idéntico al de cualquier plugin o tema que ya tenéis instalado. Si el código es vuestro o de una fuente de confianza, no hay problema.

**¿Puede un lector malicioso explotar esto?**
El lector ya puede ejecutar JavaScript en su propio navegador — eso no depende de vosotros. El bloque HTML no abre ninguna vulnerabilidad nueva en el servidor. Lo único que ejecuta el JavaScript del bloque es el propio navegador del lector.

---

### SOBRE LA ELECCIÓN DE WORDPRESS

**¿Por qué WordPress y no una web estática o GitHub Pages?**
WordPress os da gestión de contenido, SEO, comentarios, usuarios, formularios y API REST sin construir nada desde cero. La simulación interactiva vive dentro de todo ese ecosistema ya construido. Con una web estática tendríais que construir todo eso vosotros mismos.

**¿Por qué no usar un plugin de visualización como WPDataTables o Visualizer?**
Los plugins de visualización están diseñados para tipos de gráficas predefinidos: barras, líneas, tartas, mapas. La simulación de física espacial que hemos visto no cabe en ninguna de esas categorías. El bloque HTML ejecuta cualquier código — no hay límite de lo que podéis visualizar.

**¿Por qué no usar Observable, CodePen o un iframe externo?**
Podríais incrustar un iframe de Observable o CodePen, sí. Pero dependéis de un servicio externo — si ese servicio cae o cambia sus condiciones, vuestro contenido desaparece. El bloque HTML es autónomo: funciona sin conexión a ningún servicio externo, para siempre, mientras WordPress funcione.

---

### SOBRE EL CONTENIDO CIENTÍFICO

**¿Por qué este tema y no otro más sencillo?**
El Problema de los Tres Cuerpos tiene tres ventajas concretas para una charla: es visualmente impactante desde el primer segundo, conecta con misiones reales que el lector ya conoce (James Webb, Artemis), y demuestra el caos de forma intuitiva e inmediata. Un gráfico de barras no genera ese impacto.

**¿Necesito saber matemáticas para replicar esto en mi WordPress?**
No. El código de la simulación es copiable y comentado. Lo que necesitáis es el contexto narrativo — saber qué demuestra cada escenario, cómo conectarlo con algo que el lector ya conoce. Eso es lo que os lleváis de esta charla.

**¿Qué otros temas científicos funcionarían igual de bien en WordPress?**
Cualquier tema con datos o modelos que se puedan visualizar. Biología: propagación de epidemias, crecimiento de poblaciones. Economía: simulaciones de mercado, distribuciones estadísticas. Geografía: datos climáticos de la NASA, mapas de terremotos. Física: circuitos eléctricos, óptica, ondas sonoras. El patrón es siempre el mismo.

**¿Las APIs de la NASA son gratuitas?**
Sí. `api.nasa.gov` tiene APIs públicas y gratuitas sin límite de uso razonable: imagen astronómica del día (APOD), posición de satélites (JPL Horizons), asteroides cercanos a la Tierra (NeoWs), clima espacial. Se consumen directamente desde JavaScript en el bloque HTML, sin backend.

**¿Qué es la constante de Jacobi que aparece en la demo?**
Es una cantidad que se conserva siempre en este sistema — como la energía total. Su valor determina qué zonas del espacio puede visitar el satélite. Si C es grande, el satélite está atrapado cerca de la Tierra. Si baja hasta el nivel de L1, puede pasar hacia la Luna. Si baja más, puede escapar al espacio. Es lo que veíais cambiar en la demo al cambiar de escenario.

**¿Por qué el satélite se queda dentro del sistema en el escenario Artemis?**
Porque su energía (constante de Jacobi) está entre el nivel de L1 y el de L2. El cuello de L1 está abierto — puede cruzar entre Tierra y Luna. Pero el cuello de L2 está cerrado — no puede escapar al espacio exterior. Es una "jaula" de energía. Las misiones Artemis aprovechan exactamente esta ventana.

