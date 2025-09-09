# API REST de Boorie

Documentación completa de la API REST de Boorie para integraciones empresariales.

## 🔐 Autenticación

Boorie soporta múltiples métodos de autenticación:

- **API Key**: Para aplicaciones simples
- **OAuth 2.0**: Para integraciones empresariales
- **JWT**: Para aplicaciones web/móviles

## 📍 Base URL

```
https://api.boorie.org/v1
```

Para desarrollo local:
```
http://localhost:8000/v1
```

## 🚀 Endpoints Principales

### Análisis de Redes

- `POST /analyze` - Ejecutar análisis completo
- `POST /analyze/quick` - Análisis rápido
- `GET /analyze/{id}` - Obtener resultados de análisis
- `GET /analyze/{id}/report` - Descargar reporte

### Gestión de Redes

- `GET /networks` - Listar redes
- `POST /networks` - Crear nueva red
- `GET /networks/{id}` - Obtener detalles de red
- `PUT /networks/{id}` - Actualizar red
- `DELETE /networks/{id}` - Eliminar red

### Herramientas Especializadas

- `POST /tools/pressure-analysis` - Análisis de presiones
- `POST /tools/leak-detection` - Detección de fugas
- `POST /tools/energy-optimization` - Optimización energética
- `POST /tools/water-quality` - Análisis de calidad del agua

### Agente IA

- `POST /agent/query` - Consulta al agente
- `GET /agent/conversations` - Historial de conversaciones
- `POST /agent/feedback` - Enviar retroalimentación

## 📊 Ejemplos de Uso

### Python
```python
import requests

# Configuración
API_KEY = "tu-api-key"
BASE_URL = "https://api.boorie.org/v1"

headers = {
    "Authorization": f"Bearer {API_KEY}",
    "Content-Type": "application/json"
}

# Analizar una red
with open("network.inp", "rb") as f:
    response = requests.post(
        f"{BASE_URL}/analyze",
        headers=headers,
        files={"file": f},
        data={"stage": "preliminary"}
    )
    
analysis_id = response.json()["id"]
print(f"Análisis iniciado: {analysis_id}")
```

### JavaScript
```javascript
const API_KEY = 'tu-api-key';
const BASE_URL = 'https://api.boorie.org/v1';

// Consultar al agente
async function queryAgent(question) {
    const response = await fetch(`${BASE_URL}/agent/query`, {
        method: 'POST',
        headers: {
            'Authorization': `Bearer ${API_KEY}`,
            'Content-Type': 'application/json'
        },
        body: JSON.stringify({
            question: question,
            context: 'network_analysis'
        })
    });
    
    return response.json();
}

// Uso
const result = await queryAgent("¿Cómo optimizo la presión en mi red?");
console.log(result.answer);
```

### cURL
```bash
# Listar redes disponibles
curl -X GET "https://api.boorie.org/v1/networks" \
  -H "Authorization: Bearer tu-api-key"

# Ejecutar análisis rápido
curl -X POST "https://api.boorie.org/v1/analyze/quick" \
  -H "Authorization: Bearer tu-api-key" \
  -H "Content-Type: multipart/form-data" \
  -F "file=@network.inp" \
  -F "focus=pressure"
```

## 📝 Respuestas y Códigos de Estado

### Códigos de Éxito
- `200 OK` - Solicitud exitosa
- `201 Created` - Recurso creado exitosamente
- `202 Accepted` - Solicitud aceptada para procesamiento

### Códigos de Error
- `400 Bad Request` - Solicitud inválida
- `401 Unauthorized` - Autenticación requerida
- `403 Forbidden` - Sin permisos suficientes
- `404 Not Found` - Recurso no encontrado
- `429 Too Many Requests` - Límite de rate excedido
- `500 Internal Server Error` - Error del servidor

## 🔄 Webhooks

Configura webhooks para recibir notificaciones:

```json
POST /webhooks
{
  "url": "https://tu-servidor.com/webhook",
  "events": ["analysis.completed", "alert.triggered"],
  "secret": "tu-secreto-webhook"
}
```

## 📈 Límites y Cuotas

### Plan Gratuito
- 100 análisis/mes
- 1,000 consultas al agente/mes
- Redes hasta 1,000 nodos

### Plan Pro
- 10,000 análisis/mes
- Consultas ilimitadas al agente
- Redes hasta 100,000 nodos
- Soporte prioritario

### Plan Enterprise
- Límites personalizados
- SLA garantizado
- Soporte dedicado
- Instalación on-premise disponible

## 🆘 Soporte

- Documentación completa: [docs.boorie.org/api](https://docs.boorie.org/api)
- Estado de la API: [status.boorie.org](https://status.boorie.org)
- Soporte técnico: api-support@boorie.org