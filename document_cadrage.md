# Document de cadrage


## 1. Synthèse exécutive (5-6 lignes — rédigée EN DERNIER)
Le cabinet souhaite retrouver ses décisions internes en 30 secondes, contre 30 minutes actuellement.  
La solution proposée est un moteur de recherche interne combinant mots-clés, proximité de sens et filtres du registre.  
Les résultats donnent accès aux extraits et aux documents originaux pour vérification humaine.  
La génération de documents par LLM est écartée dans un premier temps. La confidentialité guide la préparation des données et le choix d’hébergement.  
Les cibles sont de 30 secondes par recherche, 75 % de précision et 95 % de rappel.  
Le projet dispose de 15 000 € au démarrage et de quelques centaines d’euros par mois, avec un horizon de six mois privilégiant la fiabilité.

> **Imprévu client** : Le prestataire informatique arrête son contrat au 31 décembre, ce qui fragilise la maintenance du serveur interne. La section 5 a été complétée avec une option d’hébergement cloud administré et les garanties de confidentialité à vérifier.

## 2. Besoin métier et contexte

Besoin exprimé initialement :  
> « On rédige beaucoup de courriers types (mise en demeure, transmission dossier). On voudrait un assistant pour aller plus vite, et aussi pour retrouver les bonnes jurisprudences en 30 secondes au lieu de 30 minutes. »

Besoin reformulé après entretien :   
Le besoin principal du client est de passer de 30 minutes à 30 secondes pour retrouver une décision de jurisprudence interne déjà obtenue ou étudiée, tout en obtenant des résultats fiables, sourcés et vérifiables.
Le besoin secondaire est de réduire le temps de rédaction des documents juridiques, sans objectif chiffré précisé par le client. 

Contraintes relevées en entretien :  
La solution est destinée à un usage interne par les 12 avocats et leurs assistants et assistantes. Le budget de démarrage est de 15 000 €, avec quelques centaines d’euros par mois pour la maintenance, la gestion et l’évolution. La confidentialité est essentielle compte tenu des données personnelles et potentiellement sensibles présentes dans les dossiers, les décisions internes n'étant pas anonymisées.

## 3. Données 

| Donnée existante | À obtenir | À préparer | Volume et qualité estimée | Données personnelles et accès |
|---|---|---|---|---|
| **Décisions internes** sur le serveur du cabinet | <ul><li>Ensemble des décisions internes du cabinet.</li><li>À défaut, un extrait de décisions anonymisées si le cabinet ne souhaite pas partager des documents trop sensibles.</li></ul> | Convertir les PDF, les documents Word et les scans dans un **format texte commun** (pour les scans, vérifier la qualité du texte après extraction). | <ul><li>**Environ 2 000 décisions sur 15 ans**, en PDF ou Word.</li><li>Anciens scans parfois peu lisibles.</li><li>**Qualité à évaluer** (aucun document examiné).</li></ul> | <ul><li>**Non anonymisées**.</li><li>Clients, parties adverses, salariés et enfants concernés.</li><li>**Nature exacte des données personnelles et sensibles à préciser** (documents non transmis).</li></ul> |
| **Registre des décisions**, tenu par une assistante | Le registre complet. | <ul><li>Vérifier la **qualité des données** (précision, complétude, cohérence).</li><li>Vérifier la **correspondance avec les documents existants**.</li></ul> | <ul><li>Extrait CSV de **20 lignes et 6 colonnes**.</li><li>Aucune cellule vide apparente.</li><li>Qualité du registre complet inconnue.</li></ul> | <ul><li>Aucune donnée directement nominative visible dans l’extrait.</li><li>Accès aux décisions associées à préciser.</li></ul> |
| **Courriers archivés** dans les dossiers clients | <ul><li>Ensemble des courriers ou, à défaut, des extraits pour observer leur format.</li><li>Informations sur le format de tous les courriers.</li><li>Précisions sur les modalités d’archivage.</li></ul> | <ul><li>Examiner les documents reçus.</li><li>Selon les formats reçus et le traitement retenu, convertir les courriers dans un **format commun** pour permettre leur exploitation.</li></ul> | <ul><li>**Des milliers de courriers**, sans nombre précis.</li><li>Qualité non évaluée.</li></ul> | <ul><li>Données personnelles présentes dans les dossiers.</li><li>Aucun courrier transmis.</li></ul> |
| **Modèles de courriers** individuels et dossier partagé | Ensemble des modèles individuels et partagés à consulter si possible ou, à défaut, un extrait. | <ul><li>Selon le traitement retenu, convertir les modèles dans un **format commun** si nécessaire.</li><li>Demander au métier d’actualiser les modèles ou de transmettre uniquement les modèles pertinents.</li></ul> | <ul><li>Dossier partagé datant de **2019**, non actualisé.</li><li>Volume et qualité des modèles individuels non évalués.</li></ul> | <ul><li>Présence de données personnelles à vérifier avant réutilisation.</li><li>Modèles individuels sur les postes des avocats.</li></ul> |
| **Base juridique publique en ligne** | <ul><li>Conditions d’accès et d’utilisation de la base.</li><li>Modalités techniques d’accès à la base pour son intégration à la solution.</li></ul> | Définir l’**architecture d’intégration de la base à la solution**. | <ul><li>Abonnement existant.</li><li>**Qualité présumée bonne, à vérifier**.</li><li>Volume et couverture non évalués.</li><li>**Formats inconnus**.</li></ul> | <ul><li>Décisions publiques **anonymisées**, selon le client.</li><li>Accès par abonnement.</li></ul> |
| **Connaissances détenues par les collègues** | Informations utiles détenues par les collègues. | <ul><li>Définir un **processus de collecte et de documentation** des informations détenues par les collègues.</li><li>Étudier la possibilité de les **rassembler dans une base de données**.</li></ul> | **Volume et qualité inconnus** (informations non matérialisées). | Collecte et confidentialité à préciser. |

