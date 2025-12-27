# n8n-workflows

Este repositorio contiene una colección de workflows creados en [n8n](https://n8n.io/) para automatizar tareas usando herramientas como Google Sheets, Gmail, WhatsApp, Asana, Calendly y APIs externas (como PiAPI, ElevenLabs, Creatomate).

> ✅ **Repositorio público (public template-safe):**  
> - **No** se almacenan credenciales, API keys, tokens ni secretos en los `.json`.  
> - Los workflows que requieren claves/IDs usan **variables de entorno (ENV vars)** en n8n.  
> - Las credenciales OAuth (Google/OpenAI/etc.) se configuran **en n8n**, no en GitHub.

---

## 📂 Workflows incluidos

### 1. 🎬 AI Automated TikTok/YouTube Shorts/Reels Generator
Genera automáticamente contenido visual (imagen + video + voz) usando prompts creativos y APIs de generación como Flux, Kling, ElevenLabs y Creatomate.

**Requisitos (este workflow):**
- ENV vars: `PIAPI_KEY`, `ELEVENLABS_API_KEY`, `CREATOMATE_API_KEY`, `CREATOMATE_TEMPLATE_ID`, `GOOGLE_SHEET_ID`, `GOOGLE_DRIVE_FOLDER_ID`, `DISCORD_WEBHOOK_URL`
- Credenciales en n8n: OpenAI + Google OAuth (Sheets/Drive)

**Seguridad (Drive):**
Los nodos de “share” deben quedar como:
- `role: reader`
- `allowFileDiscovery: false`

### 2. 📅 Automate Event Creation in Google Calendar from Google Sheets
Crea eventos automáticamente en Google Calendar al detectar nuevas filas en una hoja de cálculo de Google Sheets.

### 3. 📊 Clasificación área
Recibe formularios desde Sheets, valida emails y envía confirmaciones automáticas por Gmail, clasificando la información.

### 4. 🎉 Cumpleaños (Sheets + Gmail)
Envía saludos automáticos de cumpleaños diarios según una hoja de cálculo, filtrando por la fecha actual.

### 5. ✅ Etapa1_ResumenTareas_v2
Lee tareas desde una hoja, valida estructura y loguea errores HTTP según severidad; notifica por email si corresponde.

### 6. 🛒 Inventario - Alerta stock < 10
Detecta productos con stock bajo en Sheets y envía alertas automáticas por Gmail si el nivel cae por debajo de 10 unidades.

### 7. 📌 Status tareas (Asana → Teams)
Consulta tareas en Asana, detecta vencidas y envía resumen automático a Microsoft Teams para cada responsable.

### 8. 📆 Turnero (Calendly + WhatsApp)
Conecta eventos nuevos de Calendly con una hoja de turnos y envía confirmaciones por WhatsApp mediante la API de Meta.

---

## 📥 Importar workflows en n8n

1. Abrí [n8n](https://app.n8n.cloud/) o tu instancia self-hosted.
2. En el menú lateral, seleccioná **Workflows → Import from File**.
3. Subí cualquiera de los archivos `.json` desde la carpeta `workflows/`.
4. Configurá las credenciales requeridas en n8n (ver sección de credenciales).
5. Si el workflow usa ENV vars, setealas y reiniciá n8n (ver sección ENV vars).

---

## 🔐 Variables de entorno (ENV vars) para workflows públicos

> ⚠️ **Nunca comitees valores reales** en un repo público.

### Variables requeridas (cuando aplique)
- `PIAPI_KEY` – PiAPI (Flux/Kling)
- `ELEVENLABS_API_KEY` – ElevenLabs
- `CREATOMATE_API_KEY` – Creatomate
- `CREATOMATE_TEMPLATE_ID` – Template ID de Creatomate
- `GOOGLE_SHEET_ID` – ID del Google Sheet (documentId)
- `GOOGLE_DRIVE_FOLDER_ID` – ID de carpeta Drive para uploads
- `DISCORD_WEBHOOK_URL` – Webhook URL de Discord

### Ejemplo `.env` (NO comitear)
```env
PIAPI_KEY=your_piapi_key
ELEVENLABS_API_KEY=your_elevenlabs_key
CREATOMATE_API_KEY=your_creatomate_key
CREATOMATE_TEMPLATE_ID=your_creatomate_template_id

GOOGLE_SHEET_ID=your_sheet_id
GOOGLE_DRIVE_FOLDER_ID=your_drive_folder_id

DISCORD_WEBHOOK_URL=https://discord.com/api/webhooks/...

