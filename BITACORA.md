# Bitacora de tecnicas avanzadas 
Laboratorio 07: Tecnicas Avanzadas de Prompting. 
Herramienta de IA usada: (escribe aqui cual usaste) 
## Ejercicio 2: Zero-shot, one-shot y few-shot 
### Resultados
 
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 | Lista numerada con la etiqueta con una explicacion corta | No |
| One-shot | 5 | Lista numerada parecida al ejemplo, pero con detalles distintos en algunas lineas | No |
| Few-shot | 5 | Una linea por comentario con el formato "texto" -> Etiqueta, sin explicaciones | Si |

## Ejercicio 3: Chain of Thought 
### Comprobacion con la calculadora
| Paso | Calculo | Resultado |
|------|---------|-----------|
| 1. Precio con descuento | 120 x 0,75 | 90 |
| 2. Precio con IGV | 90 x 1,18 | 106,20 |
| 3. Total por 3 unidades | 106,20 x 3 | 318,60 |
 
### Resultados
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo | 318,60 | No | Si |
| Paso a paso | S/ 318,60 (con cada calculo detallado) | Si | Si |
## Ejercicio 4: Role prompting 
### Resultados
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | Basico, explicacion general | Un ejemplo corto sin codigo | A cualquier persona, sin un publico definido |
| B. Rol docente | Sencillo | Comparacion de la vida diaria ejemplos | A quien esta empezando a programar |
| C. Rol senior | Tecnico (tipo de dato, memoria, alcance) | Codigo en Java | A un programador que ya conoce lo basico |
## Ejercicio 5: Descomposicion 
- *Paso 1:* La IA me adjunto un archivo exel junto a la estructura y una pequeña descripcion de cada aprte
- *Paso 2:* Me entrego el diseno de las clases (por ejemplo Producto, Categoria, Proveedor e Inventario), cada una con sus atributos y tipos de dato.
- *Paso 3:* Escribio la clase Producto con sus atributos, un constructor y los metodos get y set, coherente con el diseno del paso 2.
- *Paso 4:* Propuso 3 mejoras concretas, como validar que el precio y el stock no sean negativos, usar un tipo mas preciso para el dinero y agregar el metodo toString. Y adjunto el codigo "Mejorado"
- *Comparacion:* El pedido de una sola vez me dio algo muy general y largo. Con los pasos pude revisar cada parte antes de seguir, y el resultado fue mas ordenado y coherente.
## Ejercicio 6: Prompt estructurado y autocritica
### Tabla de comparacion
| Que revisar | Cumple (Si / No) |
|-------------|------------------|
| ¿Tiene las 4 columnas pedidas? | Si |
| ¿Incluye el bloqueo despues de 3 intentos? | Si |
| ¿Incluye casos con campos vacios? | Si |
| ¿Indica que casos agrego en la autocritica? | Si |
| ¿Hay algun caso repetido o que no tenga sentido? | Si |