## 4. Risques et conformité — mini-cours `04` et `07`

**Usage réel**  :  
Les sorties sont utilisées en interne par les employés du cabinet, principalement les assistants et assistantes, ainsi que les avocats.  
Elles servent à rechercher des décisions de jurisprudence et pourraient permettre de générer un document juridique.  
Toute sortie doit être relue et vérifiée par les employés, qui peuvent la corriger ou la rejeter ; tout document juridique doit être validé par l’avocat, dont la responsabilité est engagée.

**Qualification AI Act** : 

La recherche documentaire interne au cabinet ne relève pas du cas à haut risque de l’annexe III, point 8 a.

Si la solution génère des courriers à valeur juridique (mises en demeure, transmissions de dossiers) en analysant les faits et le droit et en appliquant le droit à une situation concrète, elle pourrait être classée **à haut risque**, à condition d’être utilisée par une autorité judiciaire ou pour son compte, ou de manière similaire dans le règlement extrajudiciaire d’un litige. Cette classification entraînerait des obligations renforcées, selon le rôle du cabinet : gestion des risques, documentation, traçabilité, contrôle humain, exactitude, robustesse et cybersécurité.

**RGPD** :

| Risque (éthique, métier, conformité) | 🔴/🟠/🟡/⚪ | Obligation ou raison | Traitement dans l'archi |
|---|---|---|---|
| Profilage | ⚪ | Aucun profilage : la recherche documentaire et la préparation de courriers ne visent pas à évaluer automatiquement les caractéristiques personnelles des personnes. | / |
| Décision automatique | 🟡 | Les sorties ne s’apparentent pas à des décisions et font toujours l’objet d’une relecture humaine. | Relecture a posteriori complète de chaque sortie. |
| Utilisation de données personnelles | 🟠 | Définir et justifier une base légale au titre de l’article 6 du RGPD : intérêt légitime lié à l’activité du cabinet envisagé. Le contrat avec les clients ne couvre pas automatiquement les données des parties adverses ou de leur famille. | EDA pour identifier les données personnelles ; minimisation si possible (ne traiter que les données nécessaires à la recherche et à la préparation des courriers) ; étudier l’anonymisation ou la pseudonymisation ; utilisation réservée aux employés du cabinet. |
| Utilisation de données sensibles | 🟠 | Présence à vérifier. En complément de la base légale de l’article 6, piste à justifier : article 9(2)(f) du RGPD si le traitement est nécessaire à la constatation, à l’exercice ou à la défense d’un droit en justice. Vérifier que la réutilisation des dossiers pour la recherche et la préparation de courriers remplit cette condition. | EDA pour identifier les données sensibles ; minimisation si possible (ne traiter que les données nécessaires à la recherche et à la préparation des courriers) ; étudier l’anonymisation ou la pseudonymisation ; utilisation réservée aux employés du cabinet. |
| Documents anciens ou mal extraits | 🟠 | Les modèles de 2019 et les scans parfois peu lisibles peuvent produire des résultats inadaptés. | Vérifier l’extraction du texte et faire valider les modèles de courriers par les avocats. |
| Résultats erronés ou jurisprudences inventées | 🔴 | Une erreur dans un courrier ou une jurisprudence inventée engage la responsabilité professionnelle de l’avocat. | Sources consultables et vérification humaine complète ; si génération, vérifier chaque référence. |
| Divulgation d’informations confidentielles | 🔴 | Respect du secret professionnel et protection des dossiers non anonymisés. | Utilisation interne ; traitement à préciser selon l’hébergement et les éventuels prestataires retenus. |

