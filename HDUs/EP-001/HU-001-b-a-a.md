# Épica: 
EP-001 - Plataforma de Gestión y Evaluación de Competencias

## ID: HU-001-b-a-a  
## Título: Definir y registrar roles de la organización

---

### Historia de Usuario

Como Administrador de Talento, quiero poder registrar los roles de la organización para formalizar las responsabilidades y funciones asociadas a cada puesto de trabajo.

---

### Criterios de Aceptación

#### happy_path
Escenario: Registro exitoso de un rol
  Dado que soy un Administrador de Talento
  Cuando registro un rol con nombre 'Desarrollador Senior' y descripción 'Crea código de alta calidad'
  Entonces el rol 'Desarrollador Senior' se registra y está visible.

#### negativo
Escenario: Intento de registro de rol con nombre existente
  Dado que el rol 'Desarrollador Senior' ya existe en el sistema
  Cuando intento registrar un nuevo rol con el nombre 'Desarrollador Senior'
  Entonces el sistema me notifica que el nombre de rol ya está en uso.

#### borde
Escenario: Registro de rol con descripción de longitud máxima permitida
  Dado que soy un Administrador de Talento
  Cuando registro un rol 'Asistente Junior' con una descripción de 255 caracteres
  Entonces el rol 'Asistente Junior' se registra exitosamente.

#### error
Escenario: Falla del sistema al intentar registrar un rol
  Dado que el sistema experimenta una interrupción inesperada
  Cuando intento registrar un nuevo rol
  Entonces el sistema muestra un mensaje de error y el rol no se registra.

---

### Resultado del Análisis  
OK

