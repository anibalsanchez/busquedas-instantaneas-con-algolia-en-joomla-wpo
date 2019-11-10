# Cómo buscamos <i class="fas fa-search"></i> <!-- .slide: class="" -->


## La Búsqueda Clásica <i class="fas fa-search"></i>

- Consultas de búsqueda simple<!--.element: class="small" -->
- Basada en un motor SQL <!--.element: class="small" -->
- Resultados compuestos por consultas separadas <!--.element: class="small" -->
- Resultados ordenados según un criterio a la vez <!-- .element: class="small" -->
- Integrado con el sistema de plugins <!--.element: class="small" -->
- Buscar por un formulario POST (400-800ms)<!--.element: class="small" -->


## La Búsqueda Inteligente <i class="fas fa-search-plus"></i>

- Búsquedas simples en texto completo <!-- .element: class="small" -->
- Basado en el motor SQL y con hechos "facts" indexados <!-- .element: class="small" -->
- Resultados compuestos por consultas separadas <!--.element: class="small" -->
- Resultados ordenados por criterio único <!--.element: class="small" -->
- Integrado con el sistema de plugins <!--.element: class="small" -->
- Buscar en el formulario POST (400-800ms)<!--.element: class="small" -->


## La Búsqueda Algolia <i class="fab fa-searchengin"></i>

- Búsquedas complejas en texto completo <!--.element: class="small" -->
- Basado en un motor de búsqueda distribuido NoSQL <!--.element: class="small" -->
- Poteniado by índices gestionados<!--.element: class="small" -->
- Integrado por un amplio conjunto de UI Widgets <!-- .element: class="small" -->
- Configuración avanzada en el backend de Algolia <!-- .element: class="small" -->
- Integrado mediante extensiones (por ejemplo, [XT Search](https://www.extly.com/xt-search-for-joomla.html))<!-- .element: class="small" -->
- Búsqueda Instantánea, consultas de remotas por tipeo (50ms)<!--.element: class="small" -->


## Otros tipos de Búsquedas Algolia <i class="fab fa-searchengin"></i>

- <i class="fas fa-search-location"></i>Búsqueda por Ubicación
- <i class="fas fa-microphone"></i> Búsqueda por voz


## Algolia en términos de CMS <i class="fab fa-searchengin"></i><!-- .slide: class=" plain console" -->

- Un proceso de indexación
- Indexación de eventos (alta y actualización)
- Módulos de búsqueda
  - Basado en los widgets de Algolia
  - Búsqueda por Auto-completado
  - Búsqueda instantánea / extendida


## Algolia implementation for JED <!-- .slide: class=" plain console" -->

La Configuración del Backend de Algolia

- Índices
- Atributos de búsqueda
- Atributos de los resultados
- Campos y Facetas
- Sistema de clasificación y ordenamiento
- [JED Search Cases Docs](https://github.com/joomla/jed-issues/wiki/JED-Search-use-cases-and-definitions)


## Widget de Auto-Completado <!-- .slide: class=" plain console" -->

    const search= instantsearch(/* parameters */);

    const makeAutocomplete= instantsearch.connectors.connectAutocomplete(
      function renderFn(
          renderOpts: AutocompleteRenderingOptions,
          isFirstRendering: boolean) {
        // render the custom Autocomplete widget
      }
    );

    const  customAutocomplete = makeAutocomplete(instanceOpts: CustomAutocompleteWidgetOptions);
    search.addWidget(customAutocomplete);


## XT Search for Algolia <!-- .slide: class=" plain console" -->

Una única solución para Joomla, PrestaShop y WordPress

![SanJuan Turismo - Autocomplete](images/30-how/XTSearch-for-joomla.png)


## XT Search for Algolia

- Un componente para la indexación de datos
- Módulos
  - Autocomplete<!--.element: class="small" -->
  - InstantSearch<!--.element: class="small" -->
  - Navegar por Facet<!-- .element: class="small" -->
- Listo para Joomla 3 / 4
- Listo para prestaShop 1.6 / 1.7
- WordPress 5 / WooCommerce (Próximamente)

[extly.com/xt-search-for-joomla](https://www.extly.com/xt-search-for-joomla.html)