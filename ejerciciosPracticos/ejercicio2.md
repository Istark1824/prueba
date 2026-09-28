```mermaid
graph TD
    %% Nodos Principales
    Home[🏠 Inicio /] --> Products[📦 Productos /productes]
    Home --> Categories[🗂️ Categorías /categories]
    Home --> Cart[🛒 Cesta /cistella]
    Home --> Account[👤 Cuenta /compte]
    Home --> Contact[📞 Contacto /contacte]

    %% Subpáginas de Productos (Se añaden comillas dobles para evitar el error)
    Products --> ProductDetail["🔍 Detalle Producto /productes/:id"]

    %% Subpáginas de Categorías
    Categories --> Mobiles[📱 Móviles /categories/mobils]
    Categories --> Computers[💻 Computadoras /categories/ordinadors]
    Categories --> Accessories[🎧 Accesorios /categories/accessoris]

    %% Flujos de Compra
    Mobiles --> ProductDetail
    Computers --> ProductDetail
    Accessories --> ProductDetail
    ProductDetail --> Cart