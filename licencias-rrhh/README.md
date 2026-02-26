#  🏖️ Gestión automática de licencias

---

## 📌 Descripción
Este workflow implementa un proceso completo de gestión de solicitudes de licencia de empleados. El flujo:
1. Recibe una solicitud al endpoint disparador del flujo (POST /ask/form).
2. Validación técnica del body:
    - Formato del correo electrónico.
    - Fechas en formato ISO (YYYY-MM-DD).
    - Presencia de campos obligatorios.
    - Longitud máxima de comentarios.
3. Calculo de días solicitados.
4. Verificar que la solicitud cumpla con las siguientes reglas de negocio:
    - Haber sido solicitada con una annticipación mínima de 7 dias.
    - Que la cantidad de dias solicitados sea positiva y mayor que 0.
    - Verificar en la BD que el empleado cuente con suficientes días de licencia acumulados.
5. Aprobación humana (RRHH)
6. Se envía mensaje a RRHH vía Discord.
7. Se establece un límite de 48 horas para aprobar o rechazar la solicitud a un endpoint generado dinámicamente.
8. Si RRHH aprueba:
    - Se actualiza la BD descontando días de licencia al empleado.
    - Se crea un evento en Google Calendar.
    - Se envía mail de aprobación al empleado.
9. En caso de rechazo o falla en las validaciones:
    - Se envía mail detallando motivo.
    - No se actualiza base de datos.
    - No se crea evento en calendario.

---

## 🔌 Tecnologías integradas
- n8n
- PostgreSQL
- Discord
- Google Calendar
- Gmail
- Webhooks autenticados

---

## ⚙️ Arquitectura
Este workflow demuestra:
- API REST con autenticación.
- Validación estructural y de negocio.
- Separación entre validación técnica y lógica empresarial.
- Persistencia transaccional.
- Aprobación humana asincrónica.
- Timeout controlado con Wait.
- Orquestación multi-servicio.
- Manejo explícito de errores.
