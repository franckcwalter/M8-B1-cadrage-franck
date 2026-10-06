# Notes d'entretien

## 0. Brief  

Ton client : Cas A — Cabinet Maître Devalle (juridique PME)

Cabinet d'avocats, 12 avocats, Bordeaux. Maître Élise Devalle reçoit.
« On rédige beaucoup de courriers types (mise en demeure, transmission dossier). On voudrait un assistant pour aller plus vite, et aussi pour retrouver les bonnes jurisprudences en 30 secondes au lieu de 30 minutes. »


## 1. Avant le rendez-vous — 12 questions + 3 de réserve

> Le client accorde **12 réponses**. **Une question à la fois**. Classe par
> priorité : si tu n'en poses que 8, ce doivent être les 8 plus utiles.
> Catégories à couvrir : besoin · processus actuel · données (existence, volume,
> qualité, **extrait**) · données personnelles / confidentialité · critère de
> succès chiffré · coût d'une erreur · utilisateurs · SI / hébergement · budget / délai.



| # | Priorité (1-3) | Catégorie | Question |
|---|---|---|---|
| 1 | 1 | BESOIN | À quoi servirait l’IA pour les courriers types ? |
| 2 | 1 | PROCESSUS ACTUEL | Quelle est la démarche actuelle pour la recherche de jurisprudence ? |
| 3 | 1 | BESOIN | La recherche de jurisprudence doit se faire dans quel corpus ? |
| 4 | 1 | DONNÉES | Quels sont les types de données dont vous disposez ? |
| 5 | 1 | DONNÉES | Pouvez-vous me faire parvenir un extrait de chaque type de données ? |
| 6 | 1 | DP/ confidentialité | *Les données contiennent-elles des données personnelles ?* — Oui, il y a des données personnelles. Question à ne pas poser pour le moment ; à revoir éventuellement en fin d’entretien. |
| 7 | 1 | critère de succès chiffré | Combien de temps consacrez-vous aujourd’hui à préparer un courrier type ? |
| 8 | 1 | COUT D'UNE ERREUR | Dans quelle mesure les productions de l’IA seront-elles relues et vérifiées ? |
| 9 | 2 | USERS | Qui seront les personnes utilisatrices de la solution d’IA ? |
| 10 | 2 | SI / hébergement | De quelle architecture informatique disposez-vous actuellement ? |
| 11 | 2 | budget délai | Quel est le budget alloué ? |
| 12 | 2 | budget délai | Quand la solution doit-elle être prête ? |
| R1 | réserve | | |
| R2 | réserve | | |
| R3 | réserve | | |

## 2. Pendant le rendez-vous — dit / interprété

