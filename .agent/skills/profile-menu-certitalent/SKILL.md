---
name: profile-menu-certitalent
description: Estándares para el menú de perfil y navegación superior de CertiTalent.
---

# Menú de Perfil CertiTalent

Este skill asegura que toda interfaz de la plataforma CertiTalent incluya un icono de perfil funcional con un menú desplegable consistente.

## Propósito
Estandarizar la experiencia de navegación del perfil de usuario, asegurando que las opciones críticas (Perfil, Configuración, Logout) estén siempre disponibles y sigan el sistema de diseño.

## Reglas Obligatorias

### 1. Icono de Perfil (Header)
- **Ubicación**: Esquina superior derecha del encabezado.
- **Interactividad**: Debe ser clicable con una transición visual sutil al pasar el mouse.
- **Estilo**: Circular o isotipo de usuario, alineado con el sistema de diseño CertiTalent.

### 2. Comportamiento del Dropdown
Al hacer clic en el icono, debe aparecer un menú con las siguientes características:
- **Posición**: Justo debajo del icono del perfil.
- **Cierre**: Debe cerrarse automáticamente al hacer clic fuera del área del menú (Click Outside).
- **Animación**: Entrada suave (Fade In / Slide Down).

### 3. Opciones del Menú (Español)
Las opciones deben aparecer en este orden exacto:
1. **Mi perfil**
2. **Configuración**
3. --- (Separador visual) ---
4. **Cerrar sesión**

## Especificaciones de Diseño

### Colores (Design System)
- **Texto**: `--secondary` (#2A3662) para ítems principales.
- **Hover**: `--primary` (#F6944B) o cambio de fondo a `--bg-page` (#F8FAFC).
- **Separador**: `--border` (#E5ECF8).
- **Sombra**: Sombra suave para elevación administrativa.

### Tipografía y Espaciado
- **Fuente**: Nunito 600/700.
- **Padding**: 10px-16px por ítem para facilitar el clic.
- **Gaps**: Espaciado consistente de 8px-12px entre elementos e iconos.

## Estructura de Salida Sugerida

### HTML
```html
<div class="user-profile" id="profile-container">
    <i class="fa-solid fa-circle-user fa-xl"></i>
    <div class="profile-dropdown" id="profile-dropdown">
        <a href="#">Mi perfil</a>
        <a href="#">Configuración</a>
        <hr>
        <a href="#">Cerrar sesión</a>
    </div>
</div>
```

### JavaScript
```javascript
profileContainer.addEventListener('click', (e) => {
    e.stopPropagation();
    profileDropdown.classList.toggle('active');
});

document.addEventListener('click', (e) => {
    if (!profileContainer.contains(e.target)) {
        profileDropdown.classList.remove('active');
    }
});
```

## Notas Adicionales
- No inventar nuevos colores.
- Mantener siempre el texto en español.
- Asegurar que el z-index sea lo suficientemente alto para superponerse a otros componentes.
