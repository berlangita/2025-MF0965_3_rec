# MF0965_3_rec

- **Duración:** 3 horas
- **Lenguaje de desarrollo:** Python 3.x
- **Puntuación total:** 10 puntos

---

## Parte I Teoría - Test (2 ptos)

1. ¿Qué principio busca maximizar la reutilización en el desarrollo de componentes?

    - a) Acoplamiento fuerte
    - b) Cohesión
    - c) Inversión de control
    - d) Reutilización de código

2. En un modelo de comunicaciones síncronas entre componentes, ¿qué ocurre?

    - a) Emisor y receptor interactúan de forma independiente en el tiempo
    - b) El emisor bloquea su ejecución hasta recibir respuesta
    - c) Se usan únicamente colas de mensajes
    - d) No hay garantía de orden en la entrega

3. En el despliegue de un componente, ¿qué fichero describe normalmente sus dependencias y configuración?

    - a) `README.md`
    - b) `deployment.xml` (o `manifest.xml`)
    - c) `build.gradle`
    - d) `.gitignore`

4. ¿Qué tarea NO corresponde a la puesta en funcionamiento de un componente?

    - a) Configuración de parámetros de entorno
    - b) Creación de script de despliegue
    - c) Diseño de interfaces UML
    - d) Verificación de versiones

5. Señala la ventaja principal de los componentes orientados a servicios REST:

    - a) Estado mantenido en servidor
    - b) Acoplamiento fuerte
    - c) Uso de XML obligatoriamente
    - d) Ligereza y uso de HTTP nativo

6. Para controlar la calidad de un componente antes de su instalación, se realiza:

    - a) Pruebas unitarias y de integración
    - b) Documentación de usuario
    - c) Manual de despliegue
    - d) Creación de diagrama de despliegue

7. Un “container” (contenedor) en tecnologías de componentes proporciona, entre otras, la siguiente funcionalidad:

    - a) Compilar código fuente
    - b) Gestión de transacciones y seguridad
    - c) Control de versiones Git
    - d) Monitoreo de procesos del SO

8. ¿Qué módulo NO forma parte de la biblioteca estándar de Python?

    - a) `json`
    - b) `logging`
    - c) `requests`
    - d) `threading`

9. ¿Qué módulo de Python se utiliza para definir clases abstractas y métodos abstractos?

    - a) `typing`
    - b) `abc`
    - c) `interface`
    - d) `abstract`

10. ¿Cuál es el propósito del decorador `@property` en Python?

    - a) Definir un método estático
    - b) Crear getters y setters de forma implícita
    - c) Decorar funciones asíncronas
    - d) Documentar el código

## Parte II: Teoría - Desarollo (2 ptos)

Describe brecemente (máximo 3 lineas) cada uno de los principios **SOLID** y pon un ejemplo en código muy breve para ilustrar al menos dos de ellos.

- Responsabilidad Única
- Abierto/Cerrado
- Sustitución de Liskov
- Segregación de Interfaces
- Inversión de Dependencias

## Parte III: Ejercicios prácticos de programación

Repositorio: Antes de comenzar, forkea el repositorio original disponible en: https://github.com/elMestreAcademy/2025-MF0965_3_rec

Control de versiones: Realiza commits frecuentes a tu repositorio. Puedes hacer más commits de los sugeridos en los enunciados para reflejar el progreso de tu trabajo.

---

### **Ejercicio 3**: Gestión de inventario de una tienda (3 puntos)

Se necesita un programa en Python para gestionar el inventario de productos de una tienda. Se te proporciona un esqueleto de código que ya incluye la estructura de la clase `Producto`, las funciones y el menú principal.

Completa las porciones de código que faltan.

**Requisitos:**

1. **Clase `Producto`:**

    - Completa el constructor (`__init__`) para que asigne los parámetros a los atributos del objeto.
    - Completa el método `__str__` para que devuelva una cadena con el formato especificado en el docstring.

