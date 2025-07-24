# Épica: 
EP-001 - Plataforma de Gestión y Evaluación de Competencias

## ID: HU-001-b-a-a-a-a  
## Título: Gestión de Roles – Parte 1

---

### Historia de Usuario

Como Administrador de Talento, quiero crear un rol nuevo, especificando su nombre y descripción, para definir las posiciones que componen la estructura organizativa de la empresa.

---

### Criterios de Aceptación

#### happy_path
Escenario: Creación exitosa de un rol con nombre y descripción válidos
  Given que soy un Administrador de Talento
  When creo un nuevo rol con nombre "Gerente de Proyecto" y descripción "Líder de equipos de proyectos complejos"
  Then el rol "Gerente de Proyecto" debe ser creado exitosamente y visible en el sistema

#### negativo
Escenario: Fallo al crear un rol con un nombre ya existente
  Given que el rol "Gerente de Proyecto" ya existe en el sistema
  When intento crear un nuevo rol con el nombre "Gerente de Proyecto"
  Then el sistema debe mostrar un mensaje de error indicando que el nombre del rol ya existe

#### borde
Escenario: Fallo al crear un rol con nombre vacío
  Given que soy un Administrador de Talento
  When intento crear un nuevo rol con nombre vacío y descripción "Descripción de prueba"
  Then el sistema debe mostrar un mensaje de error indicando que el nombre del rol no puede estar vacío

#### error
Escenario: Fallo interno del sistema al crear un rol
  Given que soy un Administrador de Talento
  When intento crear un nuevo rol y ocurre un error inesperado del sistema
  Then el sistema debe mostrar un mensaje de error genérico y el rol no debe ser creado

---

### Resultado del Análisis  
OK

