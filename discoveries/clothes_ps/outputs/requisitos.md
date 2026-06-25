# Requisitos Candidatos — clothes_ps

> Generado el 2026-06-22.
> Fuentes: cliente.md, vendedor.md, administrador.md.

---

## Funcionales

- **[R-01]** El sistema debe permitir buscar prendas filtrando por talla, diseno, categoria y precio.
  - Tipo: funcional
  - Origen: cliente.md (S., G.) · vendedor.md · Cliente Comprador, Vendedor

- **[R-02]** El sistema debe mostrar la disponibilidad de stock en tiempo real para cada combinacion de talla y diseno.
  - Tipo: funcional
  - Origen: vendedor.md · Vendedor

- **[R-03]** El sistema debe incluir informacion detallada de cada prenda: composicion del material, tipo de tela, comportamiento al lavado y colores disponibles.
  - Tipo: funcional
  - Origen: vendedor.md · cliente.md (G.) · Vendedor, Cliente Comprador

- **[R-04]** El sistema debe mostrar imagenes que representen fielmente la prenda real (color, forma, ajuste).
  - Tipo: funcional
  - Origen: cliente.md (G.) · Cliente Comprador

- **[R-05]** El sistema debe ofrecer canales de contacto con el vendedor (WhatsApp, Instagram) integrados en la navegacion del catalogo.
  - Tipo: funcional
  - Origen: cliente.md (F., S., G.) · Cliente Comprador

- **[R-06]** El sistema debe incluir un catalogo especifico de prendas plus size con disenos modernos, filtrable por talla real.
  - Tipo: funcional
  - Origen: cliente.md (F., S., G.) · administrador.md · Cliente Comprador, Administrador

- **[R-07]** El sistema debe permitir configurar y visualizar descuentos y promociones, respetando el punto de equilibrio del negocio.
  - Tipo: funcional
  - Origen: cliente.md (S., G.) · administrador.md · Cliente Comprador, Administrador

- **[R-08]** El sistema debe gestionar cambios y devoluciones segun las politicas de la tienda.
  - Tipo: funcional
  - Origen: vendedor.md · Vendedor

- **[R-09]** El sistema debe permitir al vendedor consultar disponibilidad de tallas y disenos de forma inmediata.
  - Tipo: funcional
  - Origen: vendedor.md · Vendedor

- **[R-10]** El sistema debe generar reportes periodicos de flujo de caja, rotacion de inventario y reposicion de productos.
  - Tipo: funcional
  - Origen: administrador.md · Administrador

- **[R-11]** El sistema debe registrar indicadores de satisfaccion del cliente para seguimiento del administrador.
  - Tipo: funcional
  - Origen: administrador.md · Administrador

- **[R-12]** El sistema debe permitir registrar y evaluar proveedores para apoyar su seleccion y seguimiento.
  - Tipo: funcional
  - Origen: administrador.md · Administrador

---

## No funcionales

- **[R-13]** La experiencia de busqueda debe ser intuitiva y accesible desde dispositivos moviles.
  - Tipo: no funcional
  - Origen: cliente.md (S.) · Cliente Comprador

- **[R-14]** Las consultas de disponibilidad de stock deben responderse en menos de 2 segundos.
  - Tipo: no funcional
  - Origen: vendedor.md · Vendedor

- **[R-15]** El sistema debe soportar tanto el canal de venta presencial como el canal en linea.
  - Tipo: no funcional
  - Origen: vendedor.md · cliente.md (S.) · Vendedor, Cliente Comprador
