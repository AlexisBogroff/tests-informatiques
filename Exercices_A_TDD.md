# Exercices

**Recommandation** : lire l'ensemble du document avant de débuter l'implémentation.

## Cahier des charges

Vous allez permettre à un utilisateur d'exploiter un LLM local de manière multimodale (texte + pdfs + capacité de code).

**Exemples d'utilisation**
- L'utilisateur doit pouvoir fournir un PDF et demander au site de résumer le document, ou de répondre à la question de l'utilisateur en se basant sur ce document.
- Il doit pouvoir également demander en langage naturel d'effectuer un calcul, qui après avoir été extrait de la question sera effectué en utilisant du code.
- (optionnel) Il doit pouvoir fournir un jeu de données csv sur lequel des modèles simples de clustering seront entraînés, pour lesquels le site leur renverra une liste des clusters trouvés et des graphs les représentant.

**Design front-end**
- Sur cette single page app, un input permettra donc à l'utilisateur d'entrer du texte pour effectuer des demandes (prompt).
- Un bouton permettra à l'utilisateur de fournir un document (texte, pdf, csv)
- Un cadre de messagerie permettra au site d'afficher sa réponse à l'utilisateur.
- (optionnel): un cadre supplémentaire permettra d'afficher le graph avec les clusters.


**Contraintes**

Cette application :
- Sera une webapp accessible en local sur un explorateur web.
- Se basera sur le principe de clean code de modularité (front-end et back-end séparés).
- Les communications entre les composants de l'application seront effectués via une API Flask.
- Utilisera Ollama avec le modèle Mistral 7B ou Llama 7B


## Exercice 1

**Etape 1**

Définir et écrire un premier test unitaire qui sera nécessaire pour l'application.

**Etape 2** (red)

Vérifier que le test ne n'est pas validé dans l'état actuel du projet.

**Etape 3** (green)

Ecrire le code pour passer le test.

**Etape 4** (blue)

Code refactoring : à présent le test est validé. Ré-écrire le code pour qu'il soit plus lisible, maintenable et efficace.


## Exercice 2

Développement du back-end

Ajouter davantage de tests pour développer les fonctions de base nécessaires pour le back-end de cette application.

Répéter les étapes 1 à 3, puis effectuer le code refactoring une fois la majorité des fonctionnalités de base de l'application codées.


## Exercice 3

Regrouper les tests dans des classes distinctes et cohérentes.

Lancer uniquement une partie des tests (la première classe par exemple) pour en vérfiier le bon fonctionnement.


## Exercice 4

Développement de l'API

Même question que exercice 2. Cependant, écrire également les tests dans des classes cohérentes pour faciliter les tests ciblés par catégorie.


## Exercice 5

Tests d'intégration: le back-end et l'API peuvent à présent être fusionnés.

Ajouter des tests d'intégration en suivant la méthodologie TDD (fail, pass, refactor).

C'est uniquement à cette étape que le back-end doit donc contenir des fonctions pour communiquer avec l'API.
