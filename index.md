
# Instructivo - SupervisionesApp

## Preguntas frecuentes

### ¿Cuándo se ejecuta el flujo automático de notificaciones?
El sistema se ejecuta automáticamente los días 1, 20 y último de cada mes mediante un Timer de Power Automate.

### ¿Qué pasos debo seguir para cargar la información?
1. Abrir el archivo local `DG-M-P-109-F-001`.
2. Ir a la hoja `PROGRAMA ANUAL DE SUPERVISIÓN`.
3. Copiar la fila del funcionario con "X" en el mes correspondiente.
4. Abrir el sitio de SharePoint.
5. Seleccionar la carpeta de su regional.
6. Abrir el archivo `DatosLaboratorios.xlsx` y pegar en la hoja del laboratorio correspondiente.

### ¿Qué significa cada sigla?
- X: Programado
- CS: Cumple Satisfactorio
- RP: Reprogramado
- CN: Cumple No Satisfactorio

### ¿Dónde consulto los registros pendientes?
El sistema extrae automáticamente los registros marcados como RP o CN del mes anterior y los incluye en el correo de notificación.

---

## Flujo general de trabajo

1. El usuario carga datos en el archivo de su regional en SharePoint.
2. El flujo automático ejecuta scripts sobre cada archivo `DatosLaboratorios.xlsx`.
3. Se generan reportes HTML con datos actuales y pendientes.
4. Se envían notificaciones por correo y PowerApps.

---

## Instrucciones técnicas para administradores

- Los scripts de Excel extraen registros del mes actual y anterior.
- El flujo se basa en un Timer de Power Automate.
- Los datos se cargan en una lista de SharePoint automáticamente.
- Los correos contienen HTML con tablas dinámicas.

---

## Contacto

Para dudas o soporte, contactar a: nestor.hurtado@medicinalegal.gov.co
