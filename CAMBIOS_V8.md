# SCADA VOLTIQ 09 — Premium V8 · Feria interactiva

## Cambios visibles

- Nuevo **Centro de maniobras** con indicación clara del modo activo.
- **Banco virtual:** un solo clic abre o cierra cualquiera de los seis interruptores.
- **APAGAR TODO · VIRTUAL:** un clic abre los seis interruptores del simulador, sin enviar mensajes MQTT.
- Animación de respuesta, mensajes discretos y registro local.
- Se conservan navegación Premium, diagrama unifilar, datos MQTT y gráficas INA226.

## Comportamiento real conservado de la V7.2

- El panel puede conectarse a MQTT para supervisión y recibir telemetría.
- La orden física **ABRIR** se envía con un clic bajo las condiciones de conexión de la V7.2.
- La orden física **CERRAR** mantiene la pulsación sostenida de 0,85 segundos y la confirmación /state; no se eliminó esa precaución.
- El botón **APAGAR TODO · VIRTUAL** se deshabilita conectado al ESP32 y NO representa un paro de emergencia físico.

## Preparación

Ejecuta `npm ci`, `npm test` y `npm run build`. Para Vercel: Framework Vite, Build `npm run build`, Output `dist`.

La telemetría INA226 B y C requiere que el firmware la publique; la versión de firmware compartida antes solo publicaba INA226 A.
