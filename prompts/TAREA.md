# Tarea: Mi prompt profesional

## Funcionalidad elegida

Elegí crear una funcionalidad para registrar productos de una tienda utilizando Java Swing.


## Version 1: Prompt basico

```text
Haz un programa para registrar productos.
```

### ¿Qué cambié?
En esta primera versión solamente indiqué de manera general lo que quería hacer.

### ¿Por qué?
Quería observar qué información podía faltar cuando el prompt es demasiado general.

### ¿Qué mejoró en la respuesta?
La IA creó un programa en Java para consola, pero tuvo que asumir la tecnología y la forma de registrar los productos.

## Version 2: Prompt mejorado

```text
Actua como desarrollador Java. Crea un programa para registrar productos de una tienda utilizando Java Swing. Cada producto debe tener codigo, nombre, precio y stock.
```

### ¿Qué cambié?
Agregué el rol de desarrollador Java, la tecnología Java Swing, el contexto de una tienda y los datos que debe tener cada producto.

### ¿Por qué?
Quería darle más información a la IA para que la respuesta estuviera más relacionada con lo que necesitaba.

### ¿Qué mejoró en la respuesta?
La respuesta pasó de un programa de consola a una aplicación con Java Swing. También incluyó una clase Producto y los atributos codigo, nombre, precio y stock.

## Version 3: Prompt final

```text
Actua como desarrollador Java. Crea una aplicacion de escritorio en Java Swing para registrar productos de una tienda.

El sistema debe permitir ingresar codigo, nombre, precio y stock de cada producto. Valida que el codigo y nombre no esten vacios, que el precio sea mayor que 0 y que el stock sea mayor o igual a 0.

Usa una clase Producto para representar los datos y otra clase para la ventana principal. No uses librerias externas.

Primero explica brevemente el funcionamiento. Luego presenta el codigo organizado por clases y finalmente indica un ejemplo de como probar el registro de un producto.
```

### ¿Qué cambié?
Agregué validaciones para los datos, organicé el programa en dos clases, incluí una restricción y especifiqué el formato de la respuesta.

### ¿Por qué?
Quería que la IA tuviera instrucciones más claras y que el programa tuviera validaciones para evitar datos incorrectos.

### ¿Qué mejoró en la respuesta?
La respuesta final incluyó las validaciones solicitadas, separó el código en las clases Producto y VentanaPrincipal, explicó el funcionamiento y mostró un ejemplo para probar el programa.


## Componentes del prompt final

| Componente | Texto del prompt final |
|------------|-------------------------|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea una aplicacion de escritorio en Java Swing para registrar productos de una tienda. |
| Contexto | El sistema es para registrar productos de una tienda. |
| Ejemplo | Indica un ejemplo de como probar el registro de un producto. |
| Formato | Primero explica brevemente el funcionamiento, luego presenta el codigo organizado por clases y finalmente indica un ejemplo de prueba. |

## Restricción utilizada
No uses librerias externas.

## Evaluación del resultado

| Criterio | Sí / No |
|----------|---------|
| Utiliza Java Swing | Sí |
| Permite registrar productos | Sí |
| Utiliza una clase Producto | Sí |
| Valida los datos ingresados | Sí |
| Incluye una clase para la ventana principal | Sí |


## Errores que evité

### 1. Ser demasiado general

En la primera versión el pedido era muy general. Lo evité indicando la tecnología, el contexto, los atributos y las validaciones que necesitaba.

### 2. No indicar el formato

También evité este error indicando cómo quería recibir la respuesta: primero una explicación, después el código organizado por clases y finalmente un ejemplo de prueba.

---