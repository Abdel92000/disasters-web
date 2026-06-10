# Audit Initial

**Date :** 10/06/2026  
**Outil :** Extension GreenIT Analysis
**URL analysée :** http://localhost:3000

## 1. Résultats GreenIT

- EcoIndex : 44.98 (D)
- Consommation eau : 3.15 cl
- Émissions GES : 2.10 gCO2e

## 2. Poids de la page

- Taille totale : 17 513 kB

## 3. Nombre de requêtes réseau

- 1472 requêtes au moment de l'audit
- Ce nombre augmente continuellement tant que la page est ouverte
- Lighthouse signale des payloads réseau excessifs : taille totale de 17 107 kB

## 4. Principaux problèmes identifiés

- **Requêtes répétées vers `/api/payload`** : l'application envoie en continu des requêtes vers cette route. Le nombre de requêtes augmente continuellement, ce qui fait exploser le poids de la page au fil du temps.

- **Chargement d'assets lourds** : des fichiers CSS et JavaScript volumineux sont chargés par la page. Lighthouse détecte qu'une grande partie de ce code n'est pas utilisée (économie estimée : 1 675 kB de JS et 28 kB de CSS).

- **Image non optimisée** : une image lourde est chargée en taille originale alors qu'elle est affichée beaucoup plus petite. Lighthouse suggère d'utiliser un format moderne (WebP/AVIF) et de redimensionner l'image `large.jpg` (économie estimée : 6 830 kB).

- **Fichier JavaScript volumineux inutilisé** : un fichier JavaScript lourd est chargé depuis le serveur mais son contenu n'est pas utilisé par l'application (1 574 kB inutilisés détectés par Lighthouse).
