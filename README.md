## Informe Técnico del Taller

## Nombre del Taller
🛠️ Taller 1: Modelado de Proceso del Cliente con BPMN (Parte 1)

## 👥 Integrantes del equipo
## Katherin Juliana Moreno Carvajal
## David Esteban Díaz Vargas

## 🧠 Descripción general del trabajo
Modelar un proceso de negocio real del cliente utilizando la notación BPMN, identificando eventos, actividades, decisiones, actores involucrados y puntos críticos del flujo.

## 🔧  Proceso de desarrollo
Inicio
El paciente realiza las siguientes acciones
Seleccionar especialidad
Seleccionar modalidad 
Seleccionar fecha y rango horario 
El paciente debe realizar estas tres acciones antes de pasar a que el sistema verifique la disponibilidad de médico, ya que ésta va a variar según el tipo de modalidad que elija, siendo presencial o virtual. 
El sistema pasa a validar la disponibilidad de médicos y se las muestra al paciente, si no se cuenta con disponibilidad de médicos, el sistema manda un correo informándole al paciente que no hay disponibilidad.
En caso de que sí haya disponibilidad, el paciente selecciona al médico que desee y pasa a tomar la decisión de si quiere agendarla o no, si no la quiere agendar se cierra el sistema, si decide agendarla, el sistema pasa a agendar la cita y realiza la verificación de que realmente se haya agendado en el sistema; si se agendó correctamente, el sistema envía un correo diciendo que se confirma la cita; si no se agendó correctamente también recibe notificación de que no se fue exitoso 
Fin



## 📋 Tabla de actores, entidades o componentes (si aplica)

## Tabla de Elementos del Diagrama BPMN

| Nombre del elemento | Tipo | Descripción | Responsable |
|----------------------|------|-------------|-------------|
| Paciente | Actor | Usuario que desea agendar una cita médica. | Paciente |
| Sistema | Actor | Plataforma que consulta disponibilidad, registra la cita y envía la confirmación. | Sistema |
| Inicio | Evento de Inicio | Marca el comienzo del proceso de agendamiento de una cita. | Paciente |
| Seleccionar fecha y rango de horario | Actividad | El paciente selecciona la fecha y el horario en el que desea la cita. | Paciente |
| Seleccionar modalidad | Actividad | El paciente elige la modalidad de atención (presencial o virtual). | Paciente |
| Seleccionar especialidad | Actividad | El paciente selecciona la especialidad médica requerida. | Paciente |
| Consultar disponibilidad | Actividad | El sistema verifica la disponibilidad de citas según los criterios seleccionados. | Sistema |
| ¿Hay disponibilidad? | Gateway Exclusivo (XOR) | Evalúa si existen citas disponibles para continuar el proceso. | Sistema |
| Seleccionar médico | Actividad | El paciente selecciona el médico de su preferencia entre los disponibles. | Paciente |
| ¿Desea agendar alguna de las citas disponibles? | Gateway Exclusivo (XOR) | Determina si el paciente desea reservar alguna de las citas disponibles. | Paciente |
| Guardar la cita seleccionada en el sistema | Actividad | El sistema registra la cita elegida por el paciente. | Sistema |
| ¿Cita guardada correctamente en el sistema? | Gateway Exclusivo (XOR) | Verifica si el registro de la cita fue exitoso. | Sistema |
| Mandar notificación y confirmación | Actividad | El sistema envía la notificación y la confirmación de la cita al paciente. | Sistema |
| Recibir notificación | Actividad | El paciente recibe la confirmación de la cita agendada. | Paciente |
| Cita confirmada | Evento de Fin | Finaliza el proceso con la cita confirmada exitosamente. | Sistema |
| No hay disponibilidad | Evento Intermedio | Informa al paciente que no existen citas disponibles para los criterios seleccionados. | Sistema |
| Cierre del sistema | Evento de Fin | Finaliza el proceso cuando no es posible continuar con el agendamiento. | Sistema |
