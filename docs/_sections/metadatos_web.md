## Metadatos estructurados en la web

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

### ¿Por qué?
- Una persona lee «MiBaseDB, de Ana Pérez, licencia CC BY» y entiende qué es cada cosa
- Un programa solo ve texto: no sabe qué es el nombre, quién la autora, cuál la licencia
- Los metadatos estructurados lo declaran en la misma página
- Los leen buscadores, catálogos y evaluadores FAIR

### FAIR
Ya visto en la Semana 1: diagnóstico FAIR (día 2), FAIR-Checker (día 3), registros (día 4).

- **F4**: los (meta)datos se registran o indexan en un recurso donde se pueda buscar
  - Con el marcado, la página se indexa sin rellenar formularios
- **I2**: los (meta)datos usan vocabularios que siguen FAIR
  - schema.org y Bioschemas son vocabularios abiertos y versionados

### Dónde encaja hoy
- **Antes**: tipos de metadatos, ciclo de vida de los datos, ontologías
- **Ahora**: esquemas de metadatos en la web
- **Después**: grafo con RDF y consultas SPARQL
  - El JSON-LD de hoy ya es RDF
