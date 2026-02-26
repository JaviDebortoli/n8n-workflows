# 🎓 Scraping Inteligente de Cursos con IA

---

## 📌 Descripción
Este workflow implementa un pipeline automatizado para:
1. Recopilar sitios web para scraping desde Google Sheets.
2. Realizar scraping automático del contenido.
3. Convertir HTML a Markdown para facilitar el procesamiento.
4. Utilizar un Agente de IA para estructurar la información en formato JSON.
5. Persistir datos específicos de los cursos en Google Sheet.
6. Realizar un scraping profundo por cada curso usando Firecrawl.
7. Crear un Google Doc por cada curso con su temario e información formateada.
8. Vincular cada documento generado en la planilla consolidada.
Este proyecto combina scraping, procesamiento estructurado con LLMs, automatización documental y persistencia en Google Workspace.

---

🔌 Tecnologías integradas
- n8n (orquestador)
- Google Sheets (fuente y persistencia)
- HTTP Request (scraping inicial)
- Agente IA (Google Gemini)
- Firecrawl (scraping avanzado)
- Google Docs

---

⚙️ Arquitectura
- Scraping multi-etapa
- Orquestación con LLMs
- Uso de Output Parsers estructurados
- Transformación HTML → Markdown
- Procesamiento iterativo con SplitInBatches}
- Persistencia incremental
- Integración avanzada con Google Workspace
- Output Parser estructurado
