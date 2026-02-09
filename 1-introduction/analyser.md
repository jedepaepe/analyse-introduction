[1-Introduction](./introduction.md)

# Analyser
Nous essayons d'expliquer ce qu'est qu'analyser dans le contexte du développement d'application.

#### Table des matières
- [Travail de l'analyste](#travail-de-lanalyste)
- [Collecte d'information](#collecte-dinformation)
- [Produits de l'analyse](#produits-de-lanalyse)
- [Les outils](#les-outils)
- [Le développeur et l'analyse](#le-développeur-et-lanalyse)

## Travail de l'analyste
Le travail de l'analyste consiste à analyser en vue du développement d'une application ou de sa maintenance.
Il analyse 
- le métier et le domaine ou les métiers et les domaines de l'application
- les besoins des utilisateurs, des organisations
- l'application (en vue de son développement ou de sa maintenance)
- les fonctions que l'application doit implémenter
- les contraintes imposées à la solution technique
- les solutions techniques (designer) pour implémenter ces fonctions

Ce travail peut être découper en quatre phases qui se chevauchent :
![processus d'analyse](/assets/analysis-process-collect-study-document-maintain.png)

Souvent, l'analyste effectue les tests des applications.

Il est aussi une personne de référence qui connait les fonctionnalités de l'application et qui finit par connaitre le métier lié à l'application. Parfois, il connait mieux le métier que les experts métier ...

Il communique. Il communique avec toutes les parties prenantes :
- les responsables, chef de projet, product owner, sponsors
- les utilisateurs
- le (les) expert métier
- les développeurs
- les testeurs


## Collecte d'information
La première tâche d'un analyste consiste à collecter de l'information.

Il a plusieurs méthodes pour collecter de l'information :
- interviewer des experts du métier
- organiser des workshop
- rechercher la documentation existante sur le métier (formulaire, rapport, manuels, description de processus)
- rechercher la documentation déjà existante sur l'application (document de l'étude de faisabilité, différents documents produits par le chef de projet)

Dans le cas d'un remplacement d'une application, l'analyste collectera toute l'information concernant l'ancienne application, c'est-à-dire les différents manuels, le dossier d'analyse, les rapports de tests ... Si elle est toujours en fonctionnement, il aprrendra à l'utiliser et pourra en déduire les différentes fonctionnalités de l'application.

Si l'application est déjà en service, il cherchera les manuels, le dossier d'analyse, les rapports de tests... S'il ne trouve rien, il apprendra à utiliser l'application et commencera un dossier d'analyse.

## Etudier l'information
L'analyse étudie et structure l'information collectée.
Il peut commencer un glossaire, lister les concepts du métier (exemples : clients, factures, produits, ...), les processus du métier (processus d'achat), la journée de l'utilisateur (user journey) et les fonctions de l'application.
Il pourra s'aider d'outils d'organisation de notes et  d'intelligence artificielle comme NotebookLM, Notion AI et Microsoft Notes.

## Créer des modèles
L'analyste produit typiquement un [dossier d'analyse](./dossier-d-analyse.md).
Ce dossier contient essentiellement différents modèles de l'application, par exemple la modélisation des fonctions de l'application, des données de l'applications, des processus, ...

## Maintenir
Une fois le dossier d'analyse suffisant, l'analyste le maintiendra.
Mais que veut dire suffisant pour un dossier d'analyse ?
Complet et cohérent ? Il est rare de voir des dossiers d'analyse complet et cohérent car cela n'apporte généralement pas beaucoup de valeur ajoutée aux organisations. En effet, un dossier complet et cohérent est généralement très compliqué et donc, difficile à utiliser. Car il ne faut l'oublier, l'analyse, c'est un **équilibre entre communication et précision**.
Dans ce cours, je considèrerai qu'un dossier d'analyse est suffisant lorsqu'il suffisant pour démarrer les développements. Nous verrons que suivant les méthodes, ce dossier peut être très complet ou très incomplet.

Une fois l'application en production, il n'est pas rare de voir les dossiers d'analyse tomber dans l'oubli et devenir petit à petit obsolète. Ici encore, il faut tenir compte de la valeur ajoutée du dossier d'analyse. Rien ne sert de maintenir trop d'information. Il faut trouver le juste milieu et il n'y a pas de recette universelle. Chaque organisation, chaque application a son juste milieu.

## Le développeur et l'analyse
Quels rôles ont les développeurs dans l'analyse ?
Typiquement, les développeurs reçoivent le dossier d'analyse et élaborent les détails de la solution technique, de manière formelle ou informelle, c'est-à-dire qu'ils documentent ou pas les détails de la solution technique.
Certains développeurs peuvent devenir analystes, en particulier des analystes techniques.

## Les différents analystes
Le cours se concentre sur le métier de l'analyste fonctionnel. 
Cependant, nous pouvons lister d'autres types d'analystes :
- l'analyste métier (business analyst)
- l'analyste fonctionnel
- l'analyste technique

Ajoutons encore les rôles suivants :
- le product owner (propriétaire du produit, le produit étant l'application)
- data analyst
- system analyst
- solution analyst
- UX/UI analyst
- Qualit analyst

### Business analyst
Le business analyst est plus orienté métier que IT. Il est principalement concerné par le métier et secondairement par les applications qui servent le métier.
Son premier rôle est de documenter le métier, d'aider à la maîtrice opérationnelle du métier et à aider à améliorer le métier. C'est l'intellectuel du métier. C'est un métier qui existait avant l'informatique.

Ils modélisent les processus (métier) à l'aide de la notion BPMN (Business Process Modeling Notation) ou autre.

![Exemple de diagramme BPMN](/assets/wikipedia-bpmn-exemple.jpg)
*Processus d'achat typique, ref: [wikipedia](https://fr.wikipedia.org/wiki/Business_process_model_and_notation)

Comme la digitalisation des métiers est devenue centrale dans nombre d'organisations, les business analystes sont de plus en plus aussi des spécialistes des applications utilisées par le métier.

Notons les responsabilités typique d'un business analyst :
- analyser et documenter les processus métier
- aider à l'optimisation des processus
- analyser et documenter les besoins métier
- participer à la rédaction des business cases
- collaborer avec l'IT

### Fonctional analyst
L'analyste fonctionnelle se concentre sur les fonctions de l'application.
C'est typiquement l'analyste fonctionnel qui rédige le dossier d'analyse.
Traditionnellement, l'analyste fonctionnel créait des use cases et des use case diagrams.

![use case diagram](/assets/wikipedia-use-case-diagram.png)
*Use case diagram pour illustrer un eshop (le système), ref [wikipedia use case diagram](https://en.wikipedia.org/wiki/Use_case_diagram)

Aujourd'hui, les analystes préfèrent utiliser les user stories (récit utilisateur) et les story map :
![story map](/assets/wikipedia-story-map.png)

Beaucoup d'analystes documentent les applications en utilisant les wireframes et d'un texte explicatifs.
![example wireframe](/assets/wikipedia-wireframe.png)
*wireframe pour une page profile. Ref [wikipedia wireframe](https://fr.wikipedia.org/wiki/Wireframe_(design)).*


### Technical analyst
Le rôle l'analyste technique est de définir la solution technique, la maintenir et d'en être l'expert, à un niveau d'intégration. Si le développeur est l'expert du code, le technical analyst est l'expert de l'architecture et du design de la solution. Il sera souvent impliqué dans l'analyse de bug car il pourra déterminer quelle partie de la solution est à l'orgine du bug.

En pratique, peu d'organisations utilisent ce terme pour désigner une fonction et dans bien des cas, le rôle est partagé par différents profils :
- l'architecte IT qui définit les architectures
- le system analyst qui se concentre sur l'intégration des différentes systèmes (et applications)
- le solution analyst qui est un profil hybride métier et technique
- le développeur sénior qui définit le design de l'application et éventuellement l'architecture
- l'analyste fonctionnel s'il a l'appétance et les compétences nécessaires


Haut plus niveau, l'analyste technique décrit les interactions entre l'application et les différents systèmes qu'elle interface. Il peut utiliser un diagramme de déploiement ou autre.

![diagramme d'architecture](/assets/wikipedia-architecture.png)
*Architecture d'une application. Ref: [wikipedia architecture logiciel](https://fr.wikipedia.org/wiki/Architecture_logicielle) L'application est ici divisée en plusieurs exécutables : Aba (un site web visiblement), doors (un daemon/service), cae (computed aided analysis, j'imagine) tool  manager daemon, subversion manager daemon (un gestionnaire de code, comme git), file system manager daemon, hood daemon manager et teamwork manager daemon.*

Il documentera les interfaces entre les différents systèmes, les fameuses API (Application Programming Interface) du diagramme ci-dessus, typiquement en détaillant les messages échangés.

Ensuite, il choisit comment est structurée chaque application. Nous parlons ici de différents modèles comme le MVC (Model View Controller), MVVM (Model View View Model), Event driven, ... En principe, il n'est pas nécessaire de faire un diagramme car ces modèles sont plus ou moins compris par tous.

Rarement, il documentera le code en détail, par exemple avec des diagrammes de composants et des diagrammes de classes d'implémentation.

Il choisira le moteur de base de données et souvent il documentera sa structure de la base avec un diagramme entité relation (ERD).

![exempl de diagramme entites relations](/assets/wikipedia-erd.png)
*Diagramme ERD pour un achat. Ref: [wikipedia entity data model](https://en.wikipedia.org/wiki/Entity_Framework#Entity_Data_Model). Notez que ce diagramme est particulier car ici, on ne peut commander qu'un produit à la fois.*


## Product owner
Le product owner est un rôle que nous trouvons dans les frameworks agile. Dans le framework SCRUM par exemple, le product owner est responsable du product backlog qui est une liste d'éléments (item) qui décrivent l'application et nécessitent une implémentation. Souvent les user stories sont utilisées comme éléments du product backlog mais pas que. Le production owner prend donc les responsabilités de l'analyste, c'est-à-dire collecter l'information, le besoin, le structurer, l'analyser, le documenter et communiquer.

Notons qu'en SCRUM, il n'y a en principe pas d'analyste. Il y a un product owner, une équipe principalement composée de dévéloppeurs et un SCRUM master à temps partiel. L'équipe est considérée comme un tout et doit avoir les compétences nécessaires pour réaliser le produit, c'est-à-dire l'application dans notre contexte.

En pratique, les organisations appliquent un SCRUM personnalisé (customized) parfois à l'extrême et nous trouverons beaucoup d'équipes SCRUM n'ayant pas de product owner et ayant un analyste.

## UX/UI Designer
L'expert User eXperience (UX) et User Interface (UI) intervient dans les projets à fort impact sur les utilisateurs. Il s'agit généralement d'applications et de sites web où l'image de l'entreprise est très importante ou d'applications pour lesquels on prévoit un gros risques de rejet par les utilisateurs.

Il est responsable de la définition de l'interface utilisateur et produit principalement des sketchs (croquis, esquisses), wireframes, maquettes et des prototypes.


## Data analyst
TBC (To Be Confirmed)
Le data analyst est spécialisé dans l'analyse de données. Il sera impliqué dans l'analyse si l'application a une sorte composante données, typiquement les rapports.
Il sera aussi impliqué s'il s'agit d'une application avec analyse de données, par exemple une application de reporting (qui fait des rapports, souvent pour aider la direction à prendre des décisions), ou s'il s'agit d'une application avec du deep learning (par exemple, prédiction de panne).

## Résumé
Voici un résumé des différens rôles telles que je perçois en Belgique car cela peut changer de pays en pays :

| profil | focus principal | livrables | outils/compétences | Interlocuteurs |
|---|---|---|---|---|
| business analyst | stratégie & métier | business case & processus | BPMN, interviews | direction & métier & IT |
| functional analyse | fonctions de l'application | dossier d'analyse, backlog | interviews, user stories, wireframes, UML | métier & développeurs & testeurs |
| product owner | valeur de l'application | backlog priorisé | user storyes, interview | métier, développeurs, testeurs |
| technical analyst | design de l'application | partie technique du dossier d'analyse | architecture, ERD, API | développeurs & testeurs & architecte IT & métier |
| architect IT | solutions techniques, cohérence IT | architecure, roadmap | TOGAF, diagramme d'architecture | direction IT & développeurs & analystes |
| UX/UI Designer | expérience utilisateur | personna, parcours utilisateur | sketch, wireframe, maquette, prototype | utilisateurs & métier & développeurs |
| data analyst | données | rapports, tableaux de bord | SQL, Power BI, Python, data platforms | manager |

