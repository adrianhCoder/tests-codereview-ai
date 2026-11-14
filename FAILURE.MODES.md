# FAILURE-MODES.md — catálogo de fallos de IA en payments-svc

## Categoría: Generación de tests
- [n1] Para amount == 0 en calculate_fee/total_with_fee, la IA documentó el comportamiento actual del código (sin fee) como si fuera el contrato de negocio, sin cuestionar si debería aplicar el fee mínimo como en cualquier otro monto.