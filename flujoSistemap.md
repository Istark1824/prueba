```mermaid
graph TD
    Home[Inicio / Landing] --> Login[Login / Registro]
    Home --> Catalog[Catálogo de Productos]
    
    Catalog --> ProductDetail[Detalle del Producto]
    ProductDetail --> Cart[Carrito de Compras]
    
    Cart --> Checkout[Pasarela de Pago]
    Checkout --> Confirmation[Confirmación de Compra]
    
    Login --> Dashboard[Panel de Usuario]
    Dashboard --> Profile[Mi Perfil]
    Dashboard --> Orders[Mis Pedidos]