# pedido-automatizado-n8n

Este proyecto es un **bot automatizado de pedidos y comprobantes para rotiserías** desarrollado con [n8n](https://n8n.io/).  
Permite recibir pedidos por Discord, procesarlos automáticamente, validar comprobantes de pago y enviar confirmaciones al cliente y al personal de la rotisería.

## Workflows incluidos

1. **pedido_rotiseria**  
   - Recibe pedidos en tiempo real desde un canal de Discord.
   - Valida los datos del pedido.
   - Envía notificaciones de confirmación al cliente y al personal de la rotisería.
   - Integra datos en Google Sheets para registro interno (opcional).

2. **recibir_comprobantes**  
   - Recibe comprobantes de pago enviados por los clientes.
   - Valida la información del comprobante (importe, CUIT/CUIL, CVU o alias de cuenta).
   - Marca el pedido como confirmado una vez que el comprobante es validado.
   - Envía notificaciones automáticas al cliente y al personal de la rotisería.

## Tecnologías

- [n8n](https://n8n.io/) — Plataforma de automatización.
- Discord API — Recepción y envío de mensajes.
- Google Sheets API — Registro de pedidos (opcional).
- Validación de datos de comprobantes (JSON, regex, lógica condicional).

## Instalación / Uso

1. Clonar el repositorio:
```bash
git clone https://github.com/TU_USUARIO/n8n-rotiseria-bot.git
```
2. Importar los workflows en n8n:
   - Abrir n8n.
   - Crear un nuevo workflow → Importar JSON desde workflows/pedido_rotiseria.json y workflows/recibir_comprobantes.json.

4. Configurar credenciales:
   - Discord Bot Token
   - Google Sheets API (si se usa)

4. Activar los workflows y empezar a recibir pedidos y comprobantes.
