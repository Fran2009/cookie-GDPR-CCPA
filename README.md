# Módulo de Preferencias de Cookies

Este proyecto es un módulo para gestionar preferencias de cookies compatible con las normativas GDPR y CCPA. Ofrece un modal donde los usuarios pueden aceptar todas las cookies, guardar preferencias específicas o rechazarlas completamente.

## Características

- Modal centrado en pantalla
- Soporte para varios idiomas (Español, Inglés y Francés)
- Gestión de diferentes tipos de cookies: necesarias, funcionales, de rendimiento y publicitarias
- Totalmente personalizable
- Opción para aceptar todas las cookies o rechazarlas

## Instalación

1. Clona este repositorio:
```bash
git clone https://github.com/Fran2009/cookie-GDPR-CCPA.git
```

2. Incluye el archivo de estilo en tu HTML:
```bash
<link rel="stylesheet" href="ruta-al-archivo/cookie-modal.css">
```

3. Incluye el archivo JavaScript en tu HTML:
```bash
<script src="ruta-al-archivo/cookie-modal.js"></script>
```

## Uso

Para inicializar el módulo, simplemente llama a la función initCookieModal en tu JavaScript, pasando la configuración si fuera necesario.
Ejemplo de html básico

```bash
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Centro de Preferencias de Cookies</title>
    <link rel="stylesheet" href="cookie-modal.css">
</head>
<body>
    <a href="#" id="open-cookie-modal">Volver abrir preferencias de cookies</a>
    
    <div id="cookie-modal-container"></div>
    <script src="cookie-modal.js"></script>
</body>
</html>
```

## Opciones de Configuración

1. language: Idioma por defecto al mostrar el modal. Valores posibles: 'es', 'en', 'fr'.
```bash
<script>
    initCookieModal({
        language: 'es', // Idioma por defecto
    });
</script>
```

2. availableLanguages: Array de idiomas disponibles para cambiar en el modal.
```bash
<script>
    initCookieModal({
        availableLanguages: ['es', 'en', 'fr'], // Idiomas disponibles
    });
</script>
```
3. texts: Un objeto para configurar qué secciones de cookies se deben mostrar. Por ejemplo, si solo quieres mostrar las cookies estrictamente necesarias y las funcionales.
```bash
<script>
    initCookieModal({
        texts: {
            strictCookiesTitle: true, // Mostrar sección de cookies estrictamente necesarias
            functionalityCookiesTitle: true // Mostrar sección de cookies funcionales
        }
    });
</script>
```

## Personalización de Textos

Los textos pueden ser configurados dinámicamente pasando un objeto texts al inicializar el módulo. Los textos que no se configuren usarán los valores por defecto.
Ejemplo de personalización de textos

```bash
initCookieModal({
    texts: {
        functionalityCookiesTitle: true,
        advertisingCookiesTitle: true
    }
});
```

## Soporte para Idiomas

Este módulo permite cambiar entre idiomas mediante un selector en el modal. Los idiomas disponibles se pueden configurar en el array availableLanguages.
Funcionalidad Avanzada


## Contribuciones

Las contribuciones son bienvenidas. Si encuentras un error o quieres sugerir mejoras, abre un issue o envía un pull request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT.