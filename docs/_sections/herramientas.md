## Herramientas

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

### Generar

- Jekyll: [guía ELIXIR](https://elixir-europe-training.github.io/ELIXIR-TrP-Bioschemas/chapters/chapter_02/)
- MkDocs: [guía ELIXIR](https://elixir-europe-training.github.io/ELIXIR-TrP-Bioschemas/chapters/chapter_03/)
- Sphinx: [sphinx-bioschemas](https://pypi.org/project/sphinx-bioschemas/)

### Validar

- [Schema Markup Validator](https://validator.schema.org/)
- [Google Rich Results Test](https://search.google.com/test/rich-results)
- [FAIR-Checker → Inspect](https://fair-checker.france-bioinformatique.fr/inspect): valida contra perfiles Bioschemas

### Recolectar

- [TeSS](https://tess.elixir-europe.org) recolecta `TrainingMaterial`, `Course`, `Event`
- [BMUSE](https://github.com/HW-SWeL/BMUSE): recolector de Bioschemas que genera RDF
- El JSON-LD ya es RDF: se puede cargar en un grafo (siguiente sesión)

### Del JSON-LD al grafo
:::{container} small-code
```python
import json, extruct, rdflib, requests

html = requests.get("https://USUARIO.github.io/REPO/").text
jsonld = extruct.extract(html, syntaxes=["json-ld"])["json-ld"]
g = rdflib.Graph().parse(data=json.dumps(jsonld), format="json-ld")
print(g.serialize(format="turtle"))
```

```turtle
# extracto
<https://example.org/mibasedb> a schema:Dataset ;
    dcterms:conformsTo
        <https://bioschemas.org/profiles/Dataset/1.0-RELEASE> ;
    schema:name "MiBaseDB" ;
    schema:license "https://creativecommons.org/licenses/by/4.0/" .
```
:::
- Sin `@id`, el recurso queda como nodo en blanco `[]` y no se puede enlazar
