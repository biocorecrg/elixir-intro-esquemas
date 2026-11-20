# Práctica: metadatos Bioschemas en GitHub Pages

1. Crea un repositorio público nuevo en GitHub.
2. Sube [`index.html`](index.html) (*Add file → Upload files*).
3. Completa el bloque JSON-LD siguiendo el [perfil Dataset](https://bioschemas.org/profiles/Dataset).
4. Activa GitHub Pages: *Settings → Pages → Deploy from a branch → `main`*.
5. Valida la URL publicada en [validator.schema.org](https://validator.schema.org/) y contra el perfil Bioschemas con [FAIR-Checker → Inspect](https://fair-checker.france-bioinformatique.fr/inspect).

Solución de referencia: [`solucion.html`](solucion.html).

## Variante: TrainingMaterial

Describe un material de formación (tutorial, diapositivas, notebook) en lugar de un dataset.

1. Usa [`training.html`](training.html) como plantilla (o tu propio material).
2. Sigue el [perfil TrainingMaterial 1.0-RELEASE](https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE): tipo schema.org `LearningResource`.
   Mínimo: `@id`, `conformsTo`, `name`, `description`, `keywords`.
3. Publica y valida igual que arriba.

Este perfil es el que [TeSS](https://tess.elixir-europe.org) (portal de formación de ELIXIR) cosecha de los sitios registrados como fuente.

Solución de referencia: [`training-solucion.html`](training-solucion.html).

**Extra:** prueba `ComputationalTool` para un repositorio de software.
