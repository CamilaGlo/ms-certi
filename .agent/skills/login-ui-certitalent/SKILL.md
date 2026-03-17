---
name: login-ui-certitalent
description: Estándares y reglas para el diseño de interfaces de login de CertiTalent.
---

# Skill: login-ui-certitalent

Este skill define las reglas y estándares para la generación de interfaces de login de la plataforma CertiTalent, asegurando la consistencia de marca, usabilidad y cumplimiento del Design System oficial.

## Propósito
Garantizar que cada interfaz de inicio de sesión generada para CertiTalent siga estrictamente el sistema de diseño, las reglas de branding y la estructura de UX establecida.

## Reglas de Branding
- **Colores Oficiales**:
  - Primario: `#F6944B` (Orange)
  - Primario Hover: `#F46C22`
  - Primario Active: `#D95D1A`
  - Primario Disabled: `#FAD4B7`
  - Secundario: `#2A3662` (Navy Blue)
  - Fondo Página: `#FFF4E5` (Light Peach)
  - Fondo Tarjeta: `#FDFDFD` (Off-white)
  - Bordes: `#E5ECF8`
- **Logotipo**: Usar siempre el archivo `Logo Horizontal` de la carpeta `/Logotipos`.
  - Posición: Superior central.
  - No alterar colores ni proporciones.
- **Tipografía**: Montserrat (700) para títulos, Nunito (400, 600, 700) para cuerpo.

## Idioma
- La interfaz debe estar **100% en español**.

## Estructura de UX (Orden descendente)
1. **Logo Horizontal**
2. **Título**: "Iniciar sesión"
3. **Subtítulo**: "Bienvenido de nuevo. Ingresa tus credenciales para continuar."
4. **Formulario**:
   - Email: Label "Correo electrónico", placeholder "tu@correo.com".
   - Password: Label "Contraseña", placeholder "Tu contraseña", link "¿Olvidaste tu contraseña?".
   - Checkbox: "Recordarme".
5. **Botón Primario**: "Iniciar sesión" (con estados hover/active/disabled).
6. **Separador**: "o accede con".
7. **Acceso Social**: Botones para Google y Microsoft (iconos a la izquierda, estilo secundario).

## Recomendaciones Técnicas
- Usar variables CSS para los colores corporativos.
- Implementar transiciones suaves (0.2s) para estados interactivos.
- Asegurar que el logo sea SVG para máxima nitidez.
- Mantener un ancho máximo de contenedor de ~480px para desktop.
