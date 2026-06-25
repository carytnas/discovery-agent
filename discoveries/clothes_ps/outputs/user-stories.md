# User Stories — clothes_ps

Generado el 2026-06-22.
Nucleo de valor: permitir al cliente plus size encontrar prendas que le queden bien
con informacion fiel, y al vendedor cerrar ventas sin perder tiempo verificando stock.

---

## Historias del MVP

### [US-01] Buscar prendas por talla plus size

**Como** Cliente Comprador,
**quiero** filtrar el catalogo por talla (incluyendo tallas plus size como XL, 2XL y 3XL),
**para** ver unicamente las prendas disponibles en mi talla sin revisar el catalogo completo.

**Criterios de aceptacion:**
- Dado que estoy en el catalogo, cuando selecciono una talla, entonces solo se muestran prendas con stock en esa talla.
- Dado que selecciono una talla plus size, entonces el resultado incluye prendas con inventario mayor a cero en ese talle.
- Dado que no hay prendas en la talla seleccionada, entonces el sistema lo indica explicitamente en lugar de mostrar lista vacia sin mensaje.

**Fuente:** cliente.md (S., G.) - R-01, R-06

---

### [US-02] Ver informacion detallada de la prenda

**Como** Cliente Comprador,
**quiero** ver la ficha completa de cada prenda (medidas reales en cm, composicion del material, si encoge o se arruga, colores disponibles),
**para** tomar una decision de compra con confianza y sin sorpresas al recibirla.

**Criterios de aceptacion:**
- Dado que accedo al detalle de un producto, cuando lo veo en pantalla, entonces aparecen: medidas reales en centimetros, composicion del material (porcentaje fibra), comportamiento al lavado y colores disponibles.
- Dado que el vendedor completa la ficha, cuando ingresa las medidas reales, entonces el sistema las muestra al cliente tal como fueron ingresadas.

**Fuente:** vendedor.md, cliente.md (G.) - R-03

---

### [US-03] Ver imagenes fieles a la prenda real

**Como** Cliente Comprador,
**quiero** que las fotos del catalogo representen fielmente la prenda real (color real, forma de uso, ajuste en diferentes tallas),
**para** que lo que recibo coincida con lo que vi al elegirlo.

**Criterios de aceptacion:**
- Dado que veo un producto, cuando abro sus fotos, entonces hay al menos una imagen de la prenda en uso (con modelo o maniqui) ademas de la foto de estudio.
- Dado que hay variantes de color, cuando selecciono un color, entonces las imagenes cambian para mostrar la prenda en ese color especifico.

**Fuente:** cliente.md (G.) - R-04

---

### [US-04] Consultar disponibilidad de talla en tiempo real (vendedor)

**Como** Vendedor,
**quiero** consultar en el sistema si hay stock de un diseno en una talla especifica mientras atiendo a un cliente,
**para** dar una respuesta inmediata sin interrumpir la atencion ni hacer esperar al cliente.

**Criterios de aceptacion:**
- Dado que busco un diseno por nombre o codigo, cuando ingreso la talla, entonces el sistema muestra la disponibilidad en menos de 2 segundos.
- Dado que el producto no tiene stock en la talla solicitada, entonces el sistema lo indica claramente y muestra si hay stock en tallas adyacentes.

**Fuente:** vendedor.md - R-02, R-09, R-14

---

### [US-05] Ver alternativas cuando no hay stock en la talla deseada

**Como** Vendedor,
**quiero** que el sistema sugiera productos similares disponibles en la talla solicitada cuando el diseno pedido no tiene stock,
**para** no perder la venta y ofrecer al cliente una opcion equivalente de inmediato.

**Criterios de aceptacion:**
- Dado que consulto un producto sin stock en la talla pedida, entonces el sistema presenta al menos 2 alternativas similares (misma categoria) con stock en esa talla.
- Dado que el cliente rechaza las alternativas, entonces el sistema registra la talla y diseno no encontrado (para apoyar la reposicion del inventario).

**Fuente:** vendedor.md - R-01, R-02

---

### [US-06] Contactar al vendedor por WhatsApp o Instagram

**Como** Cliente Comprador,
**quiero** iniciar una conversacion con un vendedor desde la ficha del producto por WhatsApp o Instagram,
**para** resolver dudas de talla, material o disponibilidad antes de comprar sin necesidad de ir a la tienda.

**Criterios de aceptacion:**
- Dado que veo un producto, cuando hago clic en Consultar por WhatsApp, entonces se abre WhatsApp con un mensaje pre-cargado que incluye el nombre y codigo del producto.
- Dado que hago clic en Consultar por Instagram, entonces se abre el perfil de la tienda con el producto referenciado en el mensaje inicial.

**Fuente:** cliente.md (F., S., G.) - R-05

---

### [US-07] Ver descuentos y promociones en el catalogo

**Como** Cliente Comprador,
**quiero** ver las prendas con descuento claramente senaladas con su precio original y precio final,
**para** aprovechar las promociones y decidir que prendas comprar dentro de mi presupuesto.

**Criterios de aceptacion:**
- Dado que hay una promocion activa en una prenda, cuando la veo en el catalogo, entonces aparece el precio original tachado, el porcentaje de descuento y el precio final.
- Dado que una prenda esta en descuento, cuando el cliente la agrega al carrito, entonces el sistema aplica automaticamente el precio promocional.
- Dado que una prenda con descuento no admite devolucion, entonces el sistema muestra esta advertencia antes de que el cliente confirme la compra.

**Fuente:** cliente.md (S., G.), vendedor.md, administrador.md - R-07, R-08

---

### [US-08] Ver reporte basico de rotacion e inventario bajo (administrador)

**Como** Administrador,
**quiero** ver un reporte semanal de las prendas con menor stock y su velocidad de venta,
**para** decidir que reponer y cuando, antes de que el inventario se agote.

**Criterios de aceptacion:**
- Dado que accedo al panel de administracion, cuando selecciono el periodo (semana o mes), entonces veo las 10 prendas con menor stock disponible ordenadas de menor a mayor.
- Dado que una prenda llega al umbral minimo de inventario definido, entonces el sistema emite una alerta de reposicion al administrador.

**Fuente:** administrador.md - R-10

---

## Historias fuera del MVP (backlog)

| Historia | Motivo de exclusion |
|---|---|
| Gestion de proveedores | Dolor del administrador desacoplado del flujo de compra del cliente. |
| Seguimiento de satisfaccion | Requiere datos de uso previo del sistema para ser util. |
| Gestion avanzada de devoluciones | El proceso manual actual es funcional; no es el cuello de botella de valor. |
| Reportes de flujo de caja | Requiere integracion contable fuera del alcance del catalogo digital. |
