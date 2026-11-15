# Métadonnées - Hôpital A

Ce document décrit l'ensemble des 18 colonnes présentes dans le jeu de données `hopital_A.csv`.

| Colonne | Définition | Format / Unité / Modalités observées |
| :--- | :--- | :--- |
| `id` | Identifiant unique du patient | Chaîne de caractères (ex: `P100000`) |
| `date_adm` | Date d'admission à l'hôpital | Date (Format ISO `AAAA-MM-JJ`, ex: `2025-07-10`) |
| `date_dis` | Date de sortie de l'hôpital | Date (Format ISO `AAAA-MM-JJ`, ex: `2025-07-13`) |
| `age` | Âge du patient | Nombre entier (en années) |
| `gender` | Sexe du patient | `M`, `F`, `Male` |
| `weight` | Poids du patient | Nombre flottant en **kg** (ex: `76.5` kg) |
| `height_m` | Taille du patient | Nombre flottant en **mètres** (ex: `1.73` m) |
| `smoker` | Statut tabagique | `no`, `yes` |
| `diabetes` | Diagnostic de diabète | `no`, `yes` |
| `hypertension` | Diagnostic d'hypertension artérielle | `no`, `yes` |
| `icu` | Passage en réanimation / soins intensifs | `0.0` (Non), `1.0` (Oui) |
| `los` | Durée de séjour (*Length of Stay*) | Nombre flottant (en jours, ex: `3.2`) |
| `readmit30` | Réhospitalisation dans les 30 jours | `0.0` (Non), `1.0` (Oui) |
| `death` | Décès à l'hôpital | `0.0` (Non), `1.0` (Oui) |
| `diag` | Diagnostic principal à la sortie | Codes CIM-10 (ex: `I10`, `E11.9`, `E11.9+I10`) |
| `sbp` | Pression artérielle systolique | Nombre flottant en **mmHg** |
| `creatinine` | Taux de créatinine sérique | Nombre flottant en **mg/dL** (ex: `1.05`) |
| `crp` | Taux de protéine C-réactive | Nombre flottant en **mg/L** (ex: `17.8`) |

