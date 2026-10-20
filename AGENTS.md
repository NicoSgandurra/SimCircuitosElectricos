# AGENTS.md — SimCircuitosElectricos

## Flujo de Trabajo en Git y Uso de Ramas

- **Rama principal por defecto (main)**: Todo el trabajo debe realizarse e integrarse directamente sobre la rama main.
- **Excepciones para crear ramas secundarias**: Solo se debe crear y trabajar en una rama separada en cualquiera de estos dos casos:
  1. **Característica muy riesgosa**: Cuando el cambio implique un riesgo alto de romper funcionalidad crítica o requiera experimentación aislada.
  2. **Múltiples agentes en simultáneo**: Cuando haya dos o más agentes trabajando al mismo tiempo dentro del mismo repositorio y se requiera aislar el contexto para evitar conflictos.
- Fuera de esas dos excepciones, no crear ramas eature/*, ix/* ni worktrees innecesarios; mantener main actualizada y limpia.
