
```mermaid
erDiagram
    USUARIO ||--o{ PEDIDO : realiza
    PEDIDO ||--|{ DETALLE_PEDIDO : contiene
    PRODUCTO ||--o{ DETALLE_PEDIDO : pertenece

    USUARIO {
        int id PK
        string nombre
        string email
        string password
    }

    PEDIDO {
        int id PK
        int usuario_id FK
        date fecha
        float total
    }

    PRODUCTO {
        int id PK
        string nombre
        float precio
        int stock
    }