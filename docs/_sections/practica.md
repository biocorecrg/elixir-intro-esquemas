## Práctica

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

**Publica una página con metadatos Bioschemas en GitHub Pages**

Plantillas e instrucciones: [biocorecrg.github.io/elixir-intro-esquemas/practica/](https://biocorecrg.github.io/elixir-intro-esquemas/practica/)

### Paso 1 · Crear repositorio

- Crea un repositorio **público** nuevo en GitHub
- Descarga [`index.html`](https://biocorecrg.github.io/elixir-intro-esquemas/practica/index.html) y súbelo: *Add file → Upload files*

### Paso 2 · Completar JSON-LD

- Edita `index.html` en GitHub y completa el bloque `<script type="application/ld+json">`
- Sigue el [perfil `Dataset` 1.0-RELEASE](https://bioschemas.org/profiles/Dataset/1.0-RELEASE)
- Mínimo: `@id`, `conformsTo`, `name`, `description`, `identifier`, `keywords`, `license`, `url`

### Paso 3 · Publicar

- *Settings → Pages → Deploy from a branch* → rama `main`, carpeta `/ (root)`
- En uno o dos minutos: `https://USUARIO.github.io/REPO/`

### Paso 4 · Validar

- schema.org: pega la URL publicada en [validator.schema.org](https://validator.schema.org/)
- Perfil Bioschemas: [FAIR-Checker → Inspect](https://fair-checker.france-bioinformatique.fr/inspect)

### Paso 4 · Validar con la API

```bash
curl --get https://fair-checker.france-bioinformatique.fr/api/inspect/bioschemas_validation \
  --data-urlencode "url=https://USUARIO.github.io/REPO/"
```

- `"method": "by_conformsto"` → tu perfil: `"conforms": true`, `errors: []`
- `warnings` → recomendadas que faltan
- `"method": "by_type"` (p. ej. `Person`) → perfiles *draft*, ignorar

### Variante · TrainingMaterial

- Describe un tutorial, diapositivas o notebook
- Plantilla `training.html` · tipo `LearningResource`
- [Perfil TrainingMaterial 1.0-RELEASE](https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE)
- Mínimo: `@id`, `conformsTo`, `name`, `description`, `keywords`
- [TeSS](https://tess.elixir-europe.org) recolecta este perfil de las fuentes registradas

### Extra

- Añadir a `keywords` un término de EDAM o GO como `DefinedTerm` (búscalo en [OLS](https://www.ebi.ac.uk/ols4/))
- Probar `ComputationalTool` para un repositorio de software
