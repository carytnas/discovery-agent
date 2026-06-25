# Hipotesis y Experimentos — clothes_ps

Generado el 2026-06-22. Fuentes: mvp-canvas.md, evidence-map.json.
Ordenadas de mayor a menor riesgo (impacto x incertidumbre).

---

## [H-01] Adopcion del canal digital por clientes plus size — riesgo: alto

- **Supuesto a probar:** Los clientes plus size usaran un catalogo digital estructurado (con filtro por talla) en lugar de enviar mensajes directos al vendedor.
- **Hipotesis:** Creemos que los clientes plus size consultaran el catalogo de forma autonoma si ofrecemos acceso estructurado por talla desde WhatsApp o Instagram, porque S. y G. (cliente.md) ya usan esos canales y expresaron querer una busqueda intuitiva sin acercarse a la tienda.
- **Senal medible:** Porcentaje de clientes alcanzados que navegan el catalogo de forma autonoma (sin enviar mensaje directo al vendedor) sobre el total al que se compartio el acceso.
- **Criterio de exito:** Mayor o igual al 40% de los clientes alcanzados consultan el catalogo de forma autonoma durante las 2 semanas del piloto.
- **Experimento:** Mago de Oz — compartir un catalogo estatico (PDF o WhatsApp Business catalog) con 15-20 clientes habituales por WhatsApp; registrar cuantos navegan solos vs cuantos envian mensaje directo preguntando por tallas.
- **Caja de tiempo y costo:** 1 semana de preparacion mas 2 semanas de piloto. Costo: 0 (herramientas existentes). Inversion maxima: 3 horas de armado del catalogo estatico.
- **Regla de decision:**
  - Si pasa (mayor o igual al 40% autonomos): proceder con el desarrollo del catalogo digital con filtro de talla.
  - Si falla (menos del 40%): pivotar a asistente de ventas conversacional por WhatsApp; el catalogo web independiente es la funcionalidad equivocada para este segmento.

---

## [H-02] Informacion fiel de medidas y fotos reduce la friccion de compra — riesgo: alto

- **Supuesto a probar:** Mostrar medidas reales en cm y fotos fieles en el catalogo reducira las devoluciones y cambios por talla incorrecta.
- **Hipotesis:** Creemos que los clientes compraran con mayor seguridad y habra menos devoluciones si cada prenda incluye medidas reales en cm y una foto en uso real, porque G. (cliente.md) declaro que su mayor frustracion es que las tallas no coincidan con las medidas reales y que la ropa se vea diferente a las fotos.
- **Senal medible:** Tasa de devoluciones o cambios por motivo talla incorrecta sobre el total de ventas, comparada entre compras con ficha detallada y compras sin ficha del periodo anterior.
- **Criterio de exito:** Reduccion mayor o igual al 30% en la tasa de devoluciones por talla en compras con ficha vs el periodo sin ficha, medida en 4 semanas.
- **Experimento:** Concierge — seleccionar 10 prendas plus size, crear fichas manuales con medidas reales en cm y fotos en uso; enviarlas por WhatsApp a clientes habituales antes de confirmar la compra; registrar devoluciones vs compras sin ficha del mismo periodo.
- **Caja de tiempo y costo:** 3 dias de preparacion (fotografia y medicion) mas 4 semanas de seguimiento. Costo: tiempo del vendedor.
- **Regla de decision:**
  - Si pasa (mayor o igual al 30% de reduccion): invertir en fotografia y medicion de todo el catalogo plus size antes del desarrollo.
  - Si falla (menos del 30% de reduccion): el cuello de botella esta en la inconsistencia del proveedor, no en la informacion del catalogo; priorizar revision de proveedores (R-12) antes de construir.

---

## [H-03] El inventario plus size actual es suficiente para lanzar el catalogo — riesgo: medio

- **Supuesto a probar:** El inventario plus size actual tiene suficiente variedad y stock para que el catalogo muestre opciones reales y no mayoritariamente sin stock.
- **Hipotesis:** Creemos que el catalogo puede mostrar al menos 10 prendas con stock en tallas 2XL o superiores si hacemos un levantamiento del inventario, porque el administrador (administrador.md) indica que la ropa ligera y deportiva mantiene ventas altas todo el ano.
- **Senal medible:** Numero de SKUs distintos en tallas plus size (2XL o superior) con stock mayor a cero en el inventario actual.
- **Criterio de exito:** 10 o mas SKUs distintos con stock mayor a cero en tallas plus size (2XL o superior), verificado en el levantamiento previo al desarrollo.
- **Experimento:** Auditoria de inventario — revisar el sistema actual y contar SKUs en tallas XL, 2XL y 3XL con stock mayor a cero por categoria (deportiva, casual, ligera). Caja de tiempo: 1 dia. Costo: 0.
- **Regla de decision:**
  - Si pasa (10 o mas SKUs disponibles): proceder con el catalogo usando el inventario actual.
  - Si falla (menos de 10 SKUs): ampliar el portafolio plus size con proveedores antes del desarrollo; lanzar con inventario insuficiente genera expectativas que el negocio no puede cumplir.

---

## Orden de ejecucion recomendado

Empieza por H-03 (1 dia, costo 0): si el inventario es insuficiente, los demas experimentos no tienen base todavia. Luego H-01 y H-02 en paralelo.

| Prioridad | Hipotesis | Tipo | Duracion | Costo |
|---|---|---|---|---|
| 0 (antes de todo) | H-03 inventario | Auditoria | 1 dia | 0 |
| 1 | H-01 adopcion digital | Mago de Oz | 3 semanas | 0 |
| 1 | H-02 info fiel reduce devoluciones | Concierge | 5 semanas | Tiempo vendedor |
