---
name: password-recovery-ui
description: Estándares y reglas para el diseño de la interfaz de recuperación de contraseña de CertiTalent.
---

# Skill: password-recovery-ui

Este skill define las reglas y estándares para la generación de la interfaz de recuperación de contraseña de la plataforma CertiTalent, asegurando la consistencia de marca y un flujo de UX profesional.

## Propósito
Garantizar que toda interfaz de recuperación de contraseña generada para CertiTalent siga estrictamente el sistema de diseño, las reglas de branding y el flujo de UX establecido.

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
  - Éxito: `#047857` (Green)
- **Logotipo**: Usar siempre el archivo `Logo Horizontal` de la carpeta `/Logotipos`.
  - Posición: Superior central.
  - No alterar colores ni proporciones.
- **Tipografía**: Montserrat (700) para títulos, Nunito (400, 600, 700) para cuerpo.

## Idioma
- La interfaz debe ser **100% en español**.

## Estructura de la Interfaz (Orden descendente)
1. **Logo Horizontal**
2. **Título**: "Recuperar contraseña"
3. **Subtítulo**: "Ingresa tu correo electrónico y te enviaremos un enlace para restablecer tu contraseña."
4. **Formulario**:
   - Email: Label "Correo electrónico", placeholder "tu@correo.com".
5. **Acción Principal**: Botón "Enviar enlace de recuperación" (con estados hover/active/disabled).
6. **Acción Secundaria**: Enlace "Volver al inicio de sesión" (redirige a `index.html`).

## Estados de UX
- **Default**: Estado inicial del formulario.
- **Loading**: Mostrar spinner y deshabilitar botón durante el proceso.
- **Success**: Mostrar mensaje "Te enviamos un enlace de recuperación. Revisa tu correo electrónico." (Fondo verde `#ECFDF5`).
- **Error**: Mostrar mensaje "No encontramos una cuenta asociada a este correo." (Fondo rojo `#FEF2F2`).

## Diseño y Layout
- Interfaz administrativa limpia y centrada.
- Espaciado consistente (margin/padding).
- Diseño moderno siguiendo el manual de marca CertiTalent.
