## Bioschemas

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

### Historia
- **2015**: nace como comunidad en un taller en Hinxton (Reino Unido), impulsado por [ELIXIR](https://elixir-europe.org)
- **2017**: [*From Potato Salad to Protein Annotation*](https://bioschemas.org/about/publications) (ISWC 2017)
- **2021**: [schema.org v13.0](https://schema.org/docs/releases.html#v13.0) incorpora `Gene`, `Protein`, `Taxon`, `BioChemEntity`…
- **Hoy**: política insignia de ELIXIR (Programa 2024-28), comunidad abierta con llamadas mensuales

### ¿Por qué no basta schema.org?
- Sabe describir recetas, películas o eventos…
- …pero no genes, proteínas ni taxones
- Y donde sí hay tipos (`Dataset`), ofrece **demasiadas** propiedades: ¿cuáles usar?

### ¿Qué es?
Objetivo: la **F** de FAIR, que los recursos de ciencias de la vida se **encuentren** en la web.

1. **Tipos y propiedades** nuevos, propuestos a schema.org
2. **Perfiles**: qué propiedades usar y cómo

Recomendado por ELIXIR, el [ERC](https://erc.europa.eu/sites/default/files/document/file/ERC_info_document-Open_Research_Data_and_Data_Management_Plans.pdf) y la [ISB](https://www.biocuration.org/curate-now/) · [bioschemas.org](https://bioschemas.org)

### Tipos y perfiles
- **Perfil**: propiedades **mínimas** · **recomendadas** · **opcionales**, cardinalidad y ontologías
- Ejemplo: [`schema.org/Dataset`](https://schema.org/Dataset) tiene más de 100 propiedades
- El [perfil `Dataset`](https://bioschemas.org/profiles/Dataset/): **5 mínimas** + **8 recomendadas**
- Con las mínimas ya aparece en [Google Dataset Search](https://datasetsearch.research.google.com/)

### `conformsTo`
Declara qué perfil (y versión) sigue el recurso:

:::{container} small-code
```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "http://purl.org/dc/terms/conformsTo": {
    "@id": "https://bioschemas.org/profiles/Dataset/1.0-RELEASE",
    "@type": "CreativeWork"
  },
  "name": "MiBaseDB"
}
```
:::

- Viene de Dublin Core (no existe en schema.org): por eso la URI completa
- Propiedad **mínima**; la URL del perfil debe llevar **versión**

### Estados de un perfil
- **DRAFT**: en desarrollo, puede cambiar
- **RELEASE**: estable
- **DEPRECATED**: obsoleto
- La versión va en la URL de `conformsTo`:<br>`https://bioschemas.org/profiles/Dataset/1.0-RELEASE`

### Estados y validación
Con [FAIR-Checker](https://fair-checker.france-bioinformatique.fr/inspect):
- Con `conformsTo`: se valida contra **esa versión**; faltan mínimas → **errores**, faltan recomendadas → **avisos**
- Avisa si el perfil está *deprecated* y cuál es la última versión
- Sin `conformsTo`: se adivina por el tipo y se valida contra la última *release*

### Perfiles destacados
- **Recursos**: `Dataset`, `DataCatalog`, `ComputationalTool`, `ComputationalWorkflow`
- **Formación**: `TrainingMaterial`, `Course`, `CourseInstance`
- **Biología**: `Gene`, `Protein`, `Taxon`, `Sample`, `ChemicalSubstance`
- [Lista de perfiles](https://bioschemas.org/profiles/) (~38, muchos en *draft*)

### ¿Quién lo usa?

::::{container} cols
:::{container}
**Publican**
- [bio.tools](https://bio.tools): `ComputationalTool`
- [WorkflowHub](https://workflowhub.eu): `ComputationalWorkflow`
- [FAIRsharing](https://fairsharing.org), [InterPro](https://www.ebi.ac.uk/interpro/): `Dataset`
:::
:::{container}
**Consumen**
- [TeSS](https://tess.elixir-europe.org): recolecta cursos y materiales
- [BMUSE](https://github.com/HW-SWeL/BMUSE): recolector → IDPcentral
- [FAIR-Checker](https://fair-checker.france-bioinformatique.fr): evaluación FAIR
:::
::::

Los mismos registros de la **Semana 1, Día 4**
