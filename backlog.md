# Backlog du projet "Optimisation Sante+"

## USER STORIES

---

### Story 1 : Chargement initial plus rapide

**En tant que** nouvel utilisateur web,  
**je veux** que l'écran d'accueil charge en moins de 1,5 s  
**afin de** ne pas décrocher lors d'un pic de réseau lent.

- 🎯 Objectif : temps de chargement < 1500 ms
- 🧱 BP associée : réduire taille des ressources / lazy-loading
- 🛠️ KPI : LCP sur web (Lighthouse)
- 📅 Tag roadmap : M2
- 🔺 Priorité : **Haute** — LCP mesuré à 18.3s lors de l'audit, soit 12 fois plus que l'objectif

---

### Story 2 : Réduction poids images

**En tant que** utilisateur récurrent,  
**je veux** que les visuels du dashboard soient plus légers  
**afin de** économiser de la data sur mon forfait.

- 🎯 Objectif : 80% des images converties en WebP
- 🧱 BP associée : compression d'images / formats modernes
- 🛠️ KPI : poids total dossier `/assets` < 2 Mo
- 📅 Tag roadmap : M3
- 🔺 Priorité : **Haute** — économie possible de 6 830 kB sur les images détectée par Lighthouse

---

### Story 3 : Accessibilité améliorée

**En tant que** utilisateur malvoyant,  
**je veux** que les contrastes texte/fond soient conformes AA  
**afin de** pouvoir utiliser l'app sans difficulté visuelle.

- 🎯 Objectif : conformité AA WCAG
- 🧱 BP associée : respect contrastes (RGESN 6.3)
- 🛠️ KPI : score accessibilité Lighthouse > 90
- 📅 Tag roadmap : M4
- 🔻 Priorité : **Basse** — non identifiée comme problème critique lors de l'audit

---

### Story 4 : Réduction des requêtes réseau

**En tant que** utilisateur de l'application,  
**je veux** que la page n'envoie pas de requêtes inutiles en continu  
**afin de** réduire la consommation de données et l'impact environnemental.

- 🎯 Objectif : nombre de requêtes < 50 au chargement
- 🧱 BP associée : supprimer les appels réseau inutiles
- 🛠️ KPI : nombre de requêtes mesuré avec GreenIT Analysis
- 📅 Tag roadmap : M1
- 🔺 Priorité : **Critique** — 1472 requêtes observées lors de l'audit, nombre croissant

---
