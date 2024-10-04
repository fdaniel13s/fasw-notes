# Pregunta 4: Análisis ADD (Attribute-Driven Design)

## Drivers Principales, Atributos de Calidad y Tácticas

### 1. Driver Principal: Seguridad
**Atributo de Calidad:** Seguridad
**Tácticas recomendadas:**
- Detección de intrusos: Implementada a través de los servicios UTM y HoneyPot.
- Autenticación: Necesaria para el acceso a la aplicación web de administración.
- Autorización: Para controlar el acceso a diferentes funcionalidades según el rol del usuario.
- Encriptación: Utilizada en las comunicaciones VPN y potencialmente en el almacenamiento de datos sensibles.

### 2. Driver Principal: Rendimiento
**Atributo de Calidad:** Eficiencia de rendimiento
**Tácticas recomendadas:**
- Procesamiento paralelo: Utilizado en los servicios UTM para analizar grandes volúmenes de tráfico.
- Distribución de carga: Implementada a través del balanceador mencionado en la arquitectura.
- Gestión de recursos: Separación de servicios en diferentes equipos para optimizar el uso de recursos.

### 3. Driver Principal: Escalabilidad
**Atributo de Calidad:** Escalabilidad
**Tácticas recomendadas:**
- Diseño modular: La arquitectura basada en servicios permite escalar componentes individualmente.
- Replicación: Posibilidad de replicar servicios críticos como UTM o HoneyPot.
- Particionamiento: Distribución de la carga de trabajo entre diferentes instancias o nodos.

## Artefactos Mencionados en el Caso

1. **Balanceador:** Componente que distribuye el tráfico entre múltiples instancias de la plataforma.

2. **Aplicación Web de Administración:** Interfaz para configurar servicios y consultar el tráfico.

3. **ESB (Enterprise Service Bus):** Procesa grandes cantidades de información en forma de mensajes.

4. **API Gateway:** Dirige el tráfico hacia los servicios señuelos en el HoneyPot.

5. **Servicios UTM:** Conjunto de funcionalidades para identificar amenazas del tráfico externo.

6. **Servicios HoneyPot:** Software señuelo que simula servicios vulnerables para atraer y analizar ataques.

7. **Servicios NOC-SOC:** Servicios de alerta y actualización para la detección de amenazas.

8. **Servicios de LOG:** Almacena información en archivos de texto para su posterior análisis.

9. **Servicio de Configuración:** Permite configurar la funcionalidad de la plataforma.

10. **Base de Datos Derby:** Almacena la configuración de la plataforma.

11. **Sistema de Archivos:** Utilizado para almacenar logs y archivos de tráfico detectado.

Estos drivers, atributos de calidad, tácticas y artefactos forman la base de la arquitectura de la Plataforma de Ciberseguridad, proporcionando un diseño robusto, escalable y seguro que cumple con los requisitos establecidos en el caso.