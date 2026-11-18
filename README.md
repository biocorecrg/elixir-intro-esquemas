# Esquemas de metadatos y Bioschemas

Presentación (en español) sobre schema.org y Bioschemas para el [Taller ELIXIR-México 2026](https://laboratorio-de-biologia-computacional.github.io/taller-elixir-mexico-2026/#semana-2) (24 de noviembre de 2026), con una práctica breve en GitHub Pages.

Basada en [sphinx-bioschemas-presentation](https://github.com/biocorecrg/sphinx-bioschemas-presentation).

## Estructura

- `docs/` — diapositivas (Sphinx + MyST + reveal.js); secciones en `docs/_sections/`
- `docs/schemaorg.yaml` — metadatos schema.org de la propia presentación
- `practica/` — plantilla y solución de la práctica

## Construir

```bash
python -m venv .venv && . .venv/bin/activate
pip install -r docs/requirements.txt
cd docs && make revealjs   # salida en docs/_build/revealjs
```

Cada push a `main` (y cada tag) se publica en GitHub Pages: `/latest/` (diapositivas) y `/practica/`.
