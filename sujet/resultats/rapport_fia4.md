# TP FIA4 — Harmonisation et qualité des données de santé

## 1. Objectif et sources
Les trois fichiers hospitaliers synthétiques A, B et C ont été harmonisés pour étudier descriptivement la réhospitalisation à 30 jours. Les données sont pédagogiques et ne représentent pas des patients réels.

Effectif combiné : **10000 lignes**. Les effectifs par hôpital sont : {"A": 3925, "B": 3497, "C": 2578}.

## 2. Nettoyage et harmonisation
- Noms de variables harmonisés vers un schéma commun.
- Dates parsées en dates standard; les dates manquantes ou les sorties antérieures à l'admission sont invalidées.
- Poids du fichier B convertis de livres en kg; tailles converties en cm lorsque l'unité source l'indique ou selon la règle documentée pour C.
- Sexe harmonisé en M/F; variables binaires harmonisées en 0/1. Les modalités inconnues deviennent manquantes.
- Valeurs hors des plages de contrôle documentées dans le notebook mises en NA, sans imputation arbitraire.
- Durée de séjour recalculée à partir des dates; durée source conservée séparément.
- Identifiants répétés signalés, sans suppression automatique.
- Diagnostic source conservé; les codes ou libellés repérés peuvent compléter diabète/HTA seulement si l'indicateur dédié manque.
- Les valeurs manquantes restent NA; le profil détaillé est dans `profil_qualite.csv`.

Valeurs hors bornes mises en manquantes : {"age_years": 0, "weight_kg": 5, "height_cm": 0, "sbp_mmhg": 30, "creatinine_mg_dl": 0, "crp_mg_l": 0, "los_reported_days": 0}. Dates incohérentes ou manquantes : 2526.

## 3. Schéma cible et fiabilité
Le dictionnaire est fourni dans `schema_cible.csv`. Les variables binaires, l'âge, le sexe et les dates peuvent être exploités après vérification des taux de manquants et de la cohérence par établissement. Le diagnostic reste hétérogène. La durée calculée dépend de la qualité des dates. La variable `readmit30` est reprise de la source; sa définition opérationnelle et l'exhaustivité du suivi ne peuvent pas être validées à partir des seuls CSV.

## 4. Analyse descriptive
- Issues de réhospitalisation renseignées : **9603**.
- Taux global observé : **8.38%** si estimable.
- Taux par hôpital : {"A": {"n": 3816, "taux_pct": 8.31}, "B": {"n": 3357, "taux_pct": 8.91}, "C": {"n": 2430, "taux_pct": 7.78}}.
- Taux selon diabète (0 = non, 1 = oui) : {"0": {"n": 7603, "readmissions": 612, "taux_pct": 8.05}, "1": {"n": 2000, "readmissions": 193, "taux_pct": 9.65}}.
- Durée selon réhospitalisation : {"0": {"n": 6596, "moyenne_jours": 12.12, "mediane_jours": 4.0}, "1": {"n": 614, "moyenne_jours": 9.78, "mediane_jours": 4.0}}.
- Modèle logistique exploratoire : {"n_cas_complets": 6501, "odds_ratios": {"const": 0.106, "age_years": 0.997, "diabetes": 1.205, "los_days": 0.997, "sex_M": 1.043, "icu": 1.064}, "IC95_OR": {"const": [0.075, 0.148], "age_years": [0.992, 1.002], "diabetes": [0.98, 1.482], "los_days": [0.994, 1.001], "sex_M": [0.875, 1.243], "icu": [0.805, 1.408]}, "p_values": {"const": 0.0, "age_years": 0.24885, "diabetes": 0.07693, "los_days": 0.13844, "sex_M": 0.63955, "icu": 0.66175}, "note": "OR ajustés exploratoires sur cas complets; modèle non causal et potentiellement limité par les données manquantes."}.

Ces résultats sont des associations descriptives, pas des effets causaux. Le modèle ne porte que sur les cas complets et peut être biaisé si les données manquent de façon non aléatoire.

## 5. Limites et conclusion
Les hôpitaux peuvent différer par les populations prises en charge, les périodes, les codages et les définitions de la réhospitalisation. Les différences observées peuvent donc refléter des effets de structure. Avant toute conclusion confirmatoire, il faudrait valider les définitions avec les établissements, vérifier les doublons et documenter les mécanismes de données manquantes. Aucune généralisation clinique ne doit être faite à partir de ces données synthétiques.
