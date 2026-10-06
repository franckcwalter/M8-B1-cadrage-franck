# M8-B1 — Cadrage d’une recherche documentaire pour le cabinet Maître Devalle

Cadrage d’une solution de recherche documentaire pour un cabinet de 12 avocats à
Bordeaux. Le besoin principal est de retrouver une décision interne déjà obtenue
ou étudiée en 30 secondes, contre 30 minutes actuellement.

Le projet examine les données disponibles, les risques, l’architecture cible et
les indicateurs de réussite. Le budget annoncé est de 15 000 € au démarrage et de
quelques centaines d’euros par mois, avec un horizon de six mois privilégiant la
fiabilité.

## Documents

Le [document de cadrage](./document_cadrage.md) rassemble la synthèse, le besoin
métier, les données, les risques et la conformité, la solution proposée et les KPI.

| Document | Contenu |
|---|---|
| [Notes d’entretien](./notes_entretien.md) | Questions, réponses du client, interprétations et questions ouvertes |
| [Schéma d’architecture cible](./schema_archi_cible.md) | Préparation des données, recherche hybride, interface interne et traitements des risques |
| [Extrait du registre](./cas_A_registre_decisions_sample.csv) | 20 décisions décrites par six colonnes |
| [Ressources](./ressources/README.md) | Mini-cours et références utilisés pour le cadrage |

## Solution proposée

Un moteur de recherche interne combine les mots-clés, la proximité de sens et les
filtres du registre : date, matière, juridiction et issue. Les résultats affichent
des extraits et des liens vers les documents originaux pour vérification humaine.

La préparation prévoit l’analyse de qualité, l’OCR des scans, la conversion dans
un format commun et l’anonymisation ou la pseudonymisation. Le texte et les
métadonnées alimentent un index textuel et un index vectoriel.

La génération de documents juridiques par LLM est écartée dans un premier temps,
compte tenu de l’exactitude non garantie et des risques de confidentialité.

L’hébergement interne est privilégié. Le départ du prestataire informatique au
31 décembre conduit à envisager également un cloud administré, sous réserve des
garanties de confidentialité et du budget.

## Indicateurs proposés

| Indicateur | Cible | Seuil d’acceptabilité |
|---|---|---|
| Temps de recherche | 30 secondes | Quelques minutes |
| Précision des résultats | 75 % | 50 % |
| Rappel des documents pertinents | 95 % | 80 % |

Ces objectifs seront évalués lors de tests avec les employés du cabinet.

## Périmètre

Le dépôt contient les livrables de cadrage. Le choix des technologies et des
modèles, la réalisation du prototype et les tests font partie des prochaines étapes.
Seul un extrait du registre a été transmis ; aucune décision ni aucun courrier
n’a été examiné.

## Structure du dépôt

```text
.
├── document_cadrage.md                  # Livrable principal
├── notes_entretien.md                  # Entretien et questions ouvertes
├── schema_archi_cible.md                # Architecture proposée en Mermaid
├── cas_A_registre_decisions_sample.csv  # Extrait transmis par le client
├── ressources/                         # Mini-cours et références
└── README.md
```
