# Dudas de Administración Avanzada de Redes y Servidores

## 1. Características de un protocolo ideal de acceso múltiples para un canal broadcast de R bps

**Pregunta:**
¿Cuáles son las características de un protocolo ideal de acceso múltiples para un canal broadcast de R bps?

**Respuesta:**

Un protocolo ideal de acceso múltiples para un canal broadcast de R bps debe cumplir con las siguientes características:

### Descentralización
- **No habrá un único nodo maestro encargado del control**: El protocolo debe funcionar sin depender de un nodo central que coordine las transmisiones.
- **No supeditar al fallo del nodo maestro**: Al ser descentralizado, el sistema no debe verse afectado por el fallo de un único nodo, mejorando la robustez y disponibilidad del sistema.
- **Sin sincronización**: El protocolo no debe requerir sincronización entre los nodos para funcionar correctamente.

### Características adicionales de un protocolo ideal

1. **Eficiencia del canal**: Cuando solo un nodo tiene datos para transmitir, debe poder utilizar todo el ancho de banda R bps.

2. **Equidad**: Cuando M nodos tienen datos para transmitir, cada uno debe obtener un rendimiento promedio de R/M bps.

3. **Simplicidad**: El protocolo debe ser simple de implementar y no requerir hardware especializado o complejo.

---

*Última actualización: Diciembre 2025*
