# Métadonnées - Hôpital C

Ce document décrit l'ensemble des 18 colonnes présentes dans le jeu de données `hopital_C.csv`.

| Colonne | Définition | Format / Unité / Modalités observées |
| :--- | :--- | :--- |
| `id_patient` | Identifiant unique du patient | Chaîne de caractères (ex: `P100010`) |
| `date_entree` | Date d'admission à l'hôpital | Date (Format `AAAA/MM/JJ`, ex: `2025/12/02`) |
| `date_sortie` | Date de sortie de l'hôpital | Date (Format `AAAA/MM/JJ`, ex: `2025/12/05`) |
| `age` | Âge du patient | Nombre entier (en années) |
| `sexe` | Sexe du patient | `F`, `H`, `Homme` |
| `poids` | Poids du patient | Nombre flottant en **kg** (ex: `75.7` kg) |
| `taille` | Taille du patient | Nombre flottant principalement en **cm** (ex: `169.0` cm). contient quelques valeurs saisies en **mètres** (ex: `1.84` m) |
| `tabac` | Statut tabagique | `NON`, `OUI` |
| `diabete` | Diagnostic de diabète | Numeric `0.0` (Non), `1.0` (Oui) |
| `hta` | Diagnostic d'hypertension artérielle | Numeric `0.0` (Non), `1.0` (Oui) |
| `reanimation` | Passage en réanimation / soins intensifs | Numeric `0.0` (Non), `1.0` (Oui) |
| `duree` | Durée de séjour à l'hôpital | Nombre flottant (en jours, ex: `5.0`) |
| `rehosp_30j` | Réhospitalisation dans les 30 jours | Numeric `0.0` (Non), `1.0` (Oui) |
| `deces` | Décès à l'hôpital | Numeric `0.0` (Non), `1.0` (Oui) |
| `diag` | Diagnostic principal à la sortie | Codes CIM-10 / Libellés (ex: `HTA`, `E11`, `E11/HTA`) |
| `pas` | Pression artérielle systolique (*PAS*) | Nombre flottant en **mmHg** (contient des valeurs physiques aberrantes: `35.0` mmHg) |
| `creatininémie` | Taux de créatinine sérique | Nombre flottant en **mg/dL** (ex: `1.05`) |
| `CRP` | Taux de protéine C-réactive | Nombre flottant en **mg/L** (ex: `18.3`) |