| Réponse n° | Question posée (telle quelle) | Ce que le client a **dit** (citation) | Catégorie de la réponse | Ce que j'en **interprète** |
|---|---|---|---|---|
| 1 | À quoi servirait l’IA pour les courriers types ? | *« Chaque avocat a ses vieux courriers sur son poste, et on copie-colle. Il y a bien un dossier « modèles » partagé, mais il date de 2019 et personne ne le met à jour. Les assistantes préparent, l'avocat relit et signe. »* | PROCESSUS ACTUEL | <ul><li>Le processus actuel pour les courriers, c'est du copier-coller d'anciens courriers.</li><li>On a des templates mais qui sont vieux et qui ne sont pas utilisés.</li><li>Chaque employé a ses templates.</li><li>Les assistantes préparent les courriers.</li><li>L'avocat relit les courriers.</li><li>L'avocat signe les courriers et en est responsable.</li></ul> |
| 2 | Quelle est la démarche actuelle pour la recherche de jurisprudence ? | *« Pour la jurisprudence publique, on a un abonnement à une base juridique en ligne. Mais notre vraie richesse, ce sont nos propres dossiers : les décisions qu'on a obtenues ici, à Bordeaux. Elles sont rangées dans des dossiers sur le serveur, et on cherche par nom de fichier… ou on demande au collègue qui s'en souvient. »* | DONNÉES · PROCESSUS ACTUEL | <ul><li>La jurisprudence publique est recherchée dans une base juridique en ligne.</li><li>La recherche porte aussi sur les dossiers internes du cabinet.</li><li>Les dossiers internes sont stockés sur un serveur interne.</li><li>La recherche se fait actuellement par nom de fichier.</li><li>La recherche se fait aussi de manière informelle en demandant à un collègue.</li><li>Certaines informations reposent sur la mémoire des employés et ne sont pas documentées.</li></ul> |
| 3 | La recherche de jurisprudence doit se faire dans quel corpus ? | *« Pour la jurisprudence publique, on a un abonnement à une base juridique en ligne. Mais notre vraie richesse, ce sont nos propres dossiers : les décisions qu'on a obtenues ici, à Bordeaux. Elles sont rangées dans des dossiers sur le serveur, et on cherche par nom de fichier… ou on demande au collègue qui s'en souvient. »* | DONNÉES · PROCESSUS ACTUEL | / |
| 4 | Quels sont les types de données dont vous disposez ? | *« Environ 2 000 décisions sur les quinze dernières années, en PDF ou en Word, plus des milliers de courriers archivés dans les dossiers clients. Les plus anciennes décisions sont des scans papier, pas toujours très lisibles. »* | DONNÉES | <ul><li>Deux types de données : les décisions et les courriers archivés.</li><li>Volume des décisions : environ 2 000 sur quinze ans.</li><li>Volume des courriers archivés : des milliers, sans nombre précis.</li><li>Formats des décisions : PDF ou Word ; les plus anciennes sont des scans papier.</li><li>Format des courriers archivés : non précisé.</li><li>Les courriers sont archivés dans les dossiers clients ; les modalités d’archivage ne sont pas précisées.</li><li>Qualité des données : les scans des anciennes décisions ne sont pas toujours très lisibles.</li></ul> |
| 5 | Pouvez-vous me faire parvenir un extrait de chaque type de données ? | *« Une assistante tient un registre des décisions : numéro, date, matière, juridiction, issue, et le nom du fichier. Je vous en transmets un extrait, seulement le registre, pas les décisions elles-mêmes, vous comprendrez pourquoi. »*<br><br>*« (Je vous ai transmis un fichier : voir « Documents transmis ».) »*<br><br>Fichier transmis : [cas_A_registre_decisions_sample.csv](cas_A_registre_decisions_sample.csv) | DONNÉES | <ul><li>Un registre des décisions est tenu par une assistante.</li><li>Le registre comporte 6 colonnes : decision_id, date, matiere, juridiction, issue, fichier.</li><li>L’extrait consulté contient 20 lignes de données.</li><li>L’extrait paraît complet et de bonne qualité : aucune cellule vide apparente.</li><li>La qualité du registre complet reste à vérifier ; des informations pourraient manquer hors de cet extrait.</li><li>Seul un extrait du registre est accessible, sans les décisions elles-mêmes.</li><li>L’aspect et le contenu des décisions ne peuvent donc pas être vérifiés.</li><li>La présence de données personnelles semble expliquer l’absence de transmission des décisions ; ce motif reste à confirmer.</li></ul> |
| — | *Les données contiennent-elles des données personnelles ?* — Oui, il y a des données personnelles. Question à ne pas poser pour le moment ; à revoir éventuellement en fin d’entretien. | |  | |
| 6 | Combien de temps consacrez-vous aujourd’hui à préparer un courrier type ? | *« Pour tout le cabinet, une quinzaine de courriers types par jour, et une dizaine de recherches de jurisprudence interne par jour. C'est surtout la recherche qui prend du temps. »* | PROCESSUS ACTUEL · BESOIN | <ul><li>Environ 15 courriers types à écrire par jour pour le cabinet.</li><li>Environ 10 recherches internes de jurisprudence par jour.</li><li>La recherche de jurisprudence est l’activité qui prend le plus de temps.</li><li>Le besoin prioritaire est de réduire le temps de recherche de jurisprudence.</li></ul> |
| 7 | Dans quelle mesure les productions de l’IA seront-elles relues et vérifiées ? | *« Deux choses. D'abord les courriers types, mises en demeure, transmissions de dossier : on les réécrit à partir d'anciens courriers, c'est du temps perdu. Ensuite, et c'est le plus pénible, retrouver une décision qu'on a déjà obtenue ou étudiée : trente minutes pour ce qui devrait en prendre trente secondes. »* | BESOIN · critère de succès chiffré | <ul><li>Types de courriers : mises en demeure et transmissions de dossiers.</li><li>Les nouveaux courriers sont rédigés à partir d’anciens courriers.</li><li>Ce processus de rédaction fait perdre du temps.</li><li>Le principal problème est de retrouver une décision déjà obtenue ou étudiée.</li><li>Une recherche de jurisprudence prend actuellement 30 minutes.</li><li>L’objectif est de réduire ce temps de recherche à 30 secondes.</li></ul> |
| 8 | Qui seront les personnes utilisatrices de la solution d’IA ? | *« Les avocats et les assistantes, uniquement en interne. Mon associé aimerait un jour un « assistant » sur notre site pour répondre aux clients, mais ce n'est pas le sujet aujourd'hui. »* | USERS · BESOIN | <ul><li>Les utilisateurs sont les avocats, les assistants et les assistantes.</li><li>L’usage est uniquement interne.</li><li>Un assistant sur le site pour répondre aux clients est envisagé à un autre horizon.</li><li>Ce projet futur est hors du périmètre actuel.</li></ul> |
| 9 | De quelle architecture informatique disposez-vous actuellement ? | *« Un logiciel de gestion de cabinet du marché pour les dossiers et la facturation, hébergé en France, Microsoft 365 pour les mails et Word, et un serveur de fichiers au cabinet pour les documents. »* | SI / hébergement | <ul><li>Les documents sont stockés sur un serveur de fichiers au cabinet.</li></ul> |
| 10 | Quel est le budget alloué ? | *« Serré. On est un cabinet de douze, pas un grand groupe. Mettons 15 000 euros pour démarrer, et ensuite un abonnement mensuel raisonnable, pas plus de quelques centaines d'euros par mois. »* | budget délai | <ul><li>Le budget de démarrage est de 15 000 €.</li><li>Un abonnement mensuel de quelques centaines d’euros peut être prévu pour la maintenance, la gestion et l’évolution.</li></ul> |
| 11 | Quand la solution doit-elle être prête ? | *« Pas d'urgence absolue. Je préfère quelque chose de fiable dans six mois que quelque chose de risqué dans un mois. »* | budget délai | <ul><li>Délai envisagé : entre 1 et 6 mois, avec une version finale entièrement terminée à 6 mois.</li><li>Prévoir une première version de test.</li><li>Proposition : une première version d’ici 3 mois.</li><li>Prévoir ensuite des tests et des allers-retours avant la version finale.</li></ul> |
| 12 | Quelle est la liste exhaustive de courriers types ? | *« Chaque avocat a ses vieux courriers sur son poste, et on copie-colle. Il y a bien un dossier « modèles » partagé, mais il date de 2019 et personne ne le met à jour. Les assistantes préparent, l'avocat relit et signe. »* | PROCESSUS ACTUEL | / |
| 13 | quel coût et importance d'une erreur ? | *« Une erreur dans un courrier ou une jurisprudence qui n'existe pas, c'est ma responsabilité professionnelle engagée. J'ai lu cette histoire d'avocats américains qui ont cité des décisions inventées par une IA. Ça, jamais chez nous. Tout doit être vérifiable. »* | COUT D'UNE ERREUR | <ul><li>Le coût d’une erreur est très élevé.</li><li>La responsabilité professionnelle de l’avocat est engagée.</li><li>Une erreur dans un courrier ou une jurisprudence inexistante est très grave.</li><li>Tout doit être vérifiable et sourcé.</li></ul> |
| 14 | quelle données personnelle et sensibles dont présentes ? | *« Bien sûr : nos clients, les parties adverses, parfois des salariés, des enfants dans les affaires familiales. Les décisions publiques sont anonymisées, les nôtres non. »* | DP/ confidentialité | <ul><li>Présence de données personnelles et de données sensibles.</li><li>Données concernant les clients et les parties adverses.</li><li>Données relatives au travail.</li><li>Données concernant des enfants.</li><li>Les décisions internes ne sont pas anonymisées.</li><li>Les décisions publiques sont anonymisées.</li></ul> |



