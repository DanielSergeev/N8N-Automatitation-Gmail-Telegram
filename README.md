# N8N-Automatitation-Gmail-Telegram
Plantilla configurada para automatizar un flujo de respuesta automática generada por Gemini hacia Gmail y Telegram

Este proyecto consiste en un pipeline de automatización intermodular desarrollado en **n8n**. 
Está diseñado para gestionar la atención al cliente de forma proactiva, analizando el sentimiento de los correos entrantes y respondiendo de manera autónoma.

## Funcionalidades
- **Filtrado por Dominio:** Procesa automáticamente correos provenientes de `murciaeduca.es`.
- **Análisis de Contenido:** Detecta palabras clave relacionadas con quejas o mensajes de tono negativo.
- **Respuesta Automática:** Emplea la API de Gmail (OAuth2) para enviar disculpas formales de forma inmediata.
- **Notificación en Tiempo Real:** Reenvía una alerta crítica a un Bot de Telegram para supervisión administrativa.

## 🛠️ Stack Tecnológico
- **Orquestador:** n8n (Self-hosted).
- **Infraestructura:** Docker & Docker Compose en Ubuntu VM.
- **APIs:** Gmail API (Google Cloud Console), Telegram Bot API.
- **Autenticación:** OAuth2.0.

## 🐳 Despliegue con Docker tanto en Linux/Windows

docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n

📥 Cómo usar la plantilla
Descarga el archivo ai-support-automator.json de la carpeta /workflows.

En tu instancia de n8n, selecciona "Import from File".

Configura tus credenciales de Gmail y el Token de Telegram.

