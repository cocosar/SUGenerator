# Épica: 
EP-001 - Plataforma de Gestión y Evaluación de Competencias

## ID: HU-001-b-b  
## Título: Asociar competencias a roles y grados

---

### Historia de Usuario

Como Administrador de Talento, quiero asociar las competencias a los roles y grados existentes para formalizar y comunicar las rutas de crecimiento profesional en la organización.

---

### Criterios de Aceptación

#### happy_path
Escenario: Asociar una competencia a un rol y grado existentes.
  Given Soy un Administrador de Talento y existen roles, grados y competencias.
  When Asocio una competencia específica a un rol y grado.
  Then La competencia se asocia exitosamente y la ruta de crecimiento se actualiza.

#### negativo
Escenario: Intentar asociar una competencia a un rol inexistente.
  Given Soy un Administrador de Talento y existen competencias pero el rol no.
  When Intento asociar una competencia a un rol inexistente.
  Then El sistema muestra un mensaje de error indicando que el rol no existe.

#### borde
Escenario: Asociar competencia a rol/grado con muchas competencias asociadas.
  Given Soy Administrador de Talento y rol/grado tiene 99 competencias asociadas.
  When Asocio una competencia adicional (la número 100) a ese rol y grado.
  Then La competencia se asocia y el rendimiento del sistema no se degrada.

#### error
Escenario: Ocurre un error inesperado al asociar una competencia.
  Given Soy un Administrador de Talento y el sistema está activo.
  When Intento asociar una competencia y ocurre un fallo interno.
  Then El sistema muestra un mensaje de error genérico y la asociación no se completa.

---

### Resultado del Análisis  
OK

