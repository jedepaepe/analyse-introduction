[top](/README.md)
# Backlog

Dans ce chapitre, nous abordons l'analyse du point de vue de l'approche agile, plus particulière du framework SCRUM.
Nous commencerons par présenter les concepts de base, les acteurs et les récits utilisateurs. Nous verrons deux approches des user stories, l'originale et l'approche de la SCRUM alliance. Ensuite, nous aborderons les techniques pour trouver les user stories.

#### Table de matières
- [Backlog](#backlog)
      - [Table de matières](#table-de-matières)
  - [Agile](#agile)
  - [SCRUM](#scrum)
  - [Acteurs](#acteurs)
    - [Exemples d'acteurs](#exemples-dacteurs)
      - [Demande de congés](#demande-de-congés)
      - [Gestion des stages](#gestion-des-stages)
    - [Acteurs et personas](#acteurs-et-personas)
  - [User stories](#user-stories)
    - [L'approche originelle](#lapproche-originelle)
    - [L'approche courante](#lapproche-courante)
    - [Documentation](#documentation)
  - [Backlog](#backlog-1)

## Agile
L'approche agile est née dans les années 1990. C'est une approche pragmatique, basée sur la pratique des développeurs. Elle part du constat que beaucoup de projets informatiques ratent malgré des études préalables longues et couteuses. Deux concepts me semblent centraux aux approches agiles : la commaunication et le retour d'expérience rapide.

Ils considèrent que la communication directe est le moyen le plus efficace pour échanger de l'information. Ainsi, une équipe de développement est plus performante lorsqu'elle peut communiquer librement avec le "métier".

> Métier
J'utilise ici le terme de "métier", certains disent "client", d'autres "product owner". Je préfère métier car il n'y a pas nécessairement une relation commerciale entre l'équipe de développement et le métier. Quant à "product owner", c'est un terme qui est propre au cadre de travail (framework) Scrum.
Métier veut dire un ou plusieurs représentants du métier, du métier qui va bénéficier du logiciel. Souvent, il s'agit d'experts du métier, les personnes les plus compétentes dans un métier donné.

Le retour d'expérience rapide consiste à développer le plus rapidement possible un morceau de l'application dans le but de le montrer au métier. L'idée est simple : une application fonctionnelle est beaucoup plus parlante que 100 pages d'analyse. Le métier et l'équipe de développement voient concrètement l'application, ses points forts et ses défaut. Dans les méthodes traditionnelles, le métier devait imaginer le fonctionnement de l'application sur base de l'analyse et celle-ci devait être complète ou presque, ce qui est difficile. Avec les approches agiles, il n'est plus nécessaire d'analyser la totalité du logiciel. Nous avons juste besoin :
- d'une idée de la complexité de l'application pour pouvoir évaluer le budget nécessaire au développement de l'application;
- de l'architecture générale de l'application, générale car elle ne doit pas être totalement définie.
Dès que ces deux éléments sont définis, il est possible de démarrer les développements, choisir une ou plusieurs fonctionnalités et les développer le plus rapidement possible, souvent en 4 semaines parfois en 2 semaines. Cela donne une application certes limitée à quelques fonctionnalités mais fonctionnelle. L'équipe de développement montre l'application au métier, ou mieux la met à disposition du métier, par exemple en la déployant sur un environnement de test. Le métier voit l'application. Il peut demander des corrections ou des adaptations. Il comprend mieux son besoin et peut le décrire avec plus de précision. Les développements continuent en parallèle, ajout de nouvelles fonctionnalités et correction ou adaptation de l'existant. Toujours suivant le même principe : montrer le plus vite possible au métier une application fonctionnelle.

Prenons l'exemple de la demande de congés. Nous préparons le projet en listant rapidement les fonctionnalités. Nous fixons l'architecture, par exemple un application java web avec le framework spring boot et qui sera déployée dans un conteneur docker. Sur cette base, nous pouvons évaluer le budget. Ensuite, nous démarrons le développement et choisissons d'implémenter le formulaire de congé et l'envoi d'un email de notification au manager, au RH et au travailleur qui demande le congé. Le développement est réalisé en 2 semaines. En parallèle, l'équipe système a préparé l'environnement de test et de production. L'application est déployée sur les serveurs de tests fin de la deuxième semaine. Le métier demande quelques corrections / modifications. Elles sont implémentée après 4 semaines et l'application est déployée sur les machines de production et mise en service. Le développement continue en parralèle pour ajouter de nouvelles fonctionnalités.

> Budget et agilité
Voilà une question difficile pour les organisations car c'est une véritable révolution. Si nous appliquons totalement l'approche agile, le budget est fixé mais le scope ne l'est pas. Comment cela se passe ? L'organisation voit l'opportunité du développement d'une application. Elle fixe un budget sans fixer le scope, seul le but de l'application est fixé. L'équipe va développer petit à petit l'application en commençant par les fonctionnalités qui apparaissent comme les plus importantes, c'est-à-dire celles qui apportent le plus de valeur. Comme l'équipe produit très rapidement une mini-application, le métier peut en contrôler la valeur et mieux planifier la suite. Le développement peut continuer ainsi longtemps, tant qu'il apporte de la valeur, le métier augmentera le budget. Par contre, si la valeur n'est pas au rendez-vous, le métier pourra prendre la décision d'arrêter le développement avant même que le budget soit consommé.

> Budget classique
Classiquement, l'organisation attend de l'équipe de développement qu'elle estime le coût du développement de l'application, avec un scope si possible bien défini, et les spécialistes savent à quel point il est difficile de bien définir un scope. Ensuite, l'organisation attende de l'équipe de développement qu'elle fasse le développement pour le scope défini au prix estimé. Cette approche génère souvent beaucoup de tension car les évaluations sont souvent trop optimistes.c


## SCRUM
SCRUM, la mélée, comme au rudby, est le framework agile le plus courant, bien plus courant que eXtreme programming ou le DSMD. Son succès est tel qu'il est maintenant utilisé dans bien des domaines qui n'ont rien à voir avec le développement de logiciels.

Une équipe SCRUM est composé d'une équipe de développement, d'un product owner et d'un SCRUM master, ce dernier travaille souvent avec plusieurs équipes SCRUM.
L'équipe de développement développe. Elle est multifonctionnelle, c'est-à-dire qu'elle fait l'analyse fonctionnelle, l'analyse technique, le codage, les tests, les déploiements et parfois, c'est l'équipe qui gère les environnements de test et de production.
Le product owner, qu'on devrait appelé application owner car le produit, c'est l'application, représente le produit, sa valeur et donc il représente le métier. Il fait l'analyse fonctionnelle avec l'équipe, s'implique dans toutes les étapes mais surtout, c'est lui qui met les priorités : "quelle fonctionnalitée doit être développée en premier" ? 
Le SCRUM master est un spéciliste du framework (cadre de travail) SCRUM. Il est là pour aider l'équipe à bien fonctionner, en s'appuyant sur SCRUM. Il répond des questions comme "pouvons-nous déplacer un item du spring backlog au spring suivant ?".

SCRUM définit trois artéfacts importants :
- le product backlog : un ensemble d'éléments (items), lister dans l'idée de les développer pour fabriquer le produit
- l'élement du backlog est une fonctionnalités ou une tâche à développer
- le spring backlog :  quelques items du product backlog qui seront développer pendant l'itération

SCRUM organise le travail en itération généralement de 2 semaines. L'itération est organisé en plusieurs "cérémonies" (réunions si vous préférez) :
- spring planning : c'est l'instant où l'équipe se réunit pour planifier le spring (= itération)
  - l'équipe choisit les items à implémenter
  - l'équipe analyse les items, tant fonctionnellement que techniquement
- daily meeting ou standup : est une réunion organisée d'environ 10 minutes tous les jours à la même heure (c'est plus facile) pour vérifier l'avancement du travail
- spring review : est une réunion pendant laquelle l'équipe revoit et contrôle le travail effectué :
  - souvent l'équipe fait une démonstration des fonctionnalités
  - parfois, elle déploie la nouvelle version de l'application sur un environnement de test
  - rarement, elle déploie la nouvelle version sur l'envisonnement de production
- spring retrospective : est une réunion où l'équipe prend le temps de réfléchir sur sa façon de travailler dans un esprit d'amélioration continue


## Acteurs
Les acteurs sont les personnes et les machines, ordinateurs ou électroniques, qui interragisent avec l'application.

Il faut les lister et décrire leur rôle par rapport à l'application. Nous pouvons aussi décrire leurs besoins et problèmes.

Dans l'application implémentée, les acteurs humains seront très généralement des types d'utilisateurs différents. Chaque type aura des droits différents dans l'application. Par exemple, un client pourra faire des achats. Un vendeur pourra mettre en évidence un produit ou lancer une promotion.

### Exemples d'acteurs
Voic quelques exemples de liste d'acteurs dans différentes applications.

#### Demande de congés
Dans l'application demande de congés, nous listons les acteurs suivants :
- Le travailleur : une personne travaillant dans l'entreprise. Son besoin est d'organiser ses congés.
- le manager : le chef du travail. Son besoin est d'organiser son "service".
- le RH : un employé des ressources humaines. Son besoin est de contrôler la légalité des congés et d'avoir des travailleurs motivés.
- L'administrateur : son travail consiste à administrer l'application, la configurer et résoudre les problèmes techniques.
- La direction : elle a besoin de rapport pour prendre des décisions.
- L'ERP : l'application Enterprise Ressource Planing qui fournit la liste des travailleurs et de leur manager.


#### Gestion des stages
Les acteurs sont :
- L'étudiant. Il a besoin d'aide.
- Le coordinateur de stage : c'est un professeur. Il veut se faciliter la vie et améliorer la qualité de son travail.
- Le maître de stage : la personne responsable du stage dans l'entreprise. Il veut un point centralisé qui lui permet de retrouver l'ensemble des informations et il veut pouvoir communiquer facilement avec l'école. Il est important de noter que les profils de maître de stage est varié. Nous avons les maîtres de stage vrais, qui signent la convention de stage et qui coachent l'étudiant. Nous avons les chefs, qui signent la convention et délègue le coaching à un subalterne. Les RH qui signent la convention et délèguent souvent à un chef qui lui-même délègue ... Peut-être faudrait-il étudier cela plus en détail et les différencier.
- L'administrateur qui configure l'application. Ce rôle peut ce combiner avec "coordinateur de stage".
- les professeurs : il s'agit de l'ensemble des professeurs de la sections. Ils souhaitent savoir ce qui se passe au sein des entreprises et si leurs cours sont adaptés aux réalités du terrains.
- la direction : pour diriger, elle a besoin de rapports.
- Le système de gestion des cours qui fournit la liste des cours, des étudiants et des professeurs titulaires.


### Acteurs et personas
L'acteur est un rôle par rapport à l'application. C'est une entité externe, humaine ou machine qui interragit avec l'application. Le focus est sur ce qu'il fait dans l'application. Exemples : client, vendeur, administrateur, opérateur, serveur de paiement, système météo, ... L'acteur est une notion utilisé en analyse fonctionnelle et technique.

Le persona est notion utilisée en design de l'expérience utilisateur (UX degisn). C'est un archétype avec un nom, un âge, des motivations, des frustrations et un contexte de vie. Le focus est sur l'empathie, les besoins et les problèmes. Par exemple : "Simone est une technicienne de maintenance des stations d'eau potable. Elle a 50 ans. Elle aime son métier mais voit la digitalisation non comme une aide mais comme une contrainte. Cependant, elle doit maintenant rentrer des rapports de maintenance via une application dédicée." L'objectif est de prendre les bonnes décisions de design.

Personnellement, je pense que ce genre de distinction n'a en général guère d'importance. Quand nous abordons l'acteur, nous devons l'imaginer incarné, avec des questions aussi stupide que "porte-t-il des gants", "que fait-il en même temps", "quel est son état d'esprit". Modéliser l'acteur humain comme une machine est une erreur. Selon moi, le persona n'a d'intérêt que quand nous faisons un étude solide d'expérience utilisateur.
Finalement, je rappellerai que dans la bonne vieille méthode d'analyse structuré, les acteurs étaient appelés terminator !

## User stories

![Fowler intro](/assets/user-story-martin-fowler.png)
*ref : [User Story Mapping, Jeff Patton with Peter Economy, O'Reilly](https://jpattonassociates.com/jeff-pattons-book-released-user-story-mapping/)*

> Kent Beck précise :
*Plan using units of customer-visible functionality. "Handle five times the traffic with the same response time." "Provide a two-click way for user to dial frequently used numbers."; ref Extreme Programming Explained, Kent Beck with Cynthia Andress, Addison-Weley second edition.*

Une user story est une "unit of customer-visible functionality", par eExemple :
![exemple de user story](/assets/kent-beck-example-of-story.png)
*Ref : Extreme Programming Explained, Kent Beck with Cynthia Andress, Addison-Weley second edition.*

Kent Beck donne un nom et une courte description à son récit utilisateur. Il insiste sur les estimations car elles sont indispensables pour la planification.

Martin Fowler définit les user stories comme suit :
*User stories sont des parties du comportement souhaité du logiciel. Elles sont largement utilisées dans les approches agiles pour découper un grand nombre de fonctionnalités en éléments plus petits à des fins de planification. On parle aussi de fonctionnalité, mais le terme story (récit) ou user story (récit utilisateur) est maintenant répandu dans les milieux agiles."
*Ref : [Martin Fowler : User Story](https://martinfowler.com/bliki/UserStory.html).


Les points importants sont :
- un récit utilisateur est une fonctionnalitée de l'application
- elle est petite
- elle doit pouvoir être développée indépendamment des autres US
- elle doit pouvoir être estimée
- elle sert à planifier (les travaux de "fabrication" de l'application)
- elle est rédigée du point de vue de l'utilisateur
- c'est une bonne pratique de lui donner un nom court qui donne une idée de la fonctionnalité

Pour pouvoir développer une US, il est nécessaire de la détailler. Ces détails peuvent être écrits sur des documents, typiquement dans le dossier d'analyse, tout comme ils peuvent être des discussions au sein de l'équipe. 

### L'approche originelle
Quand Kent Beck et Ron Jeffries inventent l'idée de user story vers la fin des années 1990, ils insistent beaucoup sur la communication : 

![Manifeste Agile principe communication](/assets/agile-manifesto-communication.png)
*Ref : [Agile Manifesto](https://agilemanifesto.org/iso/fr/principles.html)*

Ron Jeffries invente l'approche des 3'Cs :
- card : les récits utilisateurs sont écrits sur des cartes
- conversation : les exigences sont communiquées oralement du client (expert métier ou product owner) vers les programmeurs
- confirmation : les tests d'acceptation
Pour en savoir plus, lisons l'article de [Ron Jeffries : Essential XP: Card, Conversation, Confirmation](https://ronjeffries.com/xprog/articles/expcardconversationconfirmation/).

La confirmation peut consister en des scénarios de tests avec des données ou en un wireframe avec une description.

### L'approche courante
L'approche originelle est trop radicale pour beaucoup d'entreprise et aujourd'hui, les user stories sont généralement documentées en détail.

La [Scrum Alliance](https://resources.scrumalliance.org/Article/anatomy-user-story) propose un template pour les récits utilisateurs :
![Scrum Alliance](/assets/scrum-alliance-user-story-template.png)

en général réduite à :
> En tant qu'{utilisateur}
> Je veux {action}
> ansi {valeur ou justification}

Voir par exemple [Agile Alliance, user story template](https://agilealliance.org/glossary/user-story-template/).

En fin, ces canvas ne sont que des checklists

Voici quelques exemples pour la demande de congés :
- En tant que travailleur, je veux demander un congé ainsi je saurai s'ils sera accepté ou refusé.
- En tant que travailleur, je veux connaitre le solde de mes congés ainsi je peux organiser mon temps privé.
- En tant que travailleur, je veux connaitre le statut de mes demandes de congé ainsi je sais quelle demandes sont en cours.
- En tant que manager, je veux vérifier que mon service ne sera pas impacter par la prise de congé d'un de mes subalterne ainsi j'assure la qualité de mon service.
- En tant que manager, je veux pouvoir accepter une demande de congé ainsi le travailleur sera informé.
- En tant que manager, je veux pouvoir refuser une demande de congé ainsi la demande pourra être traitée par le RH.

### Documentation
Les récits utilisateurs sont documentés, soit de manière

## Backlog