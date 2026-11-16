# payments-svc

API de pagos en Python para el curso sobre testing y code review con IA.

El proyecto esta preparado para avanzar por incrementos de clase. Para el Modulo C parte de una base limpia de producto: `amounts.py`, `refunds.py`, `auth.py` y `api.py` tienen contratos confirmados y tests unitarios.

Los artefactos especificos del revisor de PR del Modulo B se dejan fuera de esta rama para que las demos de auditoria de codigo existente empiecen sin ruido.

## Instalacion

```sh
python -m venv .venv
source .venv/bin/activate
pip install -e .[dev]
```

## Tests

```sh
python -m unittest discover -s tests -p "test_*.py" -v
```

## Smoke test

```sh
python scripts/smoke_test.py
```

## Mutation testing

```sh
sh scripts/mutation_domain.sh
```

## API local

```sh
uvicorn payments_svc.api:app --reload
```

Endpoints:

- `GET /health`
- `POST /payments`
- `POST /refunds`


# Guía de Ramas del Proyecto

## 📌 Estructura y Orden de Ramas

1. `prep/modulo-0-base-funcional` (Módulo 0 y 1)
2. `preclase-02-catalogo-inicial`
3. `preclase-03-decisiones-contrato`
4. `preclase-04-herramienta-mutacion`
5. `preclase-05-comparacion-prompts`
6. `develop` y `prep/modulo-b-base-limpia`
7. `preclase-07-schema-review`
8. `preclase-08-pr-mixto`
9. `preclase-09-ground-truth`
10. `preclase-10-legacy-settlement`
11. `preclase-11-semgrep-ruido`
12. `preclase-12-superficie-adversarial`
13. `preclase-13-dependencia-alucinada`
14. `preclase-14-ruta-llm-vulnerable`
15. `preclase-15-openrouter-ready` y `test/clase-15-openrouter-check`
16. `preclase-16-shadow-ready`
17. `preclase-17-cost-ready`
18. `preclase-18-flywheel-ready`
19. `preclase-19-policy-ready`
