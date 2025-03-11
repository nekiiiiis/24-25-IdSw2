# **📜 Análisis de Legibilidad y Calidad del Código**


---

## **📌 Proyectos Analizados**
1. [Reto 001 - Estructura de Dietas](https://github.com/nekiiiiis/23-24-eda2/tree/main/entregas/martinezNeco/Reto001)
2. [Reto 003 - Gestión de Documentos](https://github.com/nekiiiiis/23-24-eda2/tree/main/entregas/martinezNeco/Reto003)
3. [Reto 004 - Exploración de Laberintos](https://github.com/nekiiiiis/23-24-eda2/tree/main/entregas/martinezNeco/Reto004)

---

## **🔹 Errores de Legibilidad en Códigos**

### **Nombrado Incorrecto (ambigüedad o mezcla de inglés y español)**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Day.java](https://github.com/nekiiiiis/23-24-eda2/blob/main/entregas/martinezNeco/Reto001/src/Day.java#L3) | `Day` está en inglés mientras `Dieta` y otros elementos están en español. | Renombrar a `Dia` para mantener consistencia. | 3 |
| Reto 001 | [Intake.java](https://github.com/nekiiiiis/23-24-eda2/blob/main/entregas/martinezNeco/Reto001/src/Intake.java#L3) | `Intake` está en inglés mientras otros nombres están en español. | Renombrar a `Ingesta`. | 3 |
| Reto 003 | [Gestion.java](https://github.com/nekiiiiis/23-24-eda2/blob/main/entregas/martinezNeco/Reto003/src/Gestion.java#L3) | `Gestion` es genérico y poco descriptivo. | Cambiar a `GestorDocumentos`. | 3 |
| Reto 004 | [Laberinto.java](https://github.com/nekiiiiis/23-24-eda2/blob/main/entregas/martinezNeco/Reto004/src/Laberinto.java#L8) | `simbolos` es un nombre poco claro. | Cambiar a `mapaSimbolos`. | 8 |

---

## **🔹 Formato y Consistencia**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Diet.java](#) | Uso inconsistente de llaves en bloques `if/else`. | Agregar llaves en todos los bloques. | 40-60 |
| Reto 001 | [Day.java](#) | `Scanner` se usa repetitivamente en varios métodos. | Crear un método auxiliar para manejar entradas. | 20-80 |
| Reto 003 | [Gestion.java](#) | `Scanner` se usa en múltiples lugares sin cerrarse correctamente. | Usar `try-with-resources` para evitar fugas de memoria. | 10-30 |
| Reto 004 | [Laberinto.java](#) | Inconsistencia en la indentación de matrices. | Alinear correctamente el código. | 50-60 |

---

## **🔹 Problemas de Precisión**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Diet.java](#) | Eliminación de un `Day` por referencia en lugar de comparar nombres. | Corregir la lógica de comparación. | 75-90 |
| Reto 003 | [Gestion.java](#) | Entrada de usuario sin validación al seleccionar un `Tipo`. | Validar entrada para evitar `ArrayIndexOutOfBoundsException`. | 30-50 |
| Reto 004 | [Laberinto.java](#) | Coordenadas `x` e `y` impresas en orden incorrecto al marcar como visitado. | Invertir `x` e `y` en la impresión. | 85 |

---

## **🔹 Código Muerto**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Diet.java](#) | Métodos no utilizados como `deleteDiet()`. | Eliminar código innecesario. | 100-120 |
| Reto 003 | [Gestion.java](#) | Algunas opciones del `menu()` no están implementadas. | Completar funcionalidades o eliminarlas. | 50-60 |
| Reto 004 | [Laberinto.java](#) | Doble declaración de la clase `Laberinto.java`. | Eliminar código duplicado. | 120-180 |

---

## **🔹 Comentarios (Exceso o falta de comentarios)**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Day.java](#) | Falta documentación clara en `createDay()`. | Agregar comentarios explicativos. | 30-50 |
| Reto 003 | [Documento.java](#) | Comentarios poco descriptivos en métodos clave. | Explicar mejor la funcionalidad de cada método. | 10-30 |
| Reto 004 | [Laberinto.java](#) | Comentarios de depuración (`System.out.println`). | Eliminar comentarios de prueba. | 40-50 |

---

## **🔹 Incumplimiento del Principio DRY**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Diet.java](#) | Código repetido en adición y eliminación de días. | Extraer en un método reutilizable. | 40-60 |
| Reto 003 | [Gestion.java](#) | Código duplicado en `ingresarAutores()` y `ingresarPalabrasClave()`. | Unificar lógica en un solo método. | 30-50 |
| Reto 004 | [Laberinto.java](#) | Múltiples llamadas a `mostrarLaberinto()`. | Crear una función que controle la visualización. | 70-90 |

---

## **🔹 YAGNI (You Aren’t Gonna Need It)**
| Proyecto | Archivo | Fallo | Corrección | Línea |
|----------|--------|--------|------------|-------|
| Reto 001 | [Diet.java](#) | Métodos como `deleteDiet()` no se usan. | Eliminar funciones innecesarias. | 90-100 |
| Reto 003 | [Gestion.java](#) | Variables no utilizadas en `menu()`. | Revisar si realmente son necesarias. | 60-70 |
| Reto 004 | [Laberinto.java](#) | `Scanner` se usa para pausar la ejecución, lo cual no es necesario en una versión final. | Eliminar pausa innecesaria. | 100-110 |

---