### Boussole — ce que j’ai déjà obtenu

| Information | Informations obtenues / à préciser | Réponse n° |
|---|---|---|
| Besoin réel (≠ demande exprimée) | <ul><li>Priorité : **réduire le temps de recherche interne de jurisprudence**.</li><li>Accélérer aussi la rédaction des courriers.</li></ul> | 6, 7 |
| Processus actuel : recherche jurisprudentielle | <ul><li>Recherche dans une **base juridique en ligne**.</li><li>Recherche dans les **dossiers internes**, stockés sur un serveur interne.</li><li>Recherche par **nom de fichier** ou en demandant à un collègue.</li><li>Certaines informations reposent sur la **mémoire des employés** et ne sont pas documentées.</li><li>Environ **10 recherches internes par jour**.</li></ul> | 2, 6 |
| Processus actuel : rédaction des courriers | <ul><li>**Copier-coller d’anciens courriers**.</li><li>Modèles partagés de **2019**, non actualisés et non utilisés.</li><li>Chaque employé a ses propres modèles.</li><li>Les **assistantes préparent** les courriers.</li><li>L’**avocat relit** les courriers.</li><li>L’avocat **signe et en est responsable**.</li><li>Environ **15 courriers types par jour**.</li></ul> | 1, 6 |
| Données : existence | <ul><li>**Décisions internes, courriers archivés et registre des décisions** disponibles.</li><li>Abonnement à une **base juridique publique**.</li></ul> | 2, 4, 5 |
| Données : volume | <ul><li>Environ **2 000 décisions sur 15 ans**.</li><li>**Des milliers de courriers**, sans nombre précis.</li></ul> | 4 |
| Données : qualité | <ul><li>Anciens scans **parfois peu lisibles**.</li><li>Extrait du registre : **20 lignes et 6 colonnes**, sans cellule vide apparente.</li><li>**Qualité globale à vérifier**.</li></ul> | 4, 5 |
| Données : extrait obtenu | <ul><li>**CSV du registre uniquement**.</li><li>Aucune décision ni aucun courrier transmis.</li></ul> | 5 |
| Données personnelles / confidentialité | <ul><li>Données concernant les **clients, parties adverses, salariés et enfants**.</li><li>Décisions internes **non anonymisées**.</li><li>Décisions publiques anonymisées.</li><li>**Nature des données sensibles à préciser**.</li></ul> | 14 |
| Critère de succès chiffré | <ul><li>Retrouver une **décision déjà obtenue ou étudiée** en **30 secondes**, contre **30 minutes actuellement**.</li><li>**Objectif chiffré pour les courriers non obtenu**.</li></ul> | 7 |
| Coût d'une erreur | <ul><li>Coût **très élevé**.</li><li>**Responsabilité professionnelle engagée** en cas de courrier erroné ou de jurisprudence inventée.</li><li>Résultats **vérifiables et sourcés**.</li></ul> | 13 |
| Erreurs tolérées (chiffre : fausses alertes, mauvais routage…) | <ul><li>**Seuil chiffré non obtenu**.</li></ul> | — |
| Utilisateurs | <ul><li>**Avocats et assistantes**.</li><li>Usage **interne**.</li><li>Assistant public hors du périmètre actuel.</li></ul> | 8 |
| Validation humaine / qui décide | <ul><li>Les assistantes préparent les courriers.</li><li>L’avocat assure la **relecture et la signature**, avec sa **responsabilité engagée**.</li><li>**Validation de la future solution à préciser**.</li></ul> | 1 |
| SI / hébergement | <ul><li>Les documents sont stockés sur un **serveur de fichiers au cabinet**.</li></ul> | 9 |
| Budget | <ul><li>**15 000 € au démarrage**.</li><li>**Quelques centaines d’euros par mois**.</li><li>Plafond mensuel exact à préciser.</li></ul> | 10 |
| Délai | <ul><li>**Fiabilité privilégiée**.</li><li>Horizon de **6 mois**.</li><li>Proposition à valider : **version de test à 3 mois**, puis retours.</li></ul> | 11 |
| Ce qui a déjà été essayé | <ul><li>Dossier partagé de modèles de **2019**, non actualisé.</li><li>**Autres essais non précisés**.</li></ul> | 1 |

