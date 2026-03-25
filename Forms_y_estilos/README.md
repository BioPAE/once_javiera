### 1. Archivo HTML (`index.html`)
En este archivo, la clave es que los `input` de radio estén antes del campo de teléfono para que el CSS pueda detectarlos.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Contacto - Sin JS</title>
  <link rel="stylesheet" href="estilos.css">
</head>
<body>
  <main class="contenedor">
    <form class="formulario">
      <h2>Contáctanos</h2>
      
      <div class="campo">
        <label>Nombre completo</label>
        <input type="text" placeholder="Tu nombre" required>
      </div>

      <div class="campo">
        <p>¿Cómo prefieres que te contactemos?</p>
        <div class="opciones">
          <input type="radio" id="via-email" name="contacto" checked>
          <label for="via-email">Email</label>

          <input type="radio" id="via-whatsapp" name="contacto">
          <label for="via-whatsapp">WhatsApp</label>
        </div>
      </div>

      <div class="telefono-oculto">
        <label>Número de teléfono</label>
        <input type="tel" placeholder="300 123 4567">
      </div>

      <button type="submit">Enviar</button>
    </form>
  </main>
</body>
</html>
```

---

### 2. Archivo CSS (`estilos.css`)
Aquí usamos el selector `:has()` y `:checked`. Esta es la forma moderna de hacer "lógica" sin programar en Java/JavaScript.

```css
/* Estilos base */
body { font-family: Arial, sans-serif; background: #f4f4f4; padding: 20px; }
.contenedor { max-width: 400px; background: white; padding: 20px; border-radius: 8px; }

/* Ocultar el teléfono por defecto */
.telefono-oculto {
  display: none;
  margin-top: 15px;
}

/* LÓGICA: Si el radio de WhatsApp está marcado, muestra el div de teléfono */
body:has(#via-whatsapp:checked) .telefono-oculto {
  display: block;
  animation: aparecer 0.4s ease;
}

@keyframes aparecer {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}
```
