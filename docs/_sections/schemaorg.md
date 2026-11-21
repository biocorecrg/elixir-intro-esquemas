## schema.org

```{revealjs-section}
:data-background-color: rgb(15, 23, 92)
:data-background-gradient: linear-gradient(to top, rgb(244, 125, 32) 14px, transparent 14px), linear-gradient(100deg, rgb(12, 11, 61) 0%, rgb(15, 23, 92) 55%, rgb(19, 53, 120) 100%)
```

### Antes de schema.org
- Microformatos (hCard, hCalendar), RDFa, vocabularios de cada buscador…
- Un vocabulario distinto por sector, duplicados entre sí
- Cada buscador recomendaba uno diferente
- Resultado: casi nadie marcaba sus páginas, y lo que había estaba mal formado

### ¿Qué es?
- **2011**: Google, Bing y Yahoo lanzan [schema.org](https://schema.org); Yandex se une ese año
- **Un solo vocabulario**: se marca una vez y lo leen todos
- Pensado para quien publica: ejemplos que copiar, no especificaciones largas
- **2015**: un 31 % de las páginas ya lo usa ([Guha et al.](https://queue.acm.org/detail.cfm?id=2857276))
- **Hoy**: comunidad abierta (W3C + GitHub), 826 tipos y 1540 propiedades
- Admite extensiones por dominio → **Bioschemas**

### Tipos y propiedades

- TODO: jerarquía de tipos (`Thing` → `CreativeWork` → `Dataset`)
- TODO: propiedades y valores esperados

### Formatos

- JSON-LD (recomendado)
- Microdata
- RDFa

El mismo `Dataset` en los tres formatos →

### JSON-LD
Bloque aparte, separado del HTML visible:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "MiBaseDB",
  "description": "Base de datos de ejemplo",
  "creator": { "@type": "Person", "name": "Ana Pérez" }
}
</script>
```

### Microdata
Atributos dentro del HTML visible (`itemscope`, `itemtype`, `itemprop`):

```html
<div itemscope itemtype="https://schema.org/Dataset">
  <h1 itemprop="name">MiBaseDB</h1>
  <p itemprop="description">Base de datos de ejemplo</p>
  <div itemprop="creator" itemscope
       itemtype="https://schema.org/Person">
    <span itemprop="name">Ana Pérez</span>
  </div>
</div>
```

### RDFa
Atributos dentro del HTML visible (`vocab`, `typeof`, `property`):

```html
<div vocab="https://schema.org/" typeof="Dataset">
  <h1 property="name">MiBaseDB</h1>
  <p property="description">Base de datos de ejemplo</p>
  <div property="creator" typeof="Person">
    <span property="name">Ana Pérez</span>
  </div>
</div>
```

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
