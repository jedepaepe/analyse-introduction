[top](/README.md)
# Backlog

Dans ce chapitre, nous commencerons par présenter les concepts de base, les acteurs et les récits utilisateurs. Nous verrons deux approches des user stories, l'originale et l'approche de la SCRUM alliance. Ensuite, nous aborderons les techniques pour trouver les user stories.

#### Table de matières
- [Acteurs](#acteurs)
    - [Exemples](#exemples-dacteurs)
        - [Demande de congés](#demande-de-congés)
        - [Gestion des stages](#gestion-des-stages)
    - [Acteurs et personas](#acteurs-et-personas)
- [User stories](#user-stories)

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