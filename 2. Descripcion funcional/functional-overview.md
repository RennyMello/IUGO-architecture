# 2. Descripción funcional

Los requisitos funcionales de alto nivel para el nuevo IUGO son los siguientes.

## 1. Carga de usuarios y assets

* Se cargarán periodicamente (**to be defined**) los conductores/vehículos/propietarios registrados en las empresas de transporte/Administradores de flotas/placas.

* El sistema no validará la información cargada por las empresas de transporte.

## 2. Enturnamiento

* Los Administradores de los vehículos podrán enturnar un vehículo y un conductor en una región (Caribe, Andina...), departamento (Antioquia, Boyacá...) o ciudad de origen (Medellín, Bogotá...).

* Los Administradores de los vehículos deben de tener los permisos y autoridad para ser el actor de "toma de decisiones" de los vehículos que administra con el fin de hacer el match de la solicitud del servicio con el vehículo y conductor.

* Los Propietarios de los vehículos asignan a sus Administradores de vehículos de la toma de decisiones sobre los vehículos.

* Los conductores se pueden enturnar y desenturnar en cualquier momento. 

![Tomar Turno][tomar_Turno]

[tomar_Turno]: ./assets/tomar-turno.png "Tomar Turno"

## 3. Solicitudes de Servicio

* Los Despachadores de las empresas de transporte podrán crear solicitudes de servicio (carga). Las solicitudes de servicio contendrán información como el costo del flete, el origen, destino, fecha de recogida y los **posibles** tipos de vehículos requeridos para esta servicio y cantidad de los mismos.

* Las especificaciones y características que tiene la carga/el servicio
  
  Tipo de Carga: (Carga granel solida,Carga granel liquida, Perecedera, Refrigerada, Frágil y Animales vivos)
  
  Tipo de vehículo: **Resolucion 4308**
  
  Opciones a elegir: Cabezote
  
  Accesorios adicionales: TBD (Trailer y sus caracteristicas)
  
  Fechas de recogida y de entregas
  
  Fecha límite de Asignación de la Carga ( dentro de 24 horas)
  
  Rango de flete

![Crear solicitud][crear_solicitud]

[crear_solicitud]: ./assets/creacion-solicitud-carga.png "Crear solicitud de carga"

## 4. Asignación de turnos

* El sistema deberá presentar los vehículos que cumplan con las características requeridas para una solicitud de carga, los criterios con los cuales se establece el orden con el cual se muestren los candidatos deberá ser configurable para cada empresa de transporte.

* Los Despachadores seleccionarán los candidatos que consideren *aptos* para el transporte de la carga.

* El Sistema deberá notificar automaticamente a los administradores de flota que han sido pre-seleccionados (X pre-seleccionados) que cumplan con los criterios del servicio para transportar esta solicitud de carga.

* Los Administradores de Flota podrán aceptar dicha oferta y participar en la asignación de la carga.

* Los Despachadores seleccionarán uno o varios de los ofertantes/candidatos, esto dependerá de la cantidad de vehículos necesarios para transportar dicha carga.

* El Sistema deberá terminar la oferta una vez el despachador haya asignado la totalidad de vehículos requeridos para la solicitud de carga.

![Asignar turno][asignar_turno]

[asignar_turno]: ./assets/asignacion-turnos.png "Asignar turno"

## 5. Cambio de estados

* El conductor podrá cambiar el estado de la solicitud de carga a **En transito** una vez se encuentra dentro de la zona de carga especificada en la solicitud de carga.

* El conductor podrá cambiar el estado de la solicitud de carga a **Entregado** una vez se encuentre dentro de la zona de descarga especificada en la solicitud de carga.

![Cambio de estados][cambio_estados]

[cambio_estados]: ./assets/cambio-estados.png "Cambio estados"

**Enturnado:** Conductor esta disponible para hacer parte de la solicitud de servicio y match de vehículo.

**Aceptado:** Conductor acepta la solicitud de servicio y esta listo para ser asignado a su vehículo con la informacion del destino y  origen.

**En Transito:** Conductor esta en camino hacia su origen para cumplir con entrega de servicio.

**Entregado:** Conductor ha llegado a su destino y entregado el servicio.

**Emergencia:** Conductor tiene una inconvenience desde el estado Aceptado que lo impide cumplir con la recogida y entrega del servicio.

**Deserturnarse:** 

**Enturnado, Aceptado, Cargando, En Transito, Entregado, Emergencia, Desenturnarse**

## 6. Calificación de actores

* El Conductor podrá calificar de forma cuantitativa y cualitativamente al Generador de Carga, Empresa de Transporte y Vehículo.

   Cumplimiento de tiempos de recogida y descarga
   
   Uso del vehículo al entregar y retorno
   
   Verificación de Documentación actualizada (Manifiesto aunque puede ser difícil de medir)
   
   Kilometros recorridos por mes

* La Empresa de Transporte podrá calificar cuantitativa y cualitativamente al Conductor y Administrador de Flotas.

   Fairness de asignación (Difícil en medir)
   
   Veces de asignaciones
   
   Asignaciones asignadas en fechas limites

* El Generador de Carga podrá calificar cuantitativa y cualitativamente, Vehículo y Empresa de Transporte.

   Estado del vehículo durante el transcurso asignado (recogida hasta entrega)
   
   Kilometraje (Excesivo y Moderado)

* El Administrador de Flotas podrá calificar cuantitativa y cualitativamente, Conductor y Empresa de Transporte.

   Manejo de estados y su manipulacion (En especial el estado de Enturnarse y Desenturnarse)
   
   Requisitos de solicitud de servicios (veces requerido)
   
   Referridos
   

![Calificación][calificacion]

[calificacion]: ./assets/calificacion.png "Calificacion"


**TODO: Revisar sintáxis requisitos funcionales**
