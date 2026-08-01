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

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Ej: Paciente        | Actor | Usuario que agenda una cita médica | Cliente |
