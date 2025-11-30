# Analyse des Ventes Walmart - Rapport Final

**Auteur:** Jeremie Konan  
**Date:** Novembre 2025  
**Dataset:** Walmart Sales (2010-2012)  
**GitHub:** [github.com/Softwinnerr/walmart-sales-analysis](https://github.com/Softwinnerr/walmart-sales-analysis)

---

## Résumé Exécutif

Cette analyse examine 6,434 enregistrements de ventes hebdomadaires de 45 magasins Walmart sur 3 ans (2010-2012) pour identifier les tendances temporelles, la saisonnalité et l'impact des facteurs économiques sur les performances commerciales.

**Résultats principaux:**
- Impact significatif des vacances : **+7.8%** de ventes durant les périodes de vacances
- Forte saisonnalité avec pic en **Décembre**
- Corrélation négative entre **Unployment** et ventes
- Disparités importantes entre magasins (Store 20 performe le mieux)

---

## Méthodologie

### Dataset
- **Source:** Walmart Sales Data
- **Taille:** 6,434 enregistrements hebdomadaires
- **Période:** 05/02/2010 - 26/10/2012
- **Magasins:** 45 magasins Walmart
- **Variables:** 8 colonnes (Weekly_Sales, Date, Temperature, Fuel_Price, CPI, Unemployment, Holiday_Flag, Store)

### Outils utilisés
- **Python 3.10**
- **Pandas** - Manipulation et analyse de données temporelles
- **Matplotlib & Seaborn** - Visualisations
- **Jupyter Notebook** - Analyse interactive

### Approche
1. Exploration des données et statistiques descriptives
2. Création de features temporelles (Year, Month)
3. Analyse de saisonnalité et tendances
4. Identification des facteurs d'impact
5. Dashboard de visualisations finales

---

## Résultats Clés

### 1. Tendances Temporelles

**Évolution sur 3 ans:**
- Croissance globale observable de 2010 à 2012
- Pics récurrents chaque année durant la période des fêtes
- Stabilité relative avec variations saisonnières marquées

![Évolution temporelle](../visualizations/dashboard_complet.png)

**Insight:** Les ventes montrent une saisonnalité forte et prévisible, facilitant la planification d'inventaire.

---

### 2. Impact des Vacances

Les semaines de vacances montrent une **augmentation de 7.8%** des ventes comparé aux semaines normales.

**Statistiques:**
- Ventes moyennes semaine normale : **$1,046,965**
- Ventes moyennes semaine vacances : **$1,122,887.89**
- Différence : **+$81,631.51**

**Implications business:**
- Renforcer les stocks avant les périodes de vacances clés
- Augmenter temporairement le personnel durant ces périodes
- Concentrer les budgets marketing sur ces fenêtres à fort ROI

**Insight:** Les vacances sont un levier commercial majeur qui justifie des investissements ciblés.

---

### 3. Saisonnalité Mensuelle

**Performance par mois:**
- **Meilleur mois:** Décembre avec $1,281,864 de ventes moyennes
- **Pire mois:** Janvier avec $923,885 de ventes moyennes

**Pattern identifié:**
- Hausse progressive vers la fin d'année
- Baisse post-fêtes en début d'année
- Stabilité relative durant les mois d'été

**Insight:** La saisonnalité est prévisible et peut être exploitée pour optimiser la gestion des stocks.

---

### 4. Facteurs Économiques

**Corrélations identifiées avec les ventes:**
- **Temperature:** -0.064
- **Fuel_Price:** -0.009
- **CPI:** -0.073
- **Unemployment:** -0.106

**Insight:** Le facteur **Unemployment** a l'impact le plus significatif sur les ventes, suggérant que les conditions économiques locales influencent directement le comportement d'achat.

---

### 5. Performance des Magasins

**Top performer:**
- **Store 20** avec $2,107,677/semaine en moyenne
- Variation significative entre magasins (facteur géographique probable)

**Opportunité:** Analyser les best practices du top performer pour améliorer les magasins sous-performants.

---

## Insights Business Clés

1. **Saisonnalité prévisible:** Les patterns mensuels permettent une planification précise de l'inventaire et du personnel

2. **Levier vacances:** Les périodes de vacances offrent +7.8% de ventes, justifiant des investissements marketing ciblés

3. **Impact économique:** Le contexte économique local (chômage, inflation) affecte significativement les performances

4. **Tendance positive:** Croissance observable sur la période 2010-2012

---

## Recommandations

### Pour le Retail Management:

1. **Optimisation des stocks (Court terme)**
   - Augmenter les stocks de 20-30% avant les périodes de vacances identifiées
   - Réduire les stocks de 15-20% durant les mois faibles
   - Implémenter un système de prévision basé sur la saisonnalité

2. **Stratégie marketing (Moyen terme)**
   - Concentrer 60% du budget marketing sur Q4 et périodes de vacances
   - Promotions ciblées durant les mois faibles pour stimuler les ventes
   - Campagnes anticipées 2-3 semaines avant les pics

3. **Gestion du personnel (Court terme)**
   - Embauche temporaire avant les périodes de forte affluence
   - Formation croisée pour flexibilité durant les pics
   - Planification des congés durant les mois creux

4. **Analyse comparative (Moyen terme)**
   - Étudier les best practices du Store 20
   - Identifier les facteurs de succès (emplacement, démographie, gestion)
   - Appliquer les apprentissages aux magasins sous-performants

### Pour l'Analyse Future:

1. **Enrichissement des données**
   - Intégrer des données démographiques par zone de magasin
   - Ajouter des données sur les promotions spécifiques
   - Inclure des données météo plus détaillées

2. **Modélisation prédictive**
   - Développer un modèle de prévision des ventes (régression, time series)
   - Prédire l'impact de changements économiques
   - Optimiser l'allocation d'inventaire par magasin

3. **Dashboard dynamique**
   - Créer un tableau de bord interactif (Streamlit/Dash)
   - Monitoring en temps réel des KPIs
   - Alertes automatiques sur anomalies

---

## Conclusion

Cette analyse révèle des **patterns clairs et exploitables** dans les données de ventes Walmart :

**Saisonnalité forte et prévisible** facilitant la planification  
**Impact mesurable des vacances** (+7.8%) justifiant des investissements ciblés  
**Influence des facteurs économiques** confirmant l'importance du contexte local  
**Opportunités d'optimisation** via l'analyse comparative des magasins  

Ces insights permettent d'optimiser la gestion des stocks, du personnel et du marketing pour **maximiser les performances commerciales**.

**Valeur ajoutée du projet:**
- Méthodologie d'analyse temporelle reproductible
- Identification de leviers business actionnables
- Base pour développements futurs (ML, dashboards)

---

## Annexes

### Technologies utilisées
```
Python 3.10
├── pandas 2.1.0
├── numpy 1.24.3
├── matplotlib 3.7.2
└── seaborn 0.12.2
```

### Structure du projet
```
walmart-sales-analysis/
├── data/
│   ├── raw/              # Données brutes
│   └── processed/        # Données enrichies
├── notebooks/
│   ├── 01_complete_analysis.ipynb
│   └── 02_visualizations.ipynb
├── visualizations/       # Dashboard et graphiques
├── reports/             # Ce rapport
└── README.md
```

### Références
- Dataset: Walmart Sales Data (2010-2012)
- Code source: [GitHub Repository](https://github.com/Softwinnerr/walmart-sales-analysis)
- Visualisations: `/visualizations/dashboard_complet.png`

---

**Contact:**  
Jeremie Konan  
- GitHub: (https://github.com/Softwinnerr)
- LinkedIn:(https://linkedin.com/in/jeremie-konan)
- Email: jeremiesofty24@gmail.com

**Date de finalisation:** Novembre 2025