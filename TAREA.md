# Tarea: Mi prompt avanzado

## Tarea elegida
**Diseño de la estructura de clases para un Sistema de Gestión de Notas Académicas en Java.**

---

## Version 1: prompt basico
```text
Crea las clases para un sistema de notas de alumnos.
```
* **Técnica agregada:** Ninguna .
* **Por qué:** Para evaluar la respuesta espontánea y directa de la IA ante una instrucción genérica.
* **Qué mejoró:** Nada, la IA entregó una respuesta demasiado genérica.

---

## Version 2
```text
Actúa como un Arquitecto de Software Backend Senior. Diseña las clases en Java para un sistema de gestión de notas académicas. Necesito que pienses paso a paso (Chain of Thought) en las entidades necesarias como Alumno, Curso, Profesor y Nota, definiendo sus atributos con tipos de datos correctos antes de mostrar el diseño final.
```
* **Técnicas agregadas:** *Role Prompting* y *Chain of Thought*.
* **Por qué:** El rol específico fuerza un vocabulario técnico correcto y la cadena de pensamiento ayuda a que la IA no olvide la lógica relacional entre las entidades.
* **Qué mejoró:** La estructura es mucho más madura y lógica. Sin embargo, los entregables se muestran mezclados con explicaciones innecesarias y texto plano difícil de leer.

---

## Version 3: prompt final
```text
<rol>
Actúa como un Arquitecto de Software Backend Senior especializado en sistemas de gestión escolar.
</rol>

<contexto>
Estamos modelando el módulo de calificaciones de una escuela. Un Alumno puede cursar varias Asignaturas, un Profesor dicta Asignaturas, y cada Asignatura tiene múltiples Evaluaciones con un porcentaje de peso sobre la nota final.
</contexto>

<tarea>
Analiza los requerimientos y modela la arquitectura de clases en Java. Piensa paso a paso tu diseño analizando las relaciones (uno a muchos, muchos a muchos) antes de escribir el formato final.
</tarea>

<ejemplo>
Clase: Usuario
- atributos: 
  * id: Long
  * nombre: String
- relaciones: Ninguna
</ejemplo>

<formato>
Devuelve la solución exclusivamente en formato de lista Markdown con subtítulos para cada clase, especificando sus atributos, tipo de dato y su relación arquitectónica. No agregues introducciones ni conclusiones.
</formato>
```
* **Técnicas agregadas:** **Prompt Estructurado**  y **Few-shot**.
* **Por qué:** Las etiquetas aíslan y dan un orden estricto a las instrucciones para que la IA no confunda el contexto con la tarea. El ejemplo asegura un formato uniforme y predecible.
* **Qué mejoró:** El resultado final es impecable, modular, va directo al grano y utiliza exactamente el formato solicitado sin "relleno" textual.

---

## Tecnicas usadas en el prompt final

| Parte del Prompt Final | Técnica Aplicada |
| :--- | :--- |
| `<rol>Actúa como un Arquitecto de Software...</rol>` | **Role Prompting** |
| `<tarea>Piensa paso a paso tu diseño analizando... </tarea>` | **Chain of Thought (CoT)** |
| `<rol>`, `<contexto>`, `<tarea>`, `<ejemplo>`, `<formato>` | **Prompt Estructurado** |
| `<ejemplo>Clase: Usuario - atributos... </ejemplo>` | **One-shot / Few-shot** |

---

## Evaluacion del resultado

| Qué revisar | Cumple (Sí / No) |
| :--- | :--- |
| ¿El prompt final combina al menos tres técnicas avanzadas? | **Sí** |
| ¿Se asignó un rol específico de ingeniería de software en lugar de "experto"? | **Sí** |
| ¿La respuesta de la IA respeta estrictamente el formato estructurado libre de introducciones? | **Sí** |
| ¿Se incluyeron los atributos y las relaciones lógicas del sistema de notas? | **Sí** |

---

## Por que elegi estas tecnicas
Elegí combinar **Role Prompting**, **Chain of Thought** y **Prompt Estructurado** porque el diseño de arquitectura de software requiere precisión conceptual y orden lógico. 
