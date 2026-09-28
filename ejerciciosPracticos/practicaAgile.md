# Práctica Ágil: Gestión de Proyecto Frontend (TiendaTech)

## 1. Historias de Usuario (User Stories)

### 📌 HU-01: Carrito de Compras Básico
* **Como:** Cliente de TiendaTech.
* **Quiero:** Agregar productos al carrito desde la lista principal.
* **Para:** Guardar los artículos que me interesan antes de pagar.
* **Prioridad (MoSCoW):** `MUST HAVE` (Imprescindible)

#### Criterios de Aceptación (Given / When / Then)
* **Escenario 1: Agregar producto con stock**
  * **Dado** que el usuario está en la lista de productos y hay stock disponible,
  * **Cuando** hace clic en el botón "Agregar al Carrito",
  * **Entonces** el contador del carrito en la barra superior debe incrementarse en +1 y mostrar una notificación de éxito.
* **Escenario 2: Intento de agregar sin stock**
  * **Dado** que un producto tiene stock igual a 0,
  * **Cuando** el usuario ve el producto,
  * **Entonces** el botón debe aparecer deshabilitado con el texto "Agotado".

---

## 2. Desglose Técnico de Tareas (Frontend)

Para completar la **HU-01**, se desglosan las siguientes tareas técnicas:

1. `[HTML/CSS]` Diseñar el botón "Agregar al Carrito" con sus estados (normal, hover, disabled).
2. `[JS]` Crear el array/objeto `carroCompras` para almacenar los productos seleccionados en memoria.
3. `[JS]` Implementar la función `agregarProducto(id)` con la lógica de verificación de stock.
4. `[DOM]` Actualizar dinámicamente el badge contador del ícono del carrito `🛒` en el Header.
5. `[QA]` Probar los escenarios de borde (stock cero, clics repetidos rápidos).

---

## 3. Tablero Kanban del Proyecto

```mermaid
kanban
  Todo
    [HU-02: Filtro por Categorías]
    [TK-05: Pruebas de borde en Carrito]
  In Progress
    [TK-03: Función agregarProducto en JS]
    [TK-01: Maquetación de Botón en CSS]
  Code Review
    [TK-02: Estructura del Array Carrito]
  Done
    [HU-01: Definición de Criterios de Aceptación]
    [Setup: Estructura de carpetas en Git]