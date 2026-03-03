# 🗺️ Scraping de Google Maps con Extracción de Contactos

---

## 📌 Descripción
Este workflow automatiza la recolección de datos de negocios a partir de Google Maps, extrae la información de contacto disponible en sus sitios web y guarda todo de forma organizada en Google Sheets.
Su objetivo principal es resolver el problema de la prospección manual de leads, tarea que típicamente consume mucho tiempo y esfuerzo. Con esta automatización podés construir una base de datos de empresas con contactos listos para uso en campañas de marketing, ventas o desarrollo de negocio de forma completamente automática.

Automáticamente, cada cierto intervalo (por ejemplo, cada 30 minutos), ejecuta las siguientes etapas:
1. Hace scraping de datos de negocios desde Google Maps utilizando el actor de Apify Google Places
2. Guarda la información básica (nombre, dirección, teléfono, sitio web) en Google Sheets.
3. Filtra los negocios que sí tienen sitio web.
4. Realiza scraping de cada sitio web con Firecrawl para obtener contenido completo de cada sitio.
5. Extrae información de contacto (correos electrónicos, perfiles de LinkedIn, Facebook, Instagram y Twitter) a partir del contenido scrapeado.
6. Guarda los datos extraídos en hojas de Google Sheets organizadas para facilitar su análisis y seguimiento.

---

## 🔌 Tecnologías integradas
- n8n (orquestador)
- Google Sheets (fuente y persistencia)
- Apify (Google Maps Scraper)
- Firecrawl (scraping avanzado)
- Filtros / Batches