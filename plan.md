# Plan d'action

## User stories sélectionnées

- Story 4 : Réduction des requêtes réseau — **Critique**
- Story 1 : Chargement initial plus rapide — **Haute**
- Story 2 : Réduction poids images — **Haute**

> Story 3 (Accessibilité) non retenue car non identifiée comme problème lors de l'audit.

## Modifications prévues

### 1. Supprimer les requêtes répétées vers `/api/payload`

- Supprimer uniquement les requêtes vers `/api/payload` dans le `setInterval` de `App.tsx`
- Conserver le fetch vers `/api/server` qui alimente les métriques RAM/CPU/RPS

### 2. Supprimer les assets lourds inutiles

- Supprimer le chargement de `big.css` et `big.js` injectés dynamiquement dans `App.tsx`

### 3. Convertir l'image de fond en WebP

- Convertir `large.jpg` en format WebP pour réduire son poids
- Remplacer la référence dans `App.tsx` par `large.webp`

## Ordre de réalisation

1. Suppression des requêtes `/api/payload` — gain immédiat sur le nombre de requêtes
2. Suppression des assets lourds `big.js` et `big.css` — gain sur le poids de la page
3. Conversion de `large.jpg` en WebP — gain sur le poids des images
