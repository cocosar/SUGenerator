# Épica: 
EP-001 - Plataforma de Gestión y Evaluación de Competencias

## ID: HU-001-b-a-b  
## Título: Definir matriz de competencias, roles y grados – Parte 2 – Parte 1 – Parte 2

---

### Historia de Usuario

Como Administrador de Talento, quiero poder crear y gestionar los grados de seniority para estandarizar la estructura y el crecimiento profesional dentro de la compañía.

---

### Criterios de Aceptación

#### happy_path
Escenario: Crear un nuevo grado de seniority exitosamente
  Given soy un Administrador de Talento
  When creo un nuevo grado de seniority con nombre y descripción válidos
  Then el grado de seniority es guardado y visible en el sistema

#### negativo
Escenario: Intentar crear un grado de seniority con nombre existente
  Given existe un grado de seniority con el nombre "Senior"
  When intento crear un nuevo grado de seniority llamado "Senior"
  Then el sistema muestra un mensaje de error indicando que el nombre ya existe

#### borde
Escenario: Crear un grado de seniority con nombre y descripción al límite de caracteres
  Given soy un Administrador de Talento
  When creo un grado de seniority con nombre y descripción de longitud máxima
  Then el grado de seniority es guardado correctamente en el sistema

#### error
Escenario: Error del sistema al intentar guardar un grado de seniority
  Given soy un Administrador de Talento
  When intento crear un grado de seniority y ocurre un error interno del sistema
  Then el sistema muestra un mensaje de error genérico y no guarda el grado

---

### Resultado del Análisis  
OK

