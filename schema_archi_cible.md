# Schéma d’architecture cible

```mermaid
flowchart TD
    DEC[Décisions internes] --> EDA[EDA et analyse de la qualité des documents]
    REG[Registre des décisions CSV] --> EDA_CSV[EDA et analyse des données]
    COUR[Courriers archivés] --> EDA
    MOD[Modèles de courriers] --> EDA
    COL[Connaissances des collègues] --> COLLECT[Collecte, documentation et mise au propre des données]
    COLLECT --> EDA_CSV
    EDA_CSV --> PREP_INDEX[Préparation]
    EDA --> SCAN{Document scanné ?}
    SCAN -->|Oui| OCR[OCR et vérification du texte extrait]
    SCAN -->|Non| CONV[Conversion dans un format commun]
    OCR --> CONV
    CONV --> PREP_DOC[Préparation + anonymisation/pseudonymisation]
    PREP_INDEX --> ASSOC[Association des métadonnées aux documents]
    PREP_DOC --> ASSOC
    ASSOC --> PASS[Nettoyage du texte et découpage en passages avec métadonnées et lien vers le document original]
    PASS --> LEX[Index inversé : association des mots aux passages]
    PASS --> EMB[Modèle d’embeddings : transformation des passages en vecteurs de sens]
    EMB --> VEC[Index vectoriel : stockage des vecteurs des passages]
    LEX --> SEARCH[Moteur de recherche hybride : mots-clés et proximité de sens, filtres du registre]
    VEC --> SEARCH
    SEARCH --> UI[Interface interne : affichage des résultats classés, extraits et liens vers les documents originaux]
    UI --> REVIEW[Vérification humaine]
    REVIEW --> MON[Suivi du temps de recherche et de la pertinence]
    SEARCH --> LOG[Journalisation des accès et des recherches]
    classDef risqueRouge fill:#ffe5e5,stroke:#c62828,stroke-width:2px;
    class PREP_DOC,UI,REVIEW,LOG risqueRouge;
```

--- 

- **Confidentialité** : anonymisation/pseudonymisation lors de la préparation, interface réservée aux employés et journalisation des accès et des recherches.
- **Résultats erronés** : extraits et liens vers les documents originaux dans l’interface, puis vérification humaine complète.

**Composants** : préparation des données, OCR, index textuel et vectoriel, modèle d’embeddings, moteur de recherche hybride, interface interne, revue humaine, suivi et journalisation.

**Ce qu’on n’a PAS mis (et pourquoi)** : LLM génératif et RAG (exactitude non garantie), base juridique publique (priorité à la recherche interne, les données publiques ont probablement déjà un système de recherche).
