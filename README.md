# Aula IA · Química — demostración docente

Prototipo **sin API de IA** preparado específicamente para el PDF `Simulacro_Formulacion_Reactividad_2Bach(2).pdf`.

## Cómo abrirlo

Opción recomendada: abre una terminal en esta carpeta y ejecuta:

```bash
python -m http.server 8000
```

Visita `http://localhost:8000` en Chrome, Edge o Firefox. Para detener el servidor pulsa `Ctrl+C`.

La mayoría de funciones también funcionan abriendo `index.html` directamente. Usar un servidor local mejora la compatibilidad con la visualización del PDF.

## Funciones

- Los 12 ejercicios y todos sus apartados, transcritos de la ficha original.
- Soluciones explicadas paso a paso, ocultas por defecto.
- Visualizaciones SVG didácticas específicas según el tipo de ejercicio, con botones interactivos.
- Pizarra por apartado con lápiz, borrador, colores, deshacer, limpiar y exportar a PNG.
- Vista del PDF original integrado.
- Índice con distinción de los ejercicios prioritarios ★.
- Modo presentación para compartir en Google Meet.
- Progreso de ejercicios guardado en el almacenamiento local del navegador.

## Recomendación para Google Meet

Abre la web y comparte **solo la ventana del navegador**. Usa «Modo presentación» para ocultar el menú lateral. Las soluciones permanecen ocultas hasta que pulses «Mostrar respuesta»; recuerda ocultarlas antes de volver a compartir un apartado si no quieres revelarlas.

## Limitaciones de esta demo

- No hay IA real ni generación automática de contenido: los ejercicios, respuestas y visualizaciones se prepararon manualmente para esta ficha.
- Las representaciones son esquemas didácticos 2D; no son modelos moleculares 3D ni simulaciones físicas exactas.
- La pizarra se conserva al navegar entre ejercicios durante la sesión, pero no se guarda permanentemente: exporta a PNG si quieres conservarla.
- Las respuestas químicas se han elaborado para el nivel de 2.º de Bachillerato y deben revisarse antes de su uso evaluativo.
- La visualización del PDF puede depender del navegador; si falla, abre `assets/ficha_original.pdf`.
- Las fuentes web opcionales pueden no cargarse sin conexión; hay fuentes locales de reserva.

## Estructura

- `index.html` — interfaz.
- `styles.css` — diseño adaptable y modo presentación.
- `data.js` — ejercicios, explicaciones, respuestas y parámetros visuales.
- `script.js` — navegación, pizarra y motor SVG.
- `assets/ficha_original.pdf` — documento facilitado por el profesor.

## Novedades de la versión 2.0

- Diseño adaptable a ordenador, Android y tablet con botones táctiles y tipografía ampliada.
- Pizarra química avanzada por apartado: lápiz, goma, grosor de trazo, colores, texto editable con teclado, símbolos (flechas, fórmulas, cargas, grupos funcionales), deshacer, rehacer y PNG.
- Para mover un cuadro de texto en ordenador, activa «Mover» y arrástralo manteniendo **Alt**. En tablet, toca el texto para editarlo; el reposicionamiento táctil fino queda pendiente.
- «Mostrar respuesta» abre la resolución en modo progresivo: paso anterior, siguiente paso, mostrar todo y ocultar todo.
- Animaciones y modelos atómicos **conceptuales** en algunas visualizaciones de enlaces y reacciones. Los símbolos X de los esquemas genéricos no representan un elemento químico concreto.
- Las anotaciones se conservan en memoria mientras la pestaña siga abierta, pero no se sincronizan entre dispositivos ni se guardan permanentemente.
- La web se puede alojar en un hosting estático HTTPS para abrirla desde Android sin copiar los archivos. **El ZIP no publica la web automáticamente**.

### Nota sobre las visualizaciones

Los modelos animados son esquemas didácticos simplificados; no sustituyen estructuras químicas validadas, ni representan mecanismos reales de reacción. Esta versión no contiene simulaciones moleculares 3D. Para una futura versión se pueden incorporar modelos estructurales reales y motores de visualización 3D.

## Versión 2.2: edición de pizarra y tabla periódica
- Los objetos de texto y símbolos muestran sus bordes y controles únicamente cuando están seleccionados. Toca fuera para ocultarlos.
- Selector «Letra» para cambiar el tamaño del objeto seleccionado. No es un editor de texto enriquecido: el tamaño se aplica a todo el cuadro, no a palabras individuales.
- Símbolos químicos independientes, con arrastre y control de tamaño. Números 0–9 añadidos a la paleta.
- Tabla periódica de 118 elementos con búsqueda, filtros por familia y ficha de propiedades; valores de electronegatividad disponibles según el conjunto local incluido. No sustituye a una base de datos científica exhaustiva.
- Se recomienda probar los gestos de redimensionamiento en Chrome Android antes de la clase.
