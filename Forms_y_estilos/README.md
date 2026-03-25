# 📋 Documentación del Formulario de Contacto

---

## 🏗️ Estructura Semántica (HTML5)

Se ha utilizado una estructura limpia y moderna priorizando la accesibilidad y el SEO:

* **`<main class="contenedor">`**: Define el área de contenido principal de la página.
* **`<header>`**: Contiene el título principal (`h1`) y una bajada de texto con la promesa de respuesta (UX Writing).
* **`<form>`**: Configurado con `novalidate` para permitir que las validaciones personalizadas de JavaScript (si se agregan luego) tomen el control, aunque mantiene atributos de validación nativa.

---

## 🛠️ Componentes y Atributos Clave

### 1. Validación Nativa del Navegador
El formulario utiliza atributos de HTML5 para asegurar la calidad de los datos antes del envío:
* `required`: Obliga a rellenar campos críticos.
* `minlength` / `maxlength`: Controla la extensión de nombres y mensajes.
* `pattern`: Se utilizó una expresión regular en el campo de teléfono para validar formatos internacionales básicos.

### 2. Organización de Datos
* **`optgroup`**: Se implementó en el `<select>` para agrupar los motivos de consulta (Soporte, Información, Otros), facilitando la lectura al usuario.
* **`radio buttons`**: Permiten seleccionar una única opción de contacto preferida.
* **`checkbox`**: Separación clara entre la aceptación obligatoria de términos y la suscripción opcional al newsletter.

### 3. Accesibilidad (A11y)
* **Relación Label-Input**: Todos los campos cuentan con un `id` único vinculado a su respectivo `<label>` mediante el atributo `for`.
* **Autocomplete**: Uso de `autocomplete="name"` y `autocomplete="email"` para ayudar a los navegadores a autocompletar la información del usuario.

---

## 🎨 Clases CSS Preparadas (Hooks)

El código HTML incluye ganchos (clases) listos para ser estilizados en `estilo.css`:

| Clase | Propósito |
| :--- | :--- |
| `.fila-doble` | Contenedor Flexbox/Grid para mostrar dos inputs en una sola línea. |
| `.campo` | Espaciado vertical y estructura de cada unidad de entrada. |
| `.ayuda` | Estilo para los textos pequeños de guía debajo de los inputs. |
| `.btn-primario` | Estilo destacado para el botón de envío. |
| `.campo-check` | Alineación especial para inputs tipo checkbox y sus etiquetas. I

---

## 💡 Lógica Condicional (Pendiente)

El campo `#campo-telefono` está preparado con un `id` específico. La intención técnica es aplicar **JavaScript** para que este campo permanezca oculto (`display: none`) por defecto y solo se muestre cuando el usuario seleccione las opciones de **WhatsApp** o **Llamada**.
