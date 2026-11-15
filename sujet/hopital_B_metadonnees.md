# Métadonnées - Hôpital B

Ce document décrit l'ensemble des 18 colonnes présentes dans le jeu de données `hopital_B.csv`.

| Colonne | Définition | Format / Unité / Modalités observées |
| :--- | :--- | :--- |
| `patient` | Identifiant unique du patient | Chaîne de caractères (ex: `P100002`) |
| `admit` | Date d'admission à l'hôpital | Date (Format français `JJ/MM/AAAA`, ex: `22/01/2025`) |
| `discharge` | Date de sortie de l'hôpital | Date (Format français `JJ/MM/AAAA`, ex: `27/01/2025`) |
| `age` | Âge du patient | Nombre entier (en années, min: 18, max: 95) |
| `gender` | Sexe du patient | `Male`, `Female`, `M` |
| `weight_lb` | Poids du patient | Nombre flottant en **livres** (*pounds*, lb, ex: `167.2` lb) |
| `height_cm` | Taille du patient | Nombre flottant en **centimètres** (ex: `170.0` cm) |
| `smoking` | Statut tabagique | `N` (No), `Y` (Yes) |
| `diab` | Diagnostic de diabète | Numeric `0.0` (Non), `1.0` (Oui) |
| `htn` | Diagnostic d'hypertension artérielle | Numeric `0.0` (Non), `1.0` (Oui) |
| `icu` | Passage en réanimation / soins intensifs | Numeric `0.0` (Non), `1.0` (Oui) |
| `stay_days` | Durée de séjour à l'hôpital | Nombre flottant (en jours, ex: `5.0`) |
| `readmission` | Réhospitalisation dans les 30 jours | Numeric `0.0` (Non), `1.0` (Oui) |
| `mortality` | Décès à l'hôpital | Numeric `0.0` (Non), `1.0` (Oui) |
| `diagnosis` | Diagnostic principal à la sortie | Libellés abrégés / codes (ex: `HTA`, `DM2`, `DM2|HTA`) |
| `blood_pressure` | Pression artérielle systolique | Nombre flottant en **mmHg** |
| `creat` | Taux de créatinine sérique | Nombre flottant en **mg/dL** (ex: `1.05`) |
| `CRP` | Taux de protéine C-réactive | Nombre flottant en **mg/L** (ex: `18.1`) |

