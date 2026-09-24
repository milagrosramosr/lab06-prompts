# Bitacora de prompts
Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: Chat GPT

## Ejercicio 2: Tokens y ventana de contexto 
| Texto | Caracteres | Tokens | 
|-------|------------|--------| 
| Los estudiantes programan en Java. |36 |8 | 
| The students program in Java. |31 | 7| 
| desafortunadamente |51 |12|

### Observaciones

Observé que una palabra larga como "desafortunadamente" puede dividirse en varios tokens, también pude notar que la cantidad de tokens puede cambiar dependiendo del idioma y de cómo el modelo divide el texto.

En el mismo chat, la IA pudo responder que mi aplicación se llama TiendaTec y que utiliza Java Swing porque anteriormente le había dado esa información. En un chat nuevo no tenía ese contexto disponible.

---

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|----------------------------|
| 0           | 100.0%         | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5         | 65.3%          | BiblioTec, BiblioTec, BiblioTec, BiblioTec, LibroYa |
| 1           | 44.5%          | PrestaLibro, LibroYa, PrestaLibro, LectoGo, PrestaLibro |
| 1.8         | 32.2%          | LectoGo, BiblioTec, PrestaLibro, LectoGo, LibroYa |

### Observaciones

Al aumentar la temperatura, los nombres elegidos son más variados y BiblioTec deja de tener tanta probabilidad, el simulador no inventa nombres nuevos porque solamente puede elegir entre las opciones que fueron programadas previamente.

---

## Ejercicioo 4 Prompt vago vs estructurado
| Criterio | Prompt vago | Prompt estructurado | 
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |NO |SI | 
| Menciona a los usuarios principales |NO |SI | 
| Tiene exactamente 3 funcionalidades |NO |SI | 
| Esta en 3 parrafos |NO |SI | 
| Lo usaria en un informe real |NO |SI |

### Observación

El prompt vago deja más libertad a la IA y por eso la respuesta puede ser diferente o no tener todos los datos necesarios y el prompt estructurado indica exactamente qué información debe incluir y cómo debe presentarla.

---

## Ejercicio 5: Anatomia de un prompt 
| Componente | Texto de mi prompt | 
|------------|--------------------|
| Rol |Actua como desarrollador Java. Crea un programa en Java | 
| Instruccion |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de  una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock. | 
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de  una tienda. | 
| Ejemplo |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de  una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).| 
| Formato |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de  una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java.
 |

### Cambios observados por nivel

- Nivel 1: La IA recibió una instrucción muy general y podía crear cualquier tipo de programa.
- Nivel 2: Al agregar el rol de desarrollador Java, la respuesta se orientó hacia programación en Java.
- Nivel 3: Al agregar el contexto de una tienda, el programa se relacionó con la gestión de productos.
- Nivel 4: Al indicar los atributos de la clase Producto, la respuesta fue más específica.
- Nivel 5: Al indicar cómo presentar la respuesta, la IA explicó primero la estructura y después mostró el código.
- Ejemplo: Al indicar el estilo de los métodos, pude orientar la forma en que debía escribir los métodos de la clase.

## Ejercicio 6: Del prompt basico al profesional
| Qué revisar | Cumple (Sí / No) | 
|------------|--------------------|
| ¿Está escrito en Java y usa Swing? |  SI | 
| ¿Pide correo y contraseña? |SI | 
| ¿Explica el funcionamiento antes o después del código? |SI | 
| ¿El código está organizado en clases? |SI | 
| ¿Valida los datos que ingresa el usuario? |SI |

## Prompt final mejorado
```text 
Actua como desarrollador Java. Crea un ejemplo de login para una 
aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```

