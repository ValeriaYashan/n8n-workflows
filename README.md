# n8n-workflows

Este repositorio contiene una colección de workflows creados en [n8n](https://n8n.io/) para automatizar tareas usando herramientas como Google Sheets, Gmail, WhatsApp, Asana, Calendly y APIs externas (como PiAPI, ElevenLabs).

---

## 📂 Workflows incluidos

### 1. 🎬 AI Automated TikTok/YouTube Shorts/Reels Generator
Genera automáticamente contenido visual (imagen + video + voz) usando prompts creativos y APIs de generación como Flux, Kling y ElevenLabs.

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

1. Abrí [n8n](https://app.n8n.cloud/).
2. En el menú lateral, seleccioná **Workflows → Import from File**.
3. Subí cualquiera de los archivos `.json` desde la carpeta `workflows/`.

---

## 🧑‍💻 Autor

**Valeria Yashan**  
✉️ valeriayashan@gmail.com  
🌐 Automatizaciones low-code con IA y herramientas colaborativas.

---

