#  🛒 Automatización de gestión de stock con Google Forms + PostgreSQL

---

## 📌 Descripción

Workflow desarrollado en n8n que automatiza la gestión de inventario de una tienda de ropa a partir de respuestas recibidas en Google Forms. Cada nueva solicitud:
1. Se valida
2. Consulta el inventario en PostgreSQL
3. Descuenta stock si corresponde
4. Actualiza el estado en Google Sheets
5. Envía notificación por email

---

## 🔌 Tecnologías integradas
- n8n
- Google Sheets
- PostgreSQL
- Gmail
- Expresiones dinámicas
- Procesamiento por lotes

---

## ⚙️ Lógica de negocio implementada
- Evita reprocesar solicitudes verificadas
- Controla stock en tiempo real
- Maneja casos sin disponibilidad
- Genera notificación consolidada
- Actualiza estado de verificación automáticamente