**Sécurité du modèle**

| Menace | Plausibilité sur CE cas | Mitigation proposée | Risque résiduel |
|---|---|---|---|
| Injection de prompt | <ul><li>Plausible si un LLM est utilisé : instructions malveillantes dans une requête ou un document consulté.</li></ul> | <ul><li>Séparer les instructions du contenu documentaire.</li><li>Contrôler les entrées.</li><li>Relecture humaine complète des sorties.</li></ul> | <ul><li>Une instruction malveillante peut contourner les protections et fausser la sortie ou provoquer une fuite d’informations.</li></ul> |
| Fuite de données sensibles | <ul><li>Plausible : les dossiers peuvent contenir des données sensibles.</li><li>Exposition réduite par l’utilisation interne.</li></ul> | <ul><li>Utilisation réservée aux employés du cabinet.</li><li>Sécuriser le système avec les dispositifs disponibles dans le SI existant.</li></ul> | <ul><li>Une compromission du système ou une divulgation par un employé reste possible.</li></ul> |

- **Entrées modifiées pour tromper le modèle** : faible plausibilité avec l’usage interne ; pour un LLM, les entrées malveillantes sont traitées dans la ligne injection de prompt.
- **Empoisonnement des données d’entraînement** : sans objet si aucun entraînement ou réentraînement n’est prévu.
- **Extraction du modèle** : faible plausibilité si l’accès reste interne, sans API publique permettant des interrogations massives.

## 5. Architecture cible et sobriété — mini-cours `05`

Deux besoins sont identifiés : la recherche documentaire et la génération de documents juridiques.

Pour la génération libre de texte, le LLM est la seule solution IA qui pourrait répondre à ce besoin. Il est écarté dans un premier temps : l’exactitude n’est pas garantie et l’accès aux données personnelles présente des risques de confidentialité, même en usage interne. Selon l’usage et les conditions applicables, une qualification à haut risque pourrait entraîner des obligations importantes ; une analyse complémentaire serait nécessaire.

L’architecture proposée se concentre donc sur la recherche documentaire. La solution retenue est un moteur de recherche hybride interne, combinant recherche par mots-clés et proximité de sens, avec les filtres du registre (date, matière, juridiction, issue) ; les résultats affichent des extraits et des liens vers les documents originaux pour vérification humaine (voir [schéma d’architecture cible](schema_archi_cible.md)).

La recherche limitée au registre ou aux mots-clés est écartée car elle exploite insuffisamment le sens des documents ; la recherche uniquement vectorielle est écartée pour conserver la recherche de termes exacts ; le RAG est écarté car il ajoute une génération de texte par LLM.

Un hébergement sur le serveur interne du cabinet est privilégié pour conserver la maîtrise des données. L’arrêt du contrat du prestataire fragilise toutefois cette option. Un hébergement cloud administré en France ou dans l’Union européenne est envisagé, avec maintenance et sauvegardes prises en charge. Ce choix nécessite de vérifier la confidentialité, les accès du prestataire, le chiffrement, les éventuels transferts hors UE et le contrat de sous-traitance, ainsi que sa compatibilité avec le budget mensuel.


## 6. Indicateurs, seuils, questions ouvertes — mini-cours `03`
| Indicateur | Cible | Seuil d'acceptabilité | Comment on le mesure |
|---|---|---|---|
| Temps passé à effectuer une recherche | 30 secondes | Quelques minutes | Tests chronométrés réalisés par les employés. |
| Précision des résultats | 75 % de documents pertinents | 50 % : les documents non pertinents peuvent être écartés facilement par les employés. | Lors des tests, les employés évaluent la pertinence des documents retournés ; calcul du nombre de documents pertinents divisé par le nombre de documents retournés. |
| Rappel des documents pertinents | 95 % | 80 % | Comparer les mêmes recherches avec la procédure actuelle et la solution pour identifier les documents pertinents manqués. |

**Prochaines étapes** :
1. Choisir les technologies et les modèles adaptés à la mise en œuvre de la recherche hybride.
2. Obtenir le registre complet et des extraits de documents pour évaluer leur qualité et les données personnelles et sensibles présentes.
3. Définir l’hébergement et sa maintenance, puis réaliser un prototype de recherche hybride.
4. Organiser des tests avec les employés pour mesurer les KPI et ajuster la solution.

**Questions ouvertes prioritaires** :
- Quelles données sensibles sont présentes dans les dossiers ?
- Quel hébergement acceptez-vous et qui assurera sa maintenance après le départ du prestataire ?
- Quel budget mensuel maximum pouvez-vous consacrer à l’hébergement, à la maintenance et au fonctionnement de la solution ?
- Qui vérifiera les résultats et les seuils proposés de précision (50 %) et de rappel (80 %) sont-ils acceptables ?
