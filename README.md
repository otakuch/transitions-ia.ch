# transitions-ia.ch

**Observatoire de l'exposition professionnelle à l'IA en Suisse**  
Snapshot mars 2026 · 84 métiers · 19 catégories

🔗 **[transitions-ia.ch](https://transitions-ia.ch)** · par [Naully Nicolas](https://naullynicolas.ch)

---

## À propos

Tableau de bord interactif mesurant l'**exposition des tâches professionnelles à l'IA générative** pour 84 métiers représentatifs du marché du travail suisse.

Le score d'exposition (0–10) mesure la **proportion des tâches d'un métier** que l'IA générative pourrait théoriquement effectuer — pas la probabilité de suppression d'emplois. L'exposition précède la transformation ; elle ne la détermine pas.

### Spécificités suisses
- Salaires en **CHF** (ESS 2022 · OFS)
- Effectifs **ESPA 2024** (OFS)
- **Facteur réglementaire** : FINMA, LPMéd, LaMal, LLCA, CPP, nLPD, AI Act…
- Quadrilinguisme institutionnel : interface **FR / DE / IT**
- Sources : ILO WP140 (OIT/NASK 2025) · Anthropic Economic Index 2026 · KOF EPFZ · SECO · Avenir Suisse · BIS WP 1239

---

## Structure

```
transitions-ia-ch/
├── index.html        ← Application complète (standalone, ~300 KB)
├── README.md
├── LICENSE
└── .gitignore
```

L'application est **100 % standalone** : un seul fichier HTML, aucune dépendance serveur, aucune base de données. Fonctionne hors-ligne.

### Dépendances CDN (chargées à la demande)
- [D3.js v7](https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js) — visualisation Treemap
- Google Fonts — Syne · Inter · IBM Plex Mono

---

## Fonctionnalités

| Onglet | Contenu |
|--------|---------|
| **À propos** | Contexte suisse, KPIs, méthodologie |
| **Exposition des tâches** | Treemap D3 interactif · filtres domaine/score · liste |
| **Exposition → Emploi** | Chronologie académique 2022–2026 |
| **Prédictions** | Modèles de projection par scénario |
| **Productivité & IA** | Études de productivité augmentée |
| **Usage IA Suisse** | Données d'adoption CH (OFS ICT 2024) |
| **Méthodologie** | Scoring T1–T4, facteur réglementaire, sources |

### Scoring multi-sources
```
Score pondéré = T1×4 + T2×2 + T3×1 + T4×0.5  (recency-weighted)
Score net     = Score brut × (1 − reg.score/10 × 0.35)  [si effet Protecteur]
```

### Catégories (19)
Agriculture · Arts & Culture · Banque & Assurances · BTP & Architecture · Commerce · Communication · Droit & Conseil · Droit & Justice · Éducation & Formation · Gestion & Finance · Hôtellerie & Tourisme · Industrie & Fabrication · IT & Numérique · Maintenance & Automatisation · Médias & Audiovisuel · Santé · Services à la personne · Spectacle & Musique · Transport & Logistique

---

## Déploiement GitHub Pages

```bash
# 1. Cloner ou forker ce dépôt
git clone https://github.com/<votre-username>/transitions-ia-ch.git
cd transitions-ia-ch

# 2. Activer GitHub Pages
#    Settings → Pages → Source: Deploy from branch → main → / (root)

# 3. Accéder à l'application
#    https://<votre-username>.github.io/transitions-ia-ch/
```

> **Domaine personnalisé** : créez un fichier `CNAME` à la racine avec `transitions-ia.ch`

---

## Sources principales

| Source | Type | Année |
|--------|------|-------|
| [ILO Working Paper 140](https://www.ilo.org/publications/generative-ai-and-jobs-refined-global-index-occupational-exposure) — Gmyrek, Berg et al. | T1 | 2025 |
| [Anthropic Economic Index](https://www.anthropic.com/research/labor-market-impacts) — Massenkoff & McCrory | T1 | 2026 |
| [Eloundou et al. — GPTs are GPTs](https://arxiv.org/abs/2303.10130) | T1 | 2023 |
| [BIS Working Paper 1239](https://www.bis.org/publ/work1239.htm) | T1 | 2025 |
| ESPA 2024 · ESS 2022 · NP 2010 — OFS Suisse | T2 | 2024 |
| KOF EPFZ · SECO · Avenir Suisse | T2 | 2024 |

---

## Licence

**Licence Ouverte v2.0** (Etalab) — réutilisation libre avec attribution.

> Auteur : Naully Nicolas · [naullynicolas.ch](https://naullynicolas.ch) · [sayhi@naullynicolas.ch](mailto:sayhi@naullynicolas.ch)  
> Livre : [Guerill-iA](https://www.fnac.com) — disponible sur Fnac
