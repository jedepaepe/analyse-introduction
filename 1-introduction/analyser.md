[1-Introduction](./introduction.md)

# Analyser
Nous essayons d'expliquer ce qu'est qu'analyser dans le contexte du développement d'application.

#### Table des matières
- [Travail de l'analyste](#travail-de-lanalyste)
- [Collecter l'information](#collecter-linformation)
- [Étudier l'information](#etudier-linformation)
- [Créer des modèles](#créer-des-modèles)
- [Maintenir l'analyse](#maintenir)
- [Le développeur et l'analyse](#le-développeur-et-lanalyse)
- [Les différents analystes](#les-différents-analystes)
    - [Business analyst](#business-analyst)
    - [Functional analyst](#functional-analyst)
    - [Technical analyst](#technical-analyst)
    - [Product owner](#product-owner)
    - [UX/UI Designer](#uxui-designer)
    - [Data analyst](#data-analyst)
    - [Résumé](#résumé)
- [Données réelles](#données-réelles)



## Travail de l'analyste
Le travail de l'analyste consiste à analyser les besoins métier en vue du développement d'une application ou de sa maintenance.

Il analyse 
- le métier et le domaine ou les métiers et les domaines concernés par l'application
- les besoins des utilisateurs, des organisations
- l'application (en vue de son développement ou de sa maintenance)
- les fonctions que l'application doit implémenter
- les contraintes imposées à la solution
- les solutions techniques (designer) pour implémenter ces fonctions et respecter les contraintes

Ce travail peut être découper en quatre phases qui en pratique se chevauchent :
![processus d'analyse](/assets/analysis-process-collect-study-document-maintain.png)

Souvent, l'analyste effectue les tests des applications.

Il est aussi une personne de référence qui connaît les fonctionnalités de l'application et qui finit parfois par devenir un expert du métier. 

La communication est centrale dans sa pratique. Il communique avec toutes les parties prenantes du développement et de la maintenance de l'application :
- les responsables, chef de projet, product owner, sponsors
- les utilisateurs
- le (les) expert métier
- les développeurs
- les testeurs
- les architectes IT
- les SDM (Software Delivery Manager)
- ...


## Collecter l'information
La première tâche d'un analyste consiste à collecter de l'information.

Il a plusieurs techniques pour collecter de l'information :
- interviewer des experts du métier et les utilisateurs
- organiser des workshops
- rechercher la documentation existante sur le métier (formulaire, rapport, manuels, description de processus, internet, IA)
- rechercher la documentation déjà existante sur l'application (document de l'étude de faisabilité, différents documents produits par le chef de projet)

Dans le cas d'un remplacement d'une application, l'analyste collectera toute l'information concernant l'ancienne application, c'est-à-dire les différents manuels, le dossier d'analyse, les rapports de tests ... Si elle est toujours en fonctionnement, il apprendra à l'utiliser et pourra en déduire les différentes fonctionnalités de l'application.

Si l'application est déjà en service, il cherchera les manuels, le dossier d'analyse, les rapports de tests... S'il ne trouve rien, il apprendra à utiliser l'application et décrira ses interfaces (les pages web, fenêtres de l'application).

Il est conseillé de collecter les données réelles. Soit en demandant des examples réels lors des interviews. Soit en les collectant à partir des documents existants (formulaires, rapports), soit en allant les chercher dans les databases existantes.

## Étudier l'information
L'analyse étudie et structure l'information collectée.
Il peut commencer un glossaire, lister les concepts du métier (exemples : clients, factures, produits, ...), les processus du métier (processus d'achat), la journée de l'utilisateur (user journey) et les fonctions de l'application.
Il pourra s'aider d'outils d'organisation de notes et  d'intelligence artificielle comme NotebookLM, Notion AI et Microsoft Notes.

Les techniques de base sont :
- un nom commun est potentiellement un concept du métier ou une propriété d'un concept du métier
- un verbe et son complément d'objet direct est potentiellement une fonction de l'application
- une suite de fonction pour attendre en final une réelle valeur ajoutée est potentiellement un processus

L'analyste listera ainsi :
- les concepts avec leur propriété (ébauche du design la DB)
- les fonctions (ébauche des user stories ou use cases)
- les processus

## Créer des modèles
Je ne donne ici qu'un bref aperçu car c'est l'objet du cours.
L'analyste produit typiquement un [dossier d'analyse](./dossier-d-analyse.md).
Ce dossier contient essentiellement différents modèles de l'application, par exemple la modélisation des fonctions de l'application, des données de l'applications, des processus, ...

## Maintenir
Une fois le dossier d'analyse suffisant, l'analyste le maintiendra.
Mais que veut dire suffisant pour un dossier d'analyse ?
Complet et cohérent ? Il est rare de voir des dossiers d'analyse complets et cohérents car cela n'apporte généralement pas beaucoup de valeur ajoutée aux organisations. En effet, un dossier complet et cohérent est généralement très compliqué et donc, cher et difficile à utiliser. Car il ne faut l'oublier, l'analyse, c'est un **équilibre entre communication et précision**.
Dans ce cours, je considérerai qu'un dossier d'analyse est suffisant lorsqu'il suffisant pour démarrer les développements. Nous verrons que suivant les méthodes, ce dossier peut être très complet ou très incomplet. D'ailleurs beaucoup de développement sont réalisés sans dossier d'analyse et cela peut réussir. Et faire un dossier d'analyse n'est pas une garantie de réussite du projet. En pratique, cela aide à réussir.

Une fois l'application en production, il n'est pas rare que les dossiers d'analyse tombent dans l'oubli et deviennent petit à petit obsolètes. Ici encore, il faut tenir compte de la valeur ajoutée du dossier d'analyse. Rien ne sert de maintenir trop d'information. Il faut trouver le juste milieu et il n'y a pas de recette universelle. Chaque organisation, chaque application a son juste milieu.

## Le développeur et l'analyse
Quels rôles ont les développeurs dans l'analyse ?
Typiquement, les développeurs reçoivent le dossier d'analyse. Sur cette base, ils élaborent les détails de la solution technique, de manière formelle ou informelle, c'est-à-dire qu'ils documentent ou pas les détails de la solution technique.
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
- Quality analyst

### Business analyst
Le business analyst est plus orienté métier que IT. Il est principalement concerné par le métier et secondairement par les applications qui servent le métier.
Son premier rôle est de documenter le métier, d'aider à la maîtrise opérationnelle du métier et à aider à améliorer le métier. C'est l'intellectuel du métier. C'est un métier qui existait avant l'informatique.

Ils modélisent les processus (métier) à l'aide de la notion BPMN (Business Process Modeling Notation) ou autre.

![Exemple de diagramme BPMN](/assets/wikipedia-bpmn-exemple.jpg)
*Processus d'achat typique, ref: [wikipédia business process model and notation](https://fr.wikipedia.org/wiki/Business_process_model_and_notation).*

Comme la digitalisation des métiers est devenue centrale dans nombre d'organisations, les business analystes sont de plus en plus aussi des spécialistes des applications utilisées par le métier.

Notons les responsabilités typiques d'un business analyst :
- analyser et documenter les processus métier
- aider à l'optimisation des processus
- analyser et documenter les besoins métier
- rédiger des business cases
- rédiger des cahier des charges
- collaborer avec l'IT

### Functional analyst
L'analyste fonctionnelle se concentre sur les fonctions de l'application.
C'est typiquement l'analyste fonctionnel qui rédige le dossier d'analyse.
Traditionnellement, l'analyste fonctionnel créait des use cases et des use case diagrams.

![use case diagram](/assets/wikipedia-use-case-diagram.png)
*Exemple de use case diagram. Il documente les fonctions d'un eshop (le système), ref [wikipédia use case diagram](https://en.wikipedia.org/wiki/Use_case_diagram).*

Aujourd'hui, les analystes préfèrent utiliser les user stories (récit utilisateur) et les story map :
![story map](/assets/wikipedia-story-map.png)
*Exemple de story map. Elle documente les fonction de jira, une application de suivi de bugs, d'incidents, de gestion de projets agile, ref: [wikipédia récit utilisateur](https://fr.wikipedia.org/wiki/R%C3%A9cit_utilisateur)*

Beaucoup d'analystes documentent les applications à l'aide de wireframes et de textes explicatifs :
![example wireframe](/assets/wikipedia-wireframe.png)
*Example de wireframe, une page profile, ref [wikipédia wireframe](https://fr.wikipedia.org/wiki/Wireframe_(design)).*


### Technical analyst
Le rôle l'analyste technique est de définir la solution technique, la maintenir et d'en être l'expert. Si le développeur est l'expert du code, le technical analyst est l'expert de l'architecture et du design de la solution. Il sera souvent impliqué dans l'analyse de bug car il pourra déterminer quelle partie de la solution est à l'origine du bug.

En pratique, peu d'organisations utilisent ce terme pour désigner une fonction et dans bien des cas, le rôle est partagé par différents profils :
- l'architecte IT qui définit les architectures
- le system analyst qui se concentre sur l'intégration des différentes systèmes (et applications)
- le solution analyst qui est un profil hybride métier et technique
- le développeur senior qui définit le design de l'application et éventuellement l'architecture
- l'analyste fonctionnel, s'il a l'appétence et les compétences nécessaires


Au plus niveau, l'analyste technique décrit les interactions entre l'application et les différents systèmes qu'elle interface. Il utile le diagramme de déploiement UML ou plus couramment un diagramme libre :
![diagramme d'architecture](/assets/wikipedia-architecture.png)
*Example de diagramme d'architecture; ref: [wikipédia architecture logiciel](https://fr.wikipedia.org/wiki/Architecture_logicielle); l'application est ici divisée en plusieurs exécutables : Aba (un site web visiblement), doors (un daemon/service), cae (computed aided analysis, j'imagine) tool  manager daemon, subversion manager daemon (un gestionnaire de code, comme git), file system manager daemon, hood daemon manager et teamwork manager daemon.*

Il documentera les interfaces entre les différents systèmes, les fameuses API (Application Programming Interface) du diagramme ci-dessus, typiquement en détaillant les messages échangés et la séquence des échanges :
![Exemple de diagramme de séquences pour illustrer les échanges avec un serveur de mail](/assets/wikipedia-sequence-diagram-for-system-integration.png)
*Example de diagramme de séquences pour documenter une interface; ici avec un serveur mail; ref: [wikipédia](https://en.wikipedia.org/wiki/Sequence_diagram).*

Ensuite, il détermine la structure chaque application. Nous parlons ici de différents modèles comme le MVC (Model View Controller), MVVM (Model View View Model), Event driven, CQRS (Command Query Responsibility Segregation), asynchrone ou synchrone. En principe, il n'est pas nécessaire de faire un diagramme car ces modèles sont plus ou moins compris de tous.

Par le passé, il documentait le code en détail, par exemple avec des diagrammes de composants et des diagrammes de classes d'implémentation, mais cette pratique est aujourd'hui abandonnée car dans la majorité des cas, c'est une perte de temps. Ces diagrammes sont encore utilisés par les développeurs mais de manière temporaire, typiquement pour prendre du recul, pour réfléchir, pour résoudre un problème.

Il choisira le moteur de base de données et souvent il documentera sa structure de la base avec un diagramme entité relation (ERD).

![exemple de diagramme entités relations](/assets/wikipedia-erd.png)
*Diagramme ERD pour un achat. Ref: [wikipédia entity data model](https://en.wikipedia.org/wiki/Entity_Framework#Entity_Data_Model). Notez que ce diagramme est inhabituel car il illustre le fait qu'une commande ne peut contenir qu'un seul produit.*


### Product owner
Le product owner est un rôle que nous trouvons dans les frameworks agiles. Dans le framework SCRUM par exemple, le product owner est responsable du product backlog qui est une liste d'éléments (item) qui décrivent l'application. Souvent les user stories sont utilisées pour les éléments fonctionnels du product backlog. Le production owner prend donc les responsabilités de l'analyste, c'est-à-dire collecter l'information, le besoin, le structurer, l'analyser, le documenter et communiquer.

Notons qu'en SCRUM, il n'y a en principe pas d'analyste. Il y a un product owner, une équipe principalement composée de développeurs et un SCRUM master à temps partiel. L'équipe est considérée comme un tout et doit avoir les compétences nécessaires pour réaliser le produit, c'est-à-dire l'application dans notre contexte.

En pratique, les organisations appliquent un SCRUM personnalisé (customized) parfois à l'extrême et nous trouverons beaucoup d'équipes SCRUM n'ayant pas de product owner et ayant un analyste. La question du jour : "peut-on les appeler équipes SCRUM :-)" ?

### UX/UI Designer
L'expert User eXperience (UX) et User Interface (UI) intervient dans les projets à fort impact sur les utilisateurs. Il s'agit généralement d'applications et de sites web où l'image de l'organisation est très importante ou d'applications pour lesquels on prévoit un gros risques de rejet par les utilisateurs ou d'applications complexes mais qui doivent être self learning (sans manuel utilisateur).

Il est responsable de la définition de l'interface utilisateur et produit principalement des sketchs (croquis, esquisses), wireframes, maquettes et des prototypes.


### Data analyst
TBC (To Be Confirmed)
Le data analyst est spécialisé dans l'analyse de données. Il sera impliqué dans l'analyse si l'application a une sorte composante données, typiquement les rapports.
Il sera aussi impliqué s'il s'agit d'une application avec analyse de données, par exemple une application de reporting (qui fait des rapports, souvent pour aider la direction à prendre des décisions), ou s'il s'agit d'une application avec du deep learning (par exemple, prédiction de panne).

### Résumé
Résumons d'abord les trois niveaux de l'analyse d'une application :

| analyse | focus | question | explication |
|-|-|-|-|
| business | métier | pourquoi | décrit le pourquoi l'application, sa valeur ajoutée, les besoins et processus métiers |
| functional | application | quoi | décrit ce que fait l'application |
| technical/design | application | comment | décrit la solution (technique), comment l'application fait le quoi |

Résumons les différents rôles telles que je perçois en Belgique car cela peut changer de pays en pays :

| profil | focus principal | livrables | outils/compétences | Interlocuteurs |
|---|---|---|---|---|
| business analyst | stratégie, métier | business case, processus | BPMN, interviews | direction, métier, IT |
| functional analyse | fonctions de l'application | dossier d'analyse, backlog | interviews, user stories, wireframes, UML | métier, développeurs, testeurs |
| product owner | valeur de l'application | backlog priorisé | user stories, interview | métier, développeurs, testeurs |
| technical analyst | design de l'application | partie technique du dossier d'analyse | architecture, ERD, API | développeurs, testeurs, architecte IT, métier |
| architect IT | solutions techniques, cohérence IT | architecture, roadmap | TOGAF, diagramme d'architecture | direction IT, développeurs, analystes |
| UX/UI Designer | expérience utilisateur | persona, parcours utilisateur | sketch, wireframe, maquette, prototype | utilisateurs, métier, développeurs |
| data analyst | données | rapports, tableaux de bord | SQL, Power BI, Python, data platforms | managers métier |

## Données réelles
Je souhaite faire ici un focus sur les données réelles. Je crois n'avoir jamais vu un analyste relever les données réelles. Pourtant, elles valent de l'or car elles permettent de valider. 
- L'analyste pourra vérifier son analyse avec des données réelles.
- Le développeur pourra tester le code avec des données réelles.
- Le testeur pourra tester l'application avec des données réelles.

Le diagramme ci-dessous illustre l'idée :
![processus valorisant les données réelles](/assets/real-data-value-process.jpg)
Avertissement : ce diagramme n'est qu'une illustration. En pratique, les actions exécutées en parallèle et souvent répétées.

L'analyste utilisera aussi la collecte des données réelles pour amener l'expert métier ou l'utilisateur à détailler **les cas particuliers**, ces cas où les données ne sont pas standards et qui sont souvent la cause de bugs en production car ils passent à travers les mailles du filet.

