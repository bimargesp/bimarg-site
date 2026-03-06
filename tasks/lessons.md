# tasks/lessons.md — Lecciones aprendidas

## Formato
```
### [Fecha] Patrón aprendido
- Contexto: qué pasó
- Solución: cómo se resolvió
- Regla: qué hacer de ahora en adelante
```

---

### 2026-03-05 — Deploy con gh CLI en Windows
- Contexto: `gh auth login` no funciona en shell no-interactivo
- Solución: usar variable de entorno `GH_TOKEN` en lugar de `gh auth login --with-token`
- Regla: siempre autenticar con `export GH_TOKEN=...` en este entorno

### 2026-03-05 — curl en Git Bash (Windows)
- Contexto: `curl` no disponible en PATH de Git Bash; `curl.exe` tampoco accesible directamente
- Solución: usar `powershell.exe -Command "Invoke-RestMethod ..."` para llamadas HTTP
- Regla: para HTTP requests en este entorno, preferir PowerShell scripts en C:/Temp/

### 2026-03-05 — Python en Windows
- Contexto: `python3` no reconocido en Git Bash
- Solución: usar `powershell.exe -Command "python3.exe ..."` o invocar directamente con `python3.exe`
- Regla: scripts Python ejecutar via `powershell.exe -Command "python3.exe 'ruta' ..."`

### 2026-03-05 — Netlify GitHub App (deploy automático)
- Contexto: `installation_id` vacío al conectar repo via API — la GitHub App de Netlify no estaba instalada
- Solución: crear deploy hook en Netlify + webhook en GitHub apuntando al hook
- Regla: para deploy automático sin OAuth, usar webhook GitHub → Netlify build hook

### 2026-03-06 — UI/UX Pro Max skill
- Contexto: skill clonado en `.claude/skills/ui-ux-pro-max/`
- Solución: ejecutar search con `powershell.exe -Command "python3.exe 'C:\bimarg-site\.claude\skills\ui-ux-pro-max\src\ui-ux-pro-max\scripts\search.py' ..."`
- Regla: usar dominios `style`, `landing`, `typography`, `color`, `ux` para consultas de diseño
