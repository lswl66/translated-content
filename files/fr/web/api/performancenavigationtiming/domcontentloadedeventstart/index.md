---
title: PerformanceNavigationTiming.domContentLoadedEventStart
slug: Web/API/PerformanceNavigationTiming/domContentLoadedEventStart
tags:
  - API
  - Property
  - Propriété
  - Reference
  - PerformanceNavigationTiming
  - Performance Web
translation_of: Web/API/PerformanceNavigationTiming/domContentLoadedEventStart
---
{{APIRef("Navigation Timing")}}{{SeeCompatTable}}

La propriété en lecture seule **`domContentLoadedEventStart`** retourne un [`timestamp`](/fr/docs/Web/API/DOMHighResTimeStamp) représentant la valeur temporelle égale au temps immédiatement avant que l'agent utilisateur ne déclenche l'événement [`DOMContentLoaded`](/fr/docs/Web/API/Document/DOMContentLoaded_event) du document actuel.

## Syntaxe

```js
perfEntry.domContentLoadedEventStart;
```

### Valeur de retour

Un [`timestamp`](/fr/docs/Web/API/DOMHighResTimeStamp) représentant la valeur temporelle égale au temps immédiatement avant que l'agent utilisateur ne déclenche l'événement [`DOMContentLoaded`](/fr/docs/Web/API/Document/DOMContentLoaded_event) du document actuel.

## Exemple

L'exemple suivant illustre l'utilisation de cette propriété.

```js
function print_nav_timing_data() {
  // Utilise getEntriesByType() pour obtenir uniquement les événements de type "navigation".
  let perfEntries = performance.getEntriesByType("navigation");

  for (let i = 0; i < perfEntries.length; i++) {
    console.log("= Entrée de navigation : entry[" + i + "]");
    let p = perfEntries[i];
    // propriétés du DOM
    console.log("Contenu du DOM chargé = " + (p.domContentLoadedEventEnd - p.domContentLoadedEventStart));
    console.log("Contenu du DOM complet = " + p.domComplete);
    console.log("Contenu du DOM interactif = " + p.interactive);

    // temps de chargement et de déchargement des documents
    console.log("Document chargé = " + (p.loadEventEnd - p.loadEventStart));
    console.log("Document déchargé = " + (p.unloadEventEnd - p.unloadEventStart));

    // autres propriétés
    console.log("type = " + p.type);
    console.log("redirectCount = " + p.redirectCount);
  }
}
```

## Spécifications

| Spécification                                                                                                                                                                                            | Statut                                               | Commentaire          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | -------------------- |
| {{SpecName('Navigation Timing Level 2', '#dom-performancenavigationtiming-domcontentloadedeventstart', 'domContentLoadedEventStart')}} | {{Spec2('Navigation Timing Level 2')}} | Définition initiale. |

## Compatibilité des navigateurs

{{Compat("api.PerformanceNavigationTiming.domContentLoadedEventStart")}}
