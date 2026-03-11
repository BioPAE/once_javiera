# Informe Técnico: Arquitectura y Componentes de la Red

## I. Mecanismos de Operación en Internet

### Protocolos Fundamentales: TCP/IP
El funcionamiento de la red global se sustenta en el modelo **TCP/IP**, cuyas funciones se segmentan de la siguiente manera:

* **Protocolo de Internet (IP):** Actúa como el sistema de direccionamiento, asignando una **identidad numérica decimal** única a cada nodo o dispositivo conectado.
* **Protocolo de Control de Transmisión (TCP):** Su función principal es la **segmentación de datos** en unidades menores (paquetes) y su posterior ensamblaje y categorización según la naturaleza del tráfico (multimedia, texto o correo).

---

### Resolución de Nombres (DNS) y Automatización (DHCP)

A continuación se describen los sistemas de soporte para la navegación y conectividad:

 Sistema  Función Principal  Ventaja Operativa 

 **DNS**  Traductor de nombres de dominio.  Permite localizar servidores mediante alias legibles en lugar de secuencias de IP. 
 **DHCP** 
  Asignación dinámica de red.  Provee configuraciones IP automáticas, eliminando la necesidad de gestión manual por parte del usuario. 

> **Nota Técnica:** Gracias al DNS, el usuario puede invocar el dominio "Google" y el sistema resolverá internamente la dirección IP correspondiente sin intervención manual.

---

## II. El Protocolo HTTP y la Navegación Web

### Anatomía de una URL (Localizador Uniforme de Recursos)
Para identificar un recurso en la web, se utiliza una estructura jerárquica:

1.  **Esquema:** `https` (Indica una transferencia de hipertexto bajo cifrado de seguridad).
2.  **Dominio:** `www.ejemplo.com` (Identificador nominal del servidor de destino).
3.  **Ruta:** `/productos` (Ubicación lógica del archivo o sección dentro del servidor).

---

### Interacción entre Cliente y Servidor (Métodos HTTP)

La comunicación se rige principalmente por dos verbos de acción:

* **Método GET:** Se emplea estrictamente para la **recuperación de información**. Los parámetros suelen ser visibles en la barra de direcciones del navegador.
* **Método POST:** Se utiliza para el **envío de datos sensibles** (formularios, archivos, credenciales). La información se transmite de forma encapsulada en el cuerpo de la petición, ofreciendo una capa superior de privacidad.

---

### Diagnóstico de Respuesta del Servidor

 Código  Estado  Interpretación 
 `200`  **Éxito**  La solicitud ha sido procesada y el recurso se despliega correctamente. 
 `301`  **Redirección**  El recurso solicitado ha sido trasladado de forma permanente a un nuevo origen. 
 `404`  **Error de Cliente**  La conexión fue exitosa, pero la ruta o archivo específico no existe. 
 `500`  **Error de Servidor**  El servidor encontró una condición inesperada que le impidió completar la orden. 

---

### Documentación Adicional
Para una comprensión visual de estos conceptos, puede consultar el siguiente material: [Video Explicativo](https://www.youtube.com/watch?v=yYst7puZXjw)

**Autores del Proyecto:**

* Tomas Agudelo.