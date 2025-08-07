
# Instructivo de uso - Plataforma de Supervisiones Automatizadas

## ✨ Objetivo general

Facilitar y automatizar el proceso de supervisión de funcionarios de los laboratorios - organismos de inspección mediante la integración de Excel, SharePoint, Power Automate y Power Apps.

---

## 📄 1. Guía para usuarios

### ✍️ Paso 1. Actualizar archivo de programa anual

- Abrir el archivo local:
  - `DG-M-P-109-F-001 PROGRAMA ANUAL SUPERVISIÓN PERSONAL LABORATORIOS`
- Ir a la pestaña `PROGRAMA ANUAL DE SUPERVISIÓN`
- Copiar la fila completa del funcionario que ha sido programado para supervisión (tiene "X" en el mes correspondiente).

### 📁 Paso 2. Cargar información en SharePoint

- Ingresar al **sitio de documentos de SharePoint**.
- Seleccionar la carpeta correspondiente a su **regional** (hay 9 en total).
- Abrir el archivo `DatosLaboratorios.xlsx`.
- Ir a la hoja del **laboratorio correspondiente**.
- Pegar la fila del funcionario supervisado.

**❌ No editar otras hojas ni modificar encabezados.**

---

## 🛠️ 2. Guía técnica de administración

### ⏰ Flujo automático en Power Automate

- **Disparador**: Timer programado para los días **1, 20 y último de cada mes**.
- **Acciones principales**:
  1. Ejecutar scripts de Excel Online sobre cada archivo `DatosLaboratorios.xlsx` en SharePoint.
  2. Extraer:
     - Registros del **mes actual** ("X")
     - Pendientes del **mes anterior** ("RP", "CN")
  3. Insertar datos extraídos en una **lista de SharePoint**.
  4. Enviar notificaciones:
     - Correo electrónico HTML con tabla y total
     - Notificación Push mediante Power Apps

### 🔮 Scripts de Excel

- Cada hoja del archivo `DatosLaboratorios.xlsx` tiene una tabla nombrada igual que la hoja.
- Los scripts:
  - Filtran por mes actual y anterior según las siglas.
  - Devuelven los datos con el nombre del laboratorio.

---

## 🚀 3. Flujo de trabajo visual

1. Usuario carga datos programados en SharePoint.
2. Timer (Power Automate) ejecuta scripts.
3. Datos se filtran por mes y tipo.
4. Se crean notificaciones y registros.
5. Usuarios reciben avisos y revisan estado.

---

## ❓ 4. Preguntas frecuentes (FAQ)

**✅ ¿Cada cuánto se ejecuta el sistema?**  
El sistema se ejecuta automáticamente los días 1, 20 y último de cada mes.

**✅ ¿Dónde debo pegar los datos en el archivo de SharePoint?**  
En la hoja correspondiente al laboratorio, dentro del archivo `DatosLaboratorios.xlsx` de tu regional.

**✅ ¿Qué pasa si olvido cargar un funcionario?**  
El sistema lo omitirá hasta que se cargue correctamente en la tabla.

**✅ ¿Cómo identifico si un funcionario está pendiente?**  
Los estados "RP" y "CN" en el mes anterior son detectados automáticamente y notificados.

---

## 📸 5. Capturas sugeridas

- Vista del archivo DG-M-P-109-F-001 con los "X" marcados.
- Acceso a SharePoint con carpetas por regional.
- Vista del archivo `DatosLaboratorios.xlsx` con pestañas por laboratorio.
- Flujo de Power Automate (pantalla con la condición del día).
- Ejemplo de correo HTML con la tabla generada.

---

✉️ Para soporte o dudas, contacta con el administrador de la herramienta o consulta el agente Copilot dentro del sitio de SharePoint.

nestor.hurtado@medicinalegal.gov.co
