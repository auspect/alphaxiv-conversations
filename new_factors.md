Pour approfondir l'approche de "Taming the factor zoo" (2020), qui utilisait une pénalisation de type LASSO pour filtrer les facteurs, les recherches récentes s'orientent vers l'automatisation de la découverte via des agents autonomes et l'exploration des interactions d'ordre supérieur.

### Ressources et Papiers Récents

Voici une sélection de travaux récents qui proposent des cadres méthodologiques pour gérer ou étendre le "zoo des facteurs" :

| Papier | Approche Clé | Accessibilité / Code |
| :--- | :--- | :--- |
| [FactorMiner: A Self-Evolving Agent...](https://arxiv.org/abs/2602.14670) | Utilise un agent avec mémoire pour découvrir de nouveaux facteurs alpha de manière autonome. | Focus sur la scalabilité pratique de la découverte. |
| [Higher-Order Asset Pricing Factors...](https://arxiv.org/abs/2503.23501) | Propose une procédure **Forward Selection Fama-MacBeth** (FS-FMB) pour identifier les interactions entre facteurs. | Méthodologie détaillée pour classer l'importance des facteurs. |
| [The Co-Pricing Factor Zoo](https://arxiv.org/abs/2604.04430) | Utilise le **Bayesian Model Averaging** pour agréger des douzaines de facteurs dans un SDF persistant. | Analyse jointe des actions et des obligations d'entreprises. |

---

### Analyse des Approches Modernes

#### 1. Automatisation via des Agents (LLM/RL)
Le papier **FactorMiner** représente une évolution majeure. Contrairement aux méthodes statistiques classiques de sélection (comme LASSO), il utilise un agent capable d'apprendre de ses succès et échecs passés pour explorer l'espace des facteurs.
> "FactorMiner uses a self-evolving agent with memory to navigate this space, aiming to construct a diverse library of high-quality factors with low redundancy." [FactorMiner Overview](https://alphaxiv.org/abs/2602.14670v1?page=1)

#### 2. Interactions d'Ordre Supérieur
Plutôt que de se limiter à des facteurs linéaires, le travail sur les **Higher-Order Asset Pricing Factors** suggère que le pouvoir prédictif de nombreux facteurs existants provient en réalité de leur exposition à des termes non linéaires (interactions et puissances).
- La méthode **FS-FMB** permet de sélectionner itérativement les termes qui maximisent le $R^2$ dans les régressions cross-sectionnelles. [FS-FMB Method](https://alphaxiv.org/abs/2503.23501v2?page=1)

### Ressources Complémentaires (Code & Implémentation)
Pour une mise en pratique directe de l'idée originale de "Taming the Factor Zoo" :
- **Bibliothèque `factor-zoo` (GitHub)** : Bien que non officielle, plusieurs implémentations communautaires sur GitHub reprennent les méthodes de sélection de facteurs par régression pénalisée.
- **Dacheng Xiu's Website** : L'un des auteurs du papier original partage souvent des codes et des données sur sa [page académique](https://dachxiu.chicagobooth.edu/), notamment sur l'économétrie des facteurs à haute dimension.