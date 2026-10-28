# Sistema de registro de horas normales y extras
## Caso de estudio: Puma Lubricants

Trabajo Práctico Integrador y Progresivo de Organización Empresarial.
Tecnicatura Universitaria en Programación a Distancia — UTN.

## Integrante

- Gianluca Agustín Isgro.

## Descripción del proyecto

El proyecto propone una aplicación para digitalizar el registro y la
consulta de las horas normales y extras de los empleados de Puma
Lubricants, reemplazando las planillas de papel por información
centralizada.

El alcance inicial se concentra en Producción. Los operarios registran
sus jornadas y solicitan horas extras; Supervisión de Producción revisa
las solicitudes y Administración consulta los registros para realizar
sus controles.

Es una propuesta académica. Este repositorio documenta su análisis y
diseño; no representa una aplicación implementada en la empresa.

## Objetivo general

Desarrollar e implementar una aplicación que permita registrar y
consultar las horas trabajadas y las horas extras, mejorar el control
del proceso y facilitar el acceso a la información según el rol de
cada usuario.

## Funcionalidades previstas

- Registrar entrada, salida y pausas de cada jornada.
- Solicitar horas extras indicando duración y motivo.
- Aprobar o rechazar solicitudes mediante el responsable autorizado.
- Consultar jornadas y solicitudes según los permisos del usuario.
- Obtener informes de horas normales y extras aprobadas.

## Roles del sistema

- Operario: registra su jornada y solicita horas extras.
- Supervisión de Producción: revisa y resuelve las solicitudes.
- Administración: mantiene los datos del personal y consulta registros.
- Gerencia: consulta información consolidada para tomar decisiones.

## Modelo de datos

El diccionario de datos de la entrega 3 define tres entidades:

1. Empleado.
2. Registro de jornada.
3. Solicitud de horas extras.

Cada jornada pertenece a un empleado y puede tener como máximo una
solicitud de horas extras. Las solicitudes pueden estar pendientes,
aprobadas o rechazadas.

## Reglas principales

- La salida debe ser posterior a la entrada.
- No se permiten jornadas superpuestas para un mismo empleado.
- Una jornada abierta no integra los totales definitivos.
- Las solicitudes se presentan después de cerrar la jornada.
- Los minutos extras solicitados no pueden superar el tiempo
  trabajado menos los minutos normales.
- Solo el responsable autorizado puede resolver una solicitud.
- No se permite aprobar solicitudes propias.
- Una solicitud resuelta debe identificar al revisor y la fecha.
- El rechazo requiere una explicación.
- Solo las horas extras aprobadas integran el total autorizado.

## Metas e indicadores previstos

- Consultas habituales: tiempo máximo de 3 segundos en pruebas.
- Capacidad: al menos 10.000 registros sin pérdida de información.
- Validación: 100 % de los campos obligatorios antes de guardar,
  según la operación y el estado de la jornada.
- Primera versión y prueba piloto: plazo estimado de 8 semanas.

Estas son metas del proyecto; todavía no constituyen resultados
medidos ni pruebas superadas.

## Organización de las entregas

- Entrega 1: la organización y su enfoque sistémico.
- Entrega 2: diagnóstico FODA, objetivos y planificación con Gantt.
- Entrega 3: estructura formal y diccionario de datos.
- Entrega 4: BPMN, colaboración, backlog y mecanismos de control.

## Trabajo colaborativo y control de versiones

La documentación se prepara en ramas secundarias y se propone su
integración a main mediante Pull Requests.

Los commits deben describir claramente los cambios realizados.
La revisión de pares debe ser efectuada por otra persona y quedar
registrada en GitHub antes de la integración correspondiente.

El tablero de gestión se encuentra pendiente de creación. Se
organizará con los estados Por Hacer, En Progreso y Listo.

## Declaración de Uso de IA

Se utilizó ChatGPT como apoyo para analizar las consignas, organizar
la documentación y proponer redacciones y modelos del sistema.

Entre las instrucciones utilizadas estuvieron el análisis de los
materiales de las unidades y la continuidad de la entrega 4 sobre
las tres entregas anteriores. Estas instrucciones buscaron mantener
la coherencia entre el proceso, los responsables y los datos.

Durante la elaboración del organigrama, el estudiante corrigió la
propuesta inicial: indicó las gerencias reales, incorporó las
supervisiones de Producción y Mantenimiento y precisó las
dependencias de Limpieza y Laboratorio.

Estas correcciones muestran que la propuesta inicial de la IA
necesitó contrastarse con el conocimiento del caso. La IA no puede
confirmar por sí sola la estructura real de la empresa.

La asistencia de IA no sustituye la revisión humana ni la revisión
de pares del Pull Request. No se consideran realizadas pruebas,
revisiones o implementaciones sin evidencia.

El estudiante conserva la responsabilidad sobre la veracidad y
coherencia del trabajo.

## Referencias

- Material de las unidades 4 y 5 de Organización Empresarial, UTN.
- Guía Git y GitHub de la cátedra.
- Entregas 1, 2 y 3 del proyecto.
- Material y videos incluidos en el entorno virtual de la materia.
