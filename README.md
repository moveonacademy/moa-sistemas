# Sistemas MOA

Página de accesos de MOA Education: un botón por cada sistema.

| Sistema | Enlace |
|---|---|
| Moa Map | https://moamap-mk3y.vercel.app/ |
| Moa Finance | https://moa-education-finance.vercel.app/ |
| Moa Dashboard | https://moa-dashboard-three.vercel.app/ |
| Moa Student Platform | https://moa-education-students.fly.dev/ |

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
