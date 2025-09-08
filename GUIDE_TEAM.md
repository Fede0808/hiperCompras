# 🚀 Guía de Buenas Prácticas de Trabajo en GitHub

Este documento unifica las reglas y recomendaciones para el equipo de desarrollo.  
El objetivo es mantener un flujo de trabajo ordenado, colaborativo y alineado con la metodología **MVP (Minimum Viable Product)**.

---

## 🌳 Estrategia de Ramas

### Ramas principales
- **`main`**
  - Código estable y listo para producción.
  - Solo recibe merges desde `develop` cuando se completa un MVP o release.
- **`develop`**
  - Código en desarrollo.
  - Todos los cambios (`feature/*`, `fix/*`) se integran aquí primero.

### Ramas de trabajo
- **`feature/<nombre>`** → nuevas funcionalidades.  
  Ejemplo: `feature/integracion-binance`.
- **`fix/<nombre>`** → corrección de bugs.  
  Ejemplo: `fix/error-promos`.

### Flujo recomendado
1. Crear rama desde `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/nombre
   '''
2. Trabajar y hacer commits descriptivos.
3. Abrir un Pull Request (PR) hacia develop.
4. Revisar en equipo → merge a develop.
5. Cuando se finaliza un MVP → merge de develop a main.

## Convenciones de Commits

Usar prefijos para dar contexto:
  feat: → nueva funcionalidad
  fix: → corrección de bug
  docs: → cambios en documentación
  refactor: → cambios de código sin alterar funcionalidad
  test: → agregar/cambiar pruebas
  
Ejemplos:

feat: agrega visualización de evolución del portafolio
fix: corrige bug en cálculo de promociones

## Uso de GitHub Projects (Metodología MVP)

Trabajamos con GitHub Projects como tablero Kanban para organizar el trabajo.

**Columnas recomendadas**

Backlog → ideas o tareas futuras.
To Do → tareas priorizadas del sprint/MVP.
In Progress → tareas en desarrollo.
Review → tareas en PR o en testeo.
Done → tareas completadas.

**Flujo**

1. Cada Issue se crea con un entregable concreto (ej. “Importar datos desde Broker X”).
2. Se asigna al Project y al Milestone correspondiente.
3. Se trabaja en una rama (feature/* o fix/*) vinculada al Issue.
4. Al abrir PR → mover a Review.
5. Al aprobar y mergear → mover a Done.

## Uso de Milestones

Los Milestones sirven para agrupar Issues y PRs que forman parte de un mismo entregable o versión.

Ejemplo Portafolios:
  MVP – Consolidación de los datos y Visualización → incluye feature/import-iol, feature/evolucion.

Ejemplo HiperCompras:

  MVP – Canasta Óptima → incluye feature/modelo-datos, feature/optimizador, fix/promos.

Beneficios
  1. Permite ver progreso de un MVP con barra de avance (Issues cerrados vs. abiertos).
  2. Ayuda a planificar y comunicar objetivos del equipo.
  3. Da visibilidad de qué entra en cada release o entrega.
