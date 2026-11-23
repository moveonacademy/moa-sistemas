# Sistemas MOA

Página de accesos de MOA Education: un botón por cada sistema.

| Sistema | Enlace | Qué es |
|---|---|---|
| Moa Map | https://map.moaeducation.com/ | App de los KAM: carpeta operativa de cada colegio, supervisiones, incidencias, notas, Pruebas MOA y KPI. |
| Moa Finance | https://finance.moaeducation.com/ | Panel financiero: ingresos y gastos, CxC y CxP, plan vs. real mensual. |
| Moa Dashboard | https://dashboard.moaeducation.com/ | Tareas, checkpoints, revisión de calidad y KPI del equipo académico. |
| Moa Student Platform | https://moa-education-students.fly.dev/ | Clases de inglés: calendario, tareas, práctica con IA, pagos y certificados. |
| Moa Stand (D-Future) | https://stand.moaeducation.com/ | Stand «Aula viva»: registro por QR, prueba de inglés en el tótem, TV en vivo. |
| Soporte | https://soporte.moaeducation.com/ | Mesa de ayuda con tickets y aviso por correo. |

Es una página estática (solo `index.html` y la carpeta `assets/`): no necesita instalar nada ni "build".

## Agregar o cambiar un sistema

1. Abre `index.html`.
2. Busca el comentario que dice **PARA AGREGAR UN SISTEMA NUEVO**.
3. Copia un bloque completo `<li> ... </li>`, pégalo debajo del último y cambia:
   - el enlace (`href="..."`),
   - el nombre (`<h2><em>Moa</em> Nombre</h2>`),
   - la descripción (`<p>...</p>`).
4. Guarda y sube el cambio a GitHub: Vercel lo publica solo en 1–2 minutos.

## Despliegue en Vercel

- Framework Preset: **Other**
- Build Command: vacío
- Output Directory: vacío (la raíz del repositorio)

## Sonido (ElevenLabs)

Los audios están en `assets/audio/` y se generaron una sola vez con ElevenLabs, así que la página no usa ninguna clave ni gasta créditos al abrirse.

- **Saludos:** al tocar la burbuja «hola / buongiorno / hello…» se escucha el saludo que se ve, con voz nativa (`saludo-*.mp3`).
- **Escuchar qué es:** el botón con parlante de cada tarjeta lee una breve explicación del sistema (`desc-*.mp3`, voz con acento maracucho «Ask Mono»).
- **Interruptor de sonido** (abajo a la derecha): viene apagado. Encendido, suena una bienvenida según la hora, una vez al día (`bienvenida-*.mp3`). Las tarjetas no hacen ruido al pasar el mouse ni al abrirlas. La elección se recuerda en cada navegador.

Los audios en español van en maracucho bien cerrado (voseo, «primo», «qué molleja»…), a propósito. Si cambias la descripción de un sistema, conviene regenerar su `desc-*.mp3` con el mismo nombre de archivo.
