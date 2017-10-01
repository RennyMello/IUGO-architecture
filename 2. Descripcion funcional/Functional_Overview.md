# 2. Descripción funcional

Los requisitos funcionales de alto nivel para el nuevo IUGO son los siguientes.

## 1. Carga de usuarios y assets

* Se cargarán periodicamente (**to be defined**) los conductores/vehículos/propietarios registrados en las empresas de transporte.

* El sistema no validará la información cargada por las empresas de transporte.

## 2. Enturnamiento

* Los administradores de los vehículos podrán enturnar un vehículo y un conductor en una región (Caribe, Andina...), departamento (Antioquia, Boyacá...) o ciudad de origen (Medellín, Bogotá...).

![alt text][tomar_Turno]

[tomar_Turno]: ./TomarTurno.png "Tomar Turno"

## 3. Solicitudes de carga

* Los despachadores de las empresas de transporte podrán crear solicitudes de carga. Las solicitudes de carga contendrán información como el costo del flete, el origen, destino, fecha de recogida y los **posibles** tipos de vehículos requeridos para esta carga y cantidad de los mismos.

![alt text][crear_solicitud]

[crear_solicitud]: ./Creacion_solicitud_carga.png "Crear solicitud de carga"

## 4. Asignación de turnos

* El sistema deberá presentar los vehículos que cumplan con las características requeridas para una solicitud de carga, los criterios con los cuales se establece el orden con el cual se muestren los candidatos deberá ser configurable para cada empresa de transporte.

* Los despachadores seleccionarán los candidatos que consideren *aptos* para el transporte de la carga.

* El sistema deberá notificar a los administradores de flota que han sido pre-seleccionados para transportar esta solicitud de carga.

* Los administradores de flota podrán aceptar dicha oferta y participar en la asignación de la carga.

* Los despachadores seleccionarán uno o varios de los ofertantes, esto dependerá de la cantidad de vehículos necesarios para transportar dicha carga.

* El sistema deberá terminar la oferta una vez el despachador haya asignado la totalidad de vehículos requeridos para la solicitud de carga.

![alt text][asignar_turno]

[asignar_turno]: ./Asignacion_turnos.png "Asignar turno"

## 5. Cambio de estados

* El conductor podrá cambiar el estado de la solicitud de carga a **En transito** una vez se encuentra dentro de la zona de carga especificada en la solicitud de carga.

* El conductor podrá cambiar el estado de la solicitud de carga a **Entregado** una vez se encuentre dentro de la zona de descarga especificada en la solicitud de carga.

![alt text][cambio_estados]

[cambio_estados]: ./Cambio_estados.png "Cambio estados"


**TODO: Definir estados : Aceptado, Cargando, En Transito, Entregado ?**

## 6. Calificación de actores

* El conductor podrá calificar de forma cuantitativa y cualitativamente al generador de carga, empresa de transporte y vehículo.

* La empresa de transporte podrá calificar cuantitativa y cualitativamente al conductor y empresa de transporte.

* El generador de carga podrá calificar cuantitativa y cualitativamente, vehículo y empresa de transporte.

![alt text][calificacion]

[calificacion]: ./Calificacion.png "Calificacion"


**TODO: Revisar sintáxis requisitos funcionales**