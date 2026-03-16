# 🤖 AI Personal Assistant con Gmail y Google Calendar

---

## 📌 Descripción general
Este proyecto implementa un asistente personal basado en IA desarrollado con n8n, capaz de gestionar correo electrónico y calendario mediante instrucciones en lenguaje natural proporcionadas por el usuario a través de un chat.

El asistente utiliza un agente de IA basado en Gemini que interpreta las instrucciones del usuario y decide qué acciones ejecutar mediante herramientas conectadas al sistema. Estas herramientas incluyen:

- Operaciones sobre Gmail.
- Gestión de Google Calendar.
- Clasificación automática de correos electrónicos mediante un workflow personalizado.

El objetivo del sistema es automatizar tareas cotidianas de productividad para trabajadores del conocimiento, como:

- Leer y gestionar correos electrónicos.
- Redactar y enviar respuestas.
- Organizar reuniones y eventos.
- Consultar disponibilidad del calendario.
- Clasificar correos de acuerdo a tópicos y justificarlo.

El agente mantiene contexto conversacional y aplica reglas específicas de productividad para asegurar una gestión eficiente del tiempo y la comunicación.

---

## ⚙️ Arquitectura
```text
Asistente (Agente principal)
│
├── Clasificador (Tool personalizada)
│
├── Gmail MCP (Servidor de herramientas de correo)
│
└── Calendar MCP (Servidor de herramientas de calendario)
```

### 🔗 Model Context Protocol (MCP)

El proyecto utiliza Model Context Protocol (MCP) para exponer herramientas al agente de IA.

MCP permite que los modelos de lenguaje interactúen con sistemas externos mediante interfaces estructuradas.

En este proyecto se implementan dos servidores MCP:
- Gmail MCP Server
- Google Calendar MCP Server

Esto permite que el agente utilice herramientas externas de forma segura y estructurada.

### 📦 Arquitectura basada en herramientas

El sistema sigue un enfoque de Tool-based Agent Architecture, donde el agente no ejecuta acciones directamente, sino que utiliza herramientas especializadas.

Esto mejora:
- modularidad
- mantenibilidad
- escalabilidad del sistema

---

## 🚀 Capacidades del asistente
Este asistente puede encargarse de:

- Gestión de correo
    - leer correos
    - redactar respuestas
    - enviar correos
    - crear borradores
    - clasificar correos por tópicos comunes
    - marcar correos como leídos o no leídos
    - eliminar correos
- Gestión de agenda
    - consultar eventos
    - crear reuniones
    - modificar eventos
    - cancelar reuniones
    - verificar disponibilidad
- Organización personal
    - evitar conflictos de agenda
    - priorizar productividad
    - aplicar reglas de horario laboral

---

## 🔌 Tecnologías integradas

- n8n (orquestación).
- Google Gemini (modelo de lenguaje).
- LangChain Nodes (framework de agentes).
- Model Context Protocol (MCP).
- Gmail API (gestión de correo).
- Google Calendar API (gestión de agenda).
- OAuth2 (autenticación).
- JSON Structured Output (comunicación estructurada).