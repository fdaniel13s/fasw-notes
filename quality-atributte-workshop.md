## QAS - Categoría de Requerimientos:
- **Requerimientos Funcionales**: funciones del sistema
- **Atributos de Calidad**: propiedad medible
  - **Escenarios de atributos de calidad**: Permite caracterizar/capturar aspectos de atributos de calidad de una forma que pueda ser evaluado y utilizado en diseño.
  - **Tácticas**: Las “tácticas” de arquitectura no son fines en sí mismas, son formas de alcanzar atributos de calidad deseados. Una táctica es una decisión de diseño que influye en la respuesta de un atributo de calidad.
### Diseños de calidad
- **Categorías**:
  1. Allocation of Responsibilities
  2. Coordination Model
  3. Data Model
  4. Management of Resources
  5. Mapping among architectural elements
  6. Binding time decisions
  7. Choice of technology
### Atributos Relacionados con la Calidad del Sistema:
- **Disponibilidad**
- **Interoperabilidad**
- **Modificabilidad**
- **Performance**
- **Seguridad**
- **Testeabilidad**
- **Usabilidad**
- **Restricciones**: Características que no pueden ser negociadas.
### Drivers Arquitectónicos:

## Criterios de elección
La elección se determina considerando los siguientes criterios:

- **Relevancia** en la satisfacción de los objetivos del negocio del sistema.
- **Complejidad técnica** que represente su implementación.
### Drivers de Restricciones
- A diferencia de los drivers funcionales y de atributos de calidad, los requerimientos de este tipo no tienen prioridad.
- Todas las restricciones son consideradas drivers de la arquitectura.
### Ejemplo de drivers de atributos de calidad:
1. **Disponibilidad**:
    - El sistema debe estar disponible las 24 horas del día, los 7 días de la semana, con un tiempo de inactividad mínimo planificado para mantenimiento.
    - Se requiere capacidad de recuperación automática en caso de fallas para garantizar la continuidad del servicio.
2. **Rendimiento (Performance)**:
    - El sistema debe ser capaz de procesar un gran volumen de transacciones dentro de tiempos de respuesta aceptables.
    - Se especifica una velocidad mínima de carga para las páginas web o aplicaciones móviles.
3. **Seguridad**:
    - El sistema debe cumplir con estándares de seguridad específicos, como cifrado de datos, autenticación multifactor y control de acceso basado en roles.
    - Se requiere cumplimiento con normativas de protección de datos, como GDPR, HIPAA, PCI-DSS, etc.
4. **Fiabilidad (Reliability)**:
    - El sistema debe ser confiable y resistente a fallas, minimizando el riesgo de errores o fallos que afecten la disponibilidad del servicio.
    - Se especifica un tiempo medio entre fallos (MTBF) o un tiempo medio de reparación (MTTR) objetivo.
5. **Usabilidad**:
    - La interfaz de usuario debe ser intuitiva, fácil de usar y accesible para un público diverso.
    - Se especifican criterios de accesibilidad para garantizar que el sistema sea utilizable por personas con discapacidades.
6. **Mantenibilidad (Maintainability)**:
    - El sistema debe ser fácil de mantener y actualizar, permitiendo cambios en el código o la configuración con bajo impacto en otras partes del sistema.
    - Se requiere documentación detallada y clara del código fuente y la arquitectura.
7. **Escalabilidad (Scalability)**:
    - El sistema debe ser capaz de manejar un aumento en la carga de trabajo al agregar más usuarios o recursos sin comprometer el rendimiento.
    - Se especifica una estrategia de escalado horizontal o vertical para anticipar el crecimiento futuro.
8. **Interoperabilidad**:
    - El sistema debe ser capaz de integrarse y comunicarse eficazmente con otros sistemas o plataformas externas.
    - Se requiere soporte para estándares de interoperabilidad como APIs abiertas, protocolos comunes o formatos de intercambio de datos.
9. **Tolerancia a Fallos (Fault Tolerance)**:
    - El sistema debe ser capaz de recuperarse automáticamente de errores o fallos parciales sin interrupción del servicio.
10. Reliability - Confiabilidad: El sistema debe ser confiable y resistente a fallas, minimizando el riesgo de errores o fallos que afecten la disponibilidad del servicio. Se especifica un tiempo medio entre fallos (MTBF) o un tiempo medio de reparación (MTTR) objetivo.
