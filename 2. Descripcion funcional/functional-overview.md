# 2. Descripción funcional

Los requisitos funcionales de alto nivel para el nuevo IUGO son los siguientes:

## 1. Carga de usuarios y assets

* El sistema deberá cargar periódicamente (**TBD**) los conductores/vehículos/propietarios registrados en las empresas de transporte/Administradores de flotas/placas.

* El sistema no deberá validar la información cargada por las empresas de transporte.

## 2. Enturnamiento

* El sistema deberá permitir a los los Administradores de los vehículos enturnar un vehículo y un conductor en una región (Caribe, Andina...), departamento (Antioquia, Boyacá...) o ciudad de origen (Medellín, Bogotá...).

* El sistema deberá validar que el usuario que desea enturar el vehículo y el conductor sea el administrador de los mismos.

* El sistema deberá permitir a los propietarios de los vehículos asignar a un *administrador de flota* como administrador de un vehículo propio.

![Tomar Turno][tomar_Turno]

[tomar_Turno]: ./assets/tomar-turno.png "Tomar Turno"

## 3. Solicitudes de Servicio

* El sistema deberá permitir a los Despachadores de las empresas de transporte crear solicitudes de servicio (carga). Las solicitudes de servicio contendrán información como el costo del flete, el origen, destino, fecha de recogida, los **posibles** tipos de vehículos requeridos para esta servicio y cantidad de los mismos.

* Las especificaciones y características que tiene la carga/el servicio

| Nombre        | Descripción   | 
| ------------- |:-------------:| 
| Tipo de Carga      |  (Carga granel solida,Carga granel liquida, Perecedera, Refrigerada, Frágil y Animales vivos) |
| Tipo de vehículo    | Turbo, Sencillo, DobleTroque, DobleTroque Cuatromanos, Minimula(Patineta), Tractomula 3 ejes |
| Cantidad de vehículo    | 1,2,3,4 |
| Opciones a elegir | Cabezote      | 
| Accesorios adicionales | TBD (Trailer y sus caracteristicas)      | 
| Observaciones | Barras de bloqueo, Lonas, Cinchas, Cinta de amarre, Mamparra, Cadenas, Pallets      | 
| Fechas | Fechas de recogida y de entregas      | 
| Fecha límite |   Fecha límite de Asignación de la Carga ( dentro de 24 horas)    |
| Costo del flete |   Puede estar dado por unidad de carga (# cajas), por volumen, por peso (tonelada) o por valor monetario    | 


![Crear solicitud][crear_solicitud]

[crear_solicitud]: ./assets/creacion-solicitud-carga.png "Crear solicitud de carga"

## 4. Asignación de turnos

* El sistema deberá presentar los vehículos que cumplan con las características requeridas para una solicitud de carga.

* El sistema deberá permitir a cada administrador de empresa establecer los criterios con los cuales se establece el orden en el cual se muestran los candidatos.

* El sistema deberá permitir a los Despachadores seleccionar los candidatos que consideren *aptos* para el transporte de la carga.

* El sistema deberá notificar a los administradores de flota que han sido pre-seleccionados por el despachador.

* El sistema deberá permitir a los Administradores de Flota aceptar dicha oferta y participar en la asignación de la carga.

* El sistema deberá permitir a los Despachadores seleccionar uno o varios de los ofertantes/candidatos, esto dependerá de la cantidad de vehículos necesarios para transportar dicha carga.

* El sistema deberá terminar la oferta una vez el despachador haya asignado la totalidad de vehículos requeridos para la solicitud de carga.

![Asignar turno][asignar_turno]

[asignar_turno]: ./assets/asignacion-turnos.png "Asignar turno"

## 5. Cambio de estados

* El sistema deberá permitir al conductor cambiar el estado de la solicitud de carga a **En transito** una vez se encuentra dentro de la zona de carga especificada en la solicitud de carga.

* El sistema deberá permitir al conductor cambiar el estado de la solicitud de carga a **Entregado** una vez se encuentre dentro de la zona de descarga especificada en la solicitud de carga.

![Cambio de estados][cambio_estados]

[cambio_estados]: ./assets/cambio-estados.png "Cambio estados"

**Enturnado:** Conductor esta disponible para hacer parte de la solicitud de servicio y match de vehículo.

**Aceptado:** Conductor acepta la solicitud de servicio y esta listo para ser asignado a su vehículo con la informacion del destino y  origen.

**En Transito:** Conductor esta en camino hacia su origen para cumplir con entrega de servicio.

**Entregado:** Conductor ha llegado a su destino y entregado el servicio.

**Emergencia:** Conductor tiene una inconvenience desde el estado Aceptado que lo impide cumplir con la recogida y entrega del servicio.

**No Disponible:** Conductor no se encuentra disponible para iniciar el proceso de Enturnamiento lo cual no cumple para ningula pre-seleccion de servicio.

**Enturnado, Aceptado, Cargando, En Transito, Entregado, Emergencia, No Disponible**

## 6. Calificación de actores

* El sistema deberá permitir al Conductor calificar de forma cuantitativa y cualitativamente al Generador de Carga, Empresa de Transporte y Vehículo.

	* Cumplimiento de tiempos de recogida y descarga
   
	* Uso del vehículo al entregar y retorno
   
	* Verificación de Documentación actualizada (Manifiesto aunque puede ser difícil de medir)
      
	* Kilometros recorridos por mes
   
* El sistema deberá permitir a la Empresa de Transporte calificar cuantitativa y cualitativamente al Conductor y Administrador de Flotas.

	* Fairness de asignación (Difícil en medir)
   
	* Veces de asignaciones
   
	* Asignaciones asignadas en fechas límites
   
	* Comentarios adicionales

* El sistema deberá permitir al Generador de Carga calificar cuantitativa y cualitativamente de forma tipo Survey

	* Estado del vehículo durante el transcurso asignado (recogida hasta entrega)
	
	* Estado de la carga entregada
	
	* Comportamiento del sistema al utilizarlo
   
	* Comentarios adicionales

* El sistema deberá permitir al Administrador de Flotas calificar cuantitativa y cualitativamente, Conductor y Empresa de Transporte.

	* Manejo de estados y su manipulacion (En especial el estado de Enturnarse y Desenturnarse)
   
	* Requisitos de solicitud de servicios (veces requerido)
   
	* Referidos
   

![Calificación][calificacion]

[calificacion]: ./assets/calificacion.png "Calificacion"


