# Algoritmos de Ordenamiento Personalizados

Este repositorio contiene dos soluciones en Python para ordenar datos bajo condiciones especiales. A continuación se explica **qué hace** cada algoritmo y **cómo debes estructurar tus datos** para usarlos correctamente.

---

## 1. Ordenador de Cadenas Numéricas (`insertionSortCadenas`)

### ¿Para qué sirve?
Sirve para ordenar una lista de números que están guardados como texto (por ejemplo: `["10", "2", "11"]`). 

Si usas el ordenamiento por defecto de Python con textos, dirá que `"10"` va antes que `"2"` (porque empieza con `"1"`). Este algoritmo corrige eso y los ordena por su **valor numérico real** sin alterar el formato original de tu lista.

### ¿Cómo se usa?
Solo debes pasarle una lista sencilla de cadenas de texto numéricas.

* **Entrada que espera:** `["10", "2", "11", "1", "20"]`
* **Resultado que devuelve:** `['1', '2', '10', '11', '20']`

---

## 2. El Ordenador Estable con Filtro (`countSort`)

### ¿Para qué sirve?
Este algoritmo está diseñado para resolver el reto clásico *"The Full Counting Sort"*. Recibe una lista de parejas (un número y una palabra) y hace dos cosas a la vez:
1. **Oculta el pasado:** Agarra todos los elementos que están en la primera mitad de la lista y cambia su texto por un guion (`"-"`).
2. **Ordena sin desordenar:** Ordena los elementos de menor a mayor según su número. Si dos elementos tienen el mismo número, respeta estrictamente quién llegó primero (ordenamiento estable).

### ¿Cómo se usa?
Debes pasarle una lista donde cada elemento sea otra lista con el formato `["número", "palabra"]`. El resultado se imprimirá directamente en la consola en una sola línea.

* **Entrada que espera:**
    ```python
    [
        ["1", "hola"],   # Primera mitad -> Se convertirá en "-"
        ["0", "mundo"],  # Primera mitad -> Se convertirá en "-"
        ["1", "python"], # Primera mitad -> Se convertirá en "-"
        ["0", "bueno"],  # Segunda mitad -> Conserva su texto
        ["2", "adios"],  # Segunda mitad -> Conserva su texto
        ["1", "clase"]   # Segunda mitad -> Conserva su texto
    ]
    ```
* **Resultado que imprime en consola:**
    ```text
    - bueno - - clase adios
    ```

## 🛠️ Requisitos

* **Python 3.x** instalado.
* No requiere ninguna librería externa o adicional.