2. **Funciones:**

    - Completa la lógica de la función `buscar_producto` para que recorra la lista y encuentre el producto por su código.
    - Completa la función `mostrar_inventario` para que imprima todos los productos.
    - Implementa el cálculo en la función `calcular_valor_total`.

3. **Menú interactivo:**

    - Añade la lógica necesaria dentro del bucle `while` del `main` para manejar la búsqueda de productos y la impresión del resultado.

```python
class Producto:
    def __init__(self, codigo, nombre, precio):
        """
        COMPLETAR 1:
        Asigna los parámetros a los atributos
        """
        pass

    def __str__(self):
        """
        COMPLETAR 2:
        Devuelve un string con el formato especificado, usando f-string.
        Asegúrate de que el precio se muestre con 2 decimales.
        Ejemplo de formato: "[PROD001] Teclado Mecánico - Precio: 75.50 €
        """
        pass


def buscar_producto(inventario, codigo_buscar):
    """
    COMPLETAR 3:
    Busca en 'inventario' un producto cuyo código coincida con 'codigo_buscar'.
    Si lo encuentra, devuelve dicho objeto; si no, devuelve None.
    """
    pass


def mostrar_inventario(inventario):
    """
    COMPLETAR 4:
    Imprime por pantalla todos los productos que hay en 'inventario'.
    """
    print("\n--- INVENTARIO ACTUAL ---")
    if not inventario:
        print("El inventario está vacío.")
    else:
        pass


def calcular_valor_total(inventario):
    """
    COMPLETAR 5:
    Calcula y devuelve la suma de los precios de todos los productos en el inventario.
    """
    total = 0.0

    return total


def main():
    inventario = [
        Producto("PROD001", "Teclado Mecánico", 75.50),
        Producto("PROD002", "Mouse Inalámbrico", 25.00)
    ]

    while True:
        print("\n===============================")
        print("  MENÚ DE GESTIÓN DE INVENTARIO")
        print("===============================")
        print("1. Mostrar inventario")
        print("2. Buscar producto")
        print("3. Calcular valor total del inventario")
        print("4. Salir")
        opcion = input("Seleccione una opción (1-4): ")

        if opcion == '1':
            mostrar_inventario(inventario)
        elif opcion == '2':
            codigo_buscar = input("Ingrese el código del producto a buscar: ")
            producto_encontrado = buscar_producto(inventario, codigo_buscar)
            """
            COMPLETAR 6:
            Comprueba si 'producto_encontrado' es distinto de None.
            Si se encontró, imprime ">> Producto encontrado:" y luego el producto.
                     Si no, imprime ">> No se encontró ningún producto con ese código."
            """

        elif opcion == '3':
            valor_total = calcular_valor_total(inventario)
            print(f"\n>> El valor total del inventario es: {valor_total:.2f} €")
        elif opcion == '4':
            print("\nSaliendo del programa. ¡Hasta luego!")
            break
        else:
            print("Opción no válida. Por favor, elija entre 1 y 4.")


if __name__ == "__main__":
    main()
```

---

### **Ejercicio 4**: Tienda programación avanzada (2 puntos)

Sobre la misma tienda y la clase Producto, implementa:

1. Una clase abstracta `ItemInventario` con atributos comunes y un método abstracto `detalles()`.
2. Dos subclases concretas, `ProductoFisico` y `ProductoDigital`, que hereden de `ItemInventario`.
3. Añade `getters` y `setters` a los atributos `precio` y `nombre` con validaciones sencillas (precio >=0, nombre no vacío).
4. Usa herencia múltiple creando una clase `ProductoEspecial` que herede de `ProductoFisico` y de una nueva interfaz abstracta `Promocionable` con un método `aplicar_descuento(porcentaje)`.
5. Demuestra en un pequeño bloque de código cómo crear instancias de `ProductoEspecial`, establecer atributos con setters y llamar a `aplicar_descuento`.
