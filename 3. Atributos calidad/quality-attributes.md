# 3. Atributos de calidad

 ![Quality Radar][quality-radar]
 
Los escenarios de calidad para IUGO son los siguientes

1. **Avalability (Disponibilidad) 20%:**

     Referes to a property of software that is there an ready to carry out its task when you need it to be. Availability builds upon the concepto of reliability by adding the notion of recovery - that is, when the system breaks, it reparis itself.

     * La creación de solicitudes de carga y busqueda de transportadores deberá estar disponible 24x7, aunque un downtime de menos de 30 minutos pasadas las 10 de la noche es tolerable.

     * El fallo de un componente no comprometerá el funcionamiento de otros componentes, es decir, si el componente encargado de las calificaciones falla, no deberá evitar la creación de solicitudes de carga o el enturnamiento de vehículos.

     ![server-unresponsive][availability-server-unresponsive]

     ![availability-server-unresponsive-late-response][availability-server-unresponsive-late-response]
     
     * El fallo de un componente ante el estímulo de un usuario no conducirá a la generación una falla mayor en el sistema.

     ![server-unresponsive-user-request][availability-server-unresponsive-user-request]

2. **Interoperability (Interoperabilidad) 5%:**

    Interoperability is about the degree to which two or more system can usefully exchange meaningul information via interfaces in a particular context.

    * IUGO cargará inicialmente la información necesaria (conductores y vehículos) para su correcto funcionamiento de sistemas externos, las interfaces con los sistemas de datos existentes deben ajustarse a los formatos de datos de IUGO y utilizarlos.

3. **Modifiability (Modificabilidad) 20%:**

     Referes to the cost of change, both in time and money

     * IUGO será un sistema altamente cambiante, esto debido a que es un producto único en el mercado y el público objetivo no son miembros permanentes del equipo de desarrollo. Cada componente deberá tener un acomplamiento bajo y una alta cohesión.

     * Cada componente deberá ser facilmente reemplazado y/o modificado.

4. **Performance 10%:**

    It's about time and the software system's ability to meet timing requirements. When events occur-interrupts, messages, requests from user or other systems, or clock events marking the passage of time, the system, or some element of the system, must respond to them in time.

    * El procesamiento de un evento generado por un componente no deberá tardar más de 5 segundos en promedio para ser procesado.

    ![performance event process time][performance-event-process-time]

5. **Security (Seguridad) 10%:**

    Security is a measure of the system's ability to protect data and information from unauthorized access while still providing access to people and systems that are authorized.

    * La información de los vehículos y conductores propios de cada empresa de transporte deberá ser visible sólo para los administradores de flota y despachadores de cada empresa.
    
    * Visibilidad para los Administradores de Flotas para poder ver los conductores afiliados/asociados a las demás empresas.
    
    ![Security data protection][security-dataprotection]

    * Los conductores que han aceptado un turno no podrán ser suplantados por otras personas para llevar acabo el transporte de la carga.

6. **Testability (Testabilidad) 10%:**

    Referes to the ease with which software can be made to demonstrate its faults through (typically execution-based) testing.

    * Cada componente del sistema deberá tener una cobertura mínima de su código mediante pruebas unitarias de un 85%.

    * La UI de cada contexto deberá tener pruebas de aceptación que cubran al menos 70% de los diferentes flujos de la aplicación.

7. **Usability (Usabilidad) 25%:**

    Usability is concerned with how easy it is for the user to accomplish a desired task and the kind of user support the system provides.

    IUGO será utilizado por personas con una forma física endomórfica, es decir contextura gruesa, además de poseer un bajo conocimiento técnico en el uso de aplicaciones móviles.

    * El conductor de un vehículo deberá poder utilizar la aplicación de manera productiva después de diez minutos de haber instalado la aplicación. (Cambios de estado).

    * El administrador de flotas deberá poder utilizar la aplicación de manera productiva después de treinta minutos de haber instalado la aplicación. (Enturnamiento, Aceptar ofertas de solicitudes de carga)

    
     <!-- Misc -->
    [quality-radar]: ./assets/IUGO-quality-radar.PNG "IUGO quality radar"
    

     <!-- Availability -->
     [availability-server-unresponsive]: ./assets/availability-server-unresponsive.PNG "availability server unresponsive"
    
     [availability-server-unresponsive-late-response]: ./assets/availability-server-unresponsive-late-response.PNG "availability server unresponsive late response"

     [availability-server-unresponsive-user-request]: ./assets/availability-server-unresponsive-user-request.PNG "availability server unresponsive"


    <!-- Performance -->
     [performance-event-process-time]: ./assets/performance-event-process-time.PNG "performance event process time"

    <!-- Security -->
    [security-dataprotection]: ./assets/security-dataprotection.PNG "Security data protection"
    
    
