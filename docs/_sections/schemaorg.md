## schema.org

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

### ¿Qué es?

- TODO: iniciativa de Google, Microsoft, Yahoo y Yandex (2011)
- TODO: vocabulario común para describir cosas en la web
- [schema.org](https://schema.org)

### Tipos y propiedades

- TODO: jerarquía de tipos (`Thing` → `CreativeWork` → `Dataset`)
- TODO: propiedades y valores esperados

### Formatos

- JSON-LD (recomendado)
- Microdata
- RDFa

TODO: ejemplo comparativo

### Ejemplo: `Dataset`

```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "TODO",
  "description": "TODO"
}
```

### ¿Quién lee el marcado?
- **Google**: [Dataset Search](https://datasetsearch.research.google.com/) e informe en Search Console
  - En 2025 dejó de mostrar *Course Info*
- **Bing** · [**Web Data Commons**](https://webdatacommons.org/structureddata/schemaorg/) (Common Crawl)
- Otras disciplinas: [*Science on Schema.org*](https://github.com/ESIPFed/science-on-schema.org)
- **IA**: sin evidencia de que use el JSON-LD
