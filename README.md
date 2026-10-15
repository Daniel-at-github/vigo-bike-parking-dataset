## Tecnologías utilizadas

### Datos

- [SQLite](https://www.sqlite.org/): almacenamiento local del dataset.
- [Datasette](https://github.com/simonw/datasette): exploración y consulta de bases de datos SQLite.
- [Datasette Lite](https://github.com/simonw/datasette-lite): ejecución de Datasette completamente en el navegador.
- [DuckDB](https://duckdb.org/): motor analítico para consultas SQL sobre datos locales.
- [DuckDB-WASM](https://github.com/duckdb): ejecución de DuckDB directamente en el navegador mediante WebAssembly.

### Visualización

- [Leaflet](https://github.com/Leaft: visualización interactiva de mapas.
- [OpenStreetMap](https://www.openstreetmap.org/): cartografía base utilizada por el visor.

### Infraestructura

- [GitHub](https://github.com/): control de versiones y alojamiento del proyecto.
- [GitHub Pages](https://pages.github.com/): publicación de la aplicación estática.

### Tecnologías Web

- [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML://developer.mozilla.org/en-US/docs/Web/CSS
- [JavaScript](https://illa.org/en-US/docs/Web/JavaScript

## Arquitectura

```text
GeoJSON (datos.vigo.org)
          │
          ▼
       SQLite
          │
    ┌─────┴─────┐
    ▼           ▼
Datasette    DuckDB-WASM
   Lite           │
    │             ▼
    │         GeoJSON
    │             │
    └─────┬───────┘
          ▼
       Leaflet
          │
          ▼
     GitHub Pages
``

Demo: https://daniel-at-github.github.io/vigo-bike-parking-dataset/
