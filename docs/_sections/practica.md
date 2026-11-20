## Práctica

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

**Publica una página con metadatos Bioschemas en GitHub Pages**

TODO: enlace a la plantilla publicada (`/practica/`)

### Paso 1 · Crear repositorio

- TODO: nuevo repositorio público en GitHub
- TODO: subir `index.html` de la plantilla

### Paso 2 · Completar JSON-LD

- TODO: rellenar el bloque `<script type="application/ld+json">`
- TODO: perfil Bioschemas `Dataset`

### Paso 3 · Publicar

- TODO: Settings → Pages → rama `main`

### Paso 4 · Validar

- TODO: URL publicada en [validator.schema.org](https://validator.schema.org/)
- Perfil Bioschemas: [FAIR-Checker → Inspect](https://fair-checker.france-bioinformatique.fr/inspect)

### Variante · TrainingMaterial

- Describe un tutorial, diapositivas o notebook
- Plantilla `training.html` · tipo `LearningResource`
- [Perfil TrainingMaterial 1.0-RELEASE](https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE)
- Mínimo: `@id`, `conformsTo`, `name`, `description`, `keywords`
- [TeSS](https://tess.elixir-europe.org) cosecha este perfil de las fuentes registradas

### Extra

- Probar `ComputationalTool` para un repositorio de software
