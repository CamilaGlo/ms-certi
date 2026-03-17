---
name: requests-list-certitalent
description: Genera la interfaz de "Mis solicitudes" siguiendo estrictamente el sistema de diseño de CertiTalent.
---

# requests-list-certitalent

Este skill asegura que la pantalla de **"Mis solicitudes"** se genere siempre utilizando el sistema de diseño de CertiTalent y componentes de UI consistentes con el resto de la plataforma.

## Fuente de Verdad Visual

La interfaz DEBE reutilizar el mismo lenguaje visual utilizado en:
- Administración de usuarios
- Mi perfil
- Configuración
- Login

Recursos de referencia obligatorios:
- Design System PDF
- `/Kit de diseño`
- `/Tipografías` (Montserrat para encabezados, Nunito para cuerpo)

**REGLA CRÍTICA:** No inventar colores ni tipografías. Usar únicamente los tokens establecidos en `style.css`.

## Objetivo
Permitir a los usuarios visualizar, filtrar y revisar el estado de sus solicitudes enviadas.

## Estructura de la Página

### Encabezado
- **Título:** "Mis solicitudes" (Clase: `.page-title`, Fuente: Montserrat 700)
- **Subtítulo:** "Consulta el estado de tus solicitudes y revisa su historial." (Clase: `.description`, Fuente: Nunito 400)

### Sección de Filtros
Incluir filtros utilizando los mismos estilos de input y select ya utilizados en CertiTalent.
1. **Búsqueda (Input):**
   - Label: "Número de solicitud"
   - Placeholder: "Buscar por número de solicitud"
2. **Tipo de solicitud (Select):**
   - Label: "Tipo de solicitud"
   - Opción default: "Elegir una opción"
3. **Estado (Select):**
   - Label: "Estado"
   - Opción default: "Elegir una opción"
4. **Botón secundario:**
   - Label: "Limpiar" (Clase: `.btn .btn-secondary`)

### Tabla de Solicitudes
Columnas obligatorias (Clase: `.user-table` o `<table>` estándar con estilos de `style.css`):
- N.° de solicitud
- Fecha de solicitud
- Tipo de solicitud
- Estado
- Acciones

**Estilo:** Utilizar el encabezado con fondo gris claro (`#F8FAFC`) y texto en Montserrat 12px negrita uppercase.

## Badges de Estado
Utilizar badges alineados con el sistema de diseño:
- **Pendiente de revisión:** `.badge .badge-warning` (Fondo naranja claro, texto naranja oscuro)
- **Aprobada:** `.badge .badge-active` (Fondo verde claro, texto verde oscuro)
- **Rechazada:** `.badge .badge-inactive` (Fondo rojo claro, texto rojo oscuro)
- **En proceso:** `.badge .badge-info` (Fondo azul claro, texto azul oscuro)

## Columna de Acciones
- **Botón:** "Ver detalle"
- **Estilo:** Icono (Font Awesome) dentro de un botón circular sutil (`.btn-icon`).

## Estados de la Interfaz
La pantalla debe soportar estos estados mediante la clase `.state-container`:
1. **Default:** Tabla con registros.
2. **Cargando:** Spinner central con texto descriptivo.
3. **Vacío:** Icono de carpeta abierta, título "Sin resultados" y mensaje: "No se encontraron solicitudes con los filtros seleccionados."
4. **Error:** Icono de advertencia, título de error y mensaje: "No fue posible cargar las solicitudes. Intenta nuevamente."

## Reglas de Diseño
- **Tipografía:** Montserrat (títulos/headers), Nunito (cuerpo/inputs).
- **Colores:** Primario (#F6944B), Secundario (#2A3662), Bordes (#E5ECF8).
- **Espaciado:** Mantener márgenes consistentes con el dashboard de administración.
- **Bordes:** Border-radius de 12px para tarjetas y 8-10px para inputs/botones.
