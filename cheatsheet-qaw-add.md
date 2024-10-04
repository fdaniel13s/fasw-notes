# QAW & ADD CheatSheet

## Quality Attribute Workshop (QAW)

El **QAW** es un proceso que se utiliza para identificar y priorizar los atributos de calidad del sistema. Estos atributos no funcionales (como rendimiento, disponibilidad, seguridad) guían el diseño arquitectónico. A continuación, se desglosan los elementos principales de un escenario típico de QAW:

### Componentes de un escenario

- **Origen**: ¿Quién o qué causará el escenario?
  - Ejemplo: Un usuario final, un sistema externo, una falla en el hardware.

- **Estímulo**: El evento que provoca la situación.
  - Ejemplo: El sistema recibe una petición de acceso, un aumento de la carga, una caída de un servidor.

- **Artefacto**: A qué módulo, componente u objeto recae el escenario.
  - Ejemplo: El módulo de autenticación, la base de datos, el API Gateway.

- **Respuesta**: Resumen de las tácticas a implementar para cumplir con los atributos de calidad ante el escenario.
  - Ejemplo: Aumentar la capacidad de las instancias del servidor, redirigir peticiones a una cola de mensajes.

- **Medida de la respuesta**: Una métrica cuantificable que define cómo se evaluará la respuesta del sistema en base al atributo de calidad.
  - Ejemplo: El tiempo de respuesta debe ser menor a 5 segundos, la disponibilidad debe ser mayor al 99.95%.

---

### Atributos de Calidad (Drivers No Funcionales)

Los atributos de calidad son esenciales para garantizar que el sistema cumpla con sus objetivos no funcionales. Aquí algunos de los principales atributos con ejemplos para guiar la implementación:

1. **Performance (Rendimiento)**
   - Medida: El sistema debe responder en un máximo de 5 segundos en condiciones normales.
   - Tácticas: Uso de caching, paginación, balanceo de carga.

2. **Disponibilidad (Availability)**
   - Medida: El sistema debe estar disponible el 99.95% del tiempo.
   - Tácticas: Replicación de bases de datos, failover automático.

3. **Confiabilidad (Reliability)**
   - Medida: El sistema no debe fallar más de 1 vez por cada 1000 solicitudes.
   - Tácticas: Test unitarios, simulaciones de fallos.

4. **Seguridad (Security)**
   - Medida: El sistema debe estar protegido contra ataques de inyección de SQL y XSS.
   - Tácticas: Implementación de un firewall de aplicaciones, cifrado de datos en tránsito y reposo.

5. **Modificabilidad (Modifiability)**
   - Medida: El tiempo para modificar una regla de negocio debe ser menor a 10 minutos.
   - Tácticas: Aplicación de principios SOLID, uso de patrones de diseño como Factory o Strategy.

6. **Escalabilidad (Scalability)**
   - Medida: El sistema debe soportar el doble de usuarios en horas pico sin degradación significativa del rendimiento.
   - Tácticas: Balanceo de carga horizontal, escalado automático en la nube.

7. **Mantenibilidad (Maintainability)**
   - Medida: El tiempo para resolver un bug debe ser inferior a 2 horas.
   - Tácticas: Clean code, modularización, pruebas automatizadas.

8. **Interoperabilidad (Interoperability)**
   - Medida: El sistema debe poder comunicarse con sistemas de terceros mediante REST y SOAP.
   - Tácticas: Uso de APIs abiertas, estandarización de formatos (JSON, XML).

9. **Auditabilidad (Auditability)**
   - Medida: Todas las transacciones financieras deben ser rastreables por al menos 5 años.
   - Tácticas: Generación de logs de transacciones, sistemas de auditoría en bases de datos.

---

### Tácticas Arquitectónicas

Son mecanismos que ayudan a cumplir con los atributos de calidad. Se implementan a través de decisiones de diseño y patrones. Aquí algunos ejemplos:

- **Balanceo de carga**: Distribuir peticiones entre varias instancias de servidor para mejorar la escalabilidad y disponibilidad.
- **Autenticación de dos factores (2FA)**: Mejora la seguridad del sistema.
- **Colas de mensajes**: Manejo eficiente de grandes cantidades de datos mediante la creación de colas en lugar de realizar procesos síncronos que pueden sobrecargar el sistema.
- **Paginación**: Reducción de la carga de datos enviados en una respuesta RESTful al paginar los resultados.

### Ejemplos de métricas para medir la respuesta:

- **Tiempo de respuesta**: El sistema debe responder en menos de 2 segundos.
- **Disponibilidad**: El sistema debe estar disponible el 99.9% del tiempo.
- **Uso de CPU**: El uso de CPU no debe superar el 70% en cargas máximas.
- **Escalabilidad**: El sistema debe soportar un 50% más de usuarios concurrentes sin afectar el rendimiento.

---

## ADD (Attribute Driven Design)

El **ADD** es un proceso utilizado para tomar decisiones arquitectónicas basadas en los atributos de calidad (drivers). A medida que el sistema crece en complejidad, el ADD proporciona un enfoque sistemático para descomponer el sistema en módulos o componentes que cumplen con los requisitos funcionales y no funcionales.

### Proceso de ADD

1. **Identificar los atributos de calidad (drivers)**
   Basados en los requerimientos y necesidades de los stakeholders.

2. **Asignar responsabilidades a los módulos**
   Descomponer el sistema en módulos o subsistemas para cumplir los atributos de calidad.

3. **Aplicar tácticas arquitectónicas**
   Elegir las tácticas que mejor satisfacen los atributos de calidad para cada módulo.

4. **Iterar y refinar**
   A medida que se avance en el diseño, se realizan ajustes y se optimizan las decisiones arquitectónicas.

---

## C4 Model

El **C4 Model** es una manera de visualizar la arquitectura de software en diferentes niveles de abstracción, permitiendo comprender cómo se estructura el sistema desde una vista general hasta una vista detallada.

### Niveles del C4 Model

1. **Context Diagram (C1)**
   - Define los actores principales y sistemas externos con los que interactúa tu sistema.
   - Ejemplo: Un sistema bancario interactúa con usuarios, cajeros automáticos y otros bancos.
   - **Atributo clave**: Interoperabilidad.
   - **Artefacto**: Sistema bancario central.
   - **Respuesta esperada**: Comunicación fluida con sistemas externos.

2. **Container Diagram (C2)**
   - Desglosa el sistema en contenedores (aplicaciones web, bases de datos, APIs) y cómo interactúan entre sí.
   - Ejemplo: Una API RESTful que interactúa con una base de datos y envía datos a una aplicación móvil.
   - **Atributo clave**: Escalabilidad.
   - **Artefacto**: API RESTful.
   - **Respuesta esperada**: Manejo de alta concurrencia mediante escalado horizontal.

3. **Component Diagram (C3)**
   - Muestra los componentes dentro de los contenedores y sus relaciones.
   - Ejemplo: Un componente de autenticación en la API que se comunica con un servicio de autorización.
   - **Atributo clave**: Seguridad.
   - **Artefacto**: Componente de autenticación.
   - **Respuesta esperada**: Validación de autenticación en menos de 100ms.

4. **Code Diagram (C4)**
   - Detalla el código o clases dentro de los componentes si es necesario un nivel de granularidad mayor.
   - Ejemplo: Una clase "User" que tiene métodos para autenticar a los usuarios.
   - **Atributo clave**: Mantenibilidad.
   - **Artefacto**: Clase "User".
   - **Respuesta esperada**: El código debe ser modificable en menos de 10 minutos sin afectar otras funcionalidades.

---