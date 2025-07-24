# Épica: 
EP-001 - Plataforma de Gestión y Evaluación de Competencias

## ID: HU-001-b-b  
## Título: Definir matriz de competencias, roles y grados – Parte 2 – Parte 2

---

### Historia de Usuario

Como Administrador de Talento, quiero asociar competencias a cada combinación de rol y seniority, para definir las rutas de carrera de los colaboradores.

---

### Criterios de Aceptación

#### happy_path
Escenario: Asociar competencia a rol y nivel exitosamente
  Dado un rol, un nivel de seniority y una competencia existentes
  Cuando el administrador asocia la competencia al rol y al nivel
  Entonces la asociación se registra correctamente y es visible

#### negativo
Escenario: No asociar competencia inexistente
  Dado un rol y un nivel de seniority existentes
  Cuando el administrador intenta asociar una competencia inexistente
  Entonces el sistema debe mostrar un mensaje de error 'Competencia no encontrada'

#### borde
Escenario: Asociar competencia al límite máximo
  Dado un rol y nivel con N-1 competencias asociadas (N es el máximo)
  Cuando el administrador asocia la N-ésima competencia
  Entonces la asociación se registra exitosamente

#### error
Escenario: Error interno al asociar competencia
  Dado un rol, nivel y competencia válidos
  Cuando ocurre un fallo interno del sistema al intentar asociar
  Entonces el sistema debe informar un error y no registrar la asociación

---

### Resultado del Análisis  
REWORK

### Observaciones
La historia presenta una fuerte dependencia de la creación previa de roles y grados, lo cual incumple el principio de Independencia (I). Es crucial gestionar esta dependencia para permitir un desarrollo más flexible. Gherkin añadido en el refinador.