## 3. Après — ce que je n'ai pas pu demander → questions ouvertes

| Je n'ai pas pu demander / pas eu de réponse claire | Pourquoi c'est important | → §6 du cadrage |
|---|---|---|
| **Nombre précis de courriers archivés** | Préciser le volume de données à traiter. | Volume des courriers à confirmer. |
| **Format et modalités d’archivage des courriers** | Évaluer leur exploitation. | Formats et archivage à préciser. |
| **Qualité du registre complet et des documents** | Seules 20 lignes du registre ont été consultées. Aucun courrier ni aucune décision examinés. | Qualité globale à vérifier. |
| **Motif de non-transmission des décisions** | La présence de données personnelles est une explication supposée. | Motif à confirmer. |
| **Nature des données sensibles** | La réponse identifie les personnes concernées, sans préciser les données sensibles présentes. | Nature des données sensibles à préciser. |
| **Objectif chiffré pour les courriers** | Mesurer le gain attendu sur la rédaction. | Objectif pour les courriers à définir. |
| **Seuil chiffré d’erreurs tolérées** | Définir un critère d’acceptation compte tenu du coût élevé d’une erreur. | Seuil d’erreurs à définir. |
| **Validation humaine de la future solution** | La relecture actuelle est connue. Le fonctionnement futur reste à préciser. | Validation future à préciser. |
| **Plafond mensuel exact du budget** | Vérifier que les coûts récurrents restent acceptables. | Budget mensuel à confirmer. |
| **Première version de test à 3 mois** | Ce calendrier est une proposition, à valider avec le client. | Jalon de test à valider. |
| **Autres solutions déjà essayées** | Seul le dossier de modèles de 2019 est connu. | Autres essais à préciser. |

## 4. Reformulation du besoin

Le besoin principal du client est de passer de 30 minutes à 30 secondes pour retrouver une décision de jurisprudence interne déjà obtenue ou étudiée, tout en obtenant des résultats fiables, sourcés et vérifiable.

Le besoin secondaire est de réduire le temps de rédaction des documents juridiques, sans objectif chiffré précisé par le client. Il pourrait être traité sans IA, avec des modèles de courriers validés, partagés et alimentés par une recherche rapide. Le recours à un modèle de génération de texte (LLM) soulève un risque d’informations inventées, mais ce choix serait réévalué si une solution IA pouvait démontrer une fiabilité de 100 %, sans information inventée.
