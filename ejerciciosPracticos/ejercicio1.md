```mermaid
graph TD
    A([Inicio: Usuario entra al Formulario]) --> B[Ingresar Email y Contraseña]
    
    %% Validación 1: Formato Email
    B --> C{¿Email tiene formato válido?}
    C -- No --> D[Error: Email inválido]
    D --> E[Incrementar Contador de Reintentos +1]
    E --> F{¿Contador < 3?}
    F -- Sí --> B
    F -- No --> G([Fin: Cuenta Bloqueada por Seguridad])

    %% Validación 2: Contraseña
    C -- Sí --> H{¿Contraseña >= 8 caracteres?}
    H -- No --> I[Error: Contraseña muy corta]
    I --> E

    %% Validación 3: Servidor y Disponibilidad
    H -- Sí --> J[Enviar datos al Servidor]
    J --> K{¿Conexión Exitosa?}
    K -- No --> L[Error: Fallo de Red]
    L --> E

    K -- Sí --> M{¿Email ya está registrado?}
    M -- Sí --> N[Error: Email en uso]
    N --> E

    %% Flujo Exitoso
    M -- No --> O[Guardar Usuario en Base de Datos]
    O --> P[Enviar Correo de Confirmación]
    P --> Q([Fin: Registro Exitoso])