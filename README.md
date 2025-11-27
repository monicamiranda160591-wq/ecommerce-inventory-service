# 📦 ecommerce-inventory-service

- El Inventory Service administra el stock de productos del sistema de e-commerce.
- Se encarga de verificar disponibilidad, actualizar existencias y responder a eventos provenientes del Order Service a través de Apache Kafka.

## Funciones principales

- Registrar stock inicial de productos

- Consultar disponibilidad por productId

- Descontar stock cuando se crea una orden

- Publicar eventos a Kafka:

    - ecommerce.orders.confirmed (hay stock suficiente)

    - ecommerce.orders.cancelled (no hay stock)

Responsabilidad dentro de la arquitectura

Es el servicio que valida si un pedido puede completarse o debe cancelarse, asegurando la integridad del inventario en el ecosistema de microservicios.
