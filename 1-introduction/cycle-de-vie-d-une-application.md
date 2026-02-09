[1-Introduction](./introduction.md)

# Cycle de vie d'une application

Comme toute chose, une application nait, se développe, vit et meure. 

#### Table des matières
- [Modèle de référence](#modèle-de-référence)
- [Autres modèles](#autres-modèles)
- [Parties prenantes](#parties-prenantes)
- [Cycle de vie d'une application dans la litérature](#cycle-de-vie-dune-application-dans-la-litérature)
- [ALC et stakeholders](#alc-et-stakeholders)


### Modèle de référence

Nous pouvons modéliser ce cycle comme suit :
![cycle de vie d'une application](/assets/application-live-cycle.png)

Le point de départ est l'**idée**. Une ou plusieurs personnes ont une idée. Souvent ils ont l'idée qu'ils ont besoin d'une application pour les aider dans leur métier. Ou ils ont l'idée qu'une ancienne application ne répond plus aux besoins actuels et qu'il faut la remplacer. Ou remplacer une partie. Ou un mixte des deux. L'idée suit son cours et si elle semble bonne, il est possible qu'on décide d'investir de l'argent et du temps à cette idée.

Il faudra alors évaluer la **faisabilité** de l'idée. Il s'agit essentiellement de calculer le budget nécessaire au développement de l'application et vérifier sa valeur ajoutée. L'outil idéal est le ROI (Return On Investment). Le principe est le suivant : si le retour de l'investissement est positif, cela vaut la peine de passer à l'étape suivante.

Nous pouvons maintenant **préparer** le développement de l'application. Un chef de projet est généralement nommé et il sera en charge de planifier le développement. Il devra aussi définir l'équipe qui développera l'application. Le coût du développement de l'application sera recalculé et le ROI revu.

Si le ROI reste positif, les **développements** vont commencer. Au final, ils produiront une application fonctionnelle.

Lorsque l'application est terminée, elle sera **mise en service**. L'application sera déployée (installée) sur les ordinateurs de production et les accès seront donnés aux utilisateurs.

Il faut maintenant **maintenir** l'application, c'est-à-dire aider les utilisateurs, corriger les bugs, modifier l'application suite à des nouveaux besoins et mettre à jour les librairies utilisées pour garantir la sécurité.

Finalement, l'application sera **démantelée**. Elle sera désinstallée. Suivant les cas, une nouvelle application prendra sa place ou simplement arrêtée, par exemple si l'entreprise fait faillite ou, plus couramment si l'activité métier concernée est abandonnée.

> **diagramme UML d'activités
Le diagramme que j'ai utilisé pour illustrer le cycle de vie de l'application est un diagramme d'activité.
J'ai considéré que le développement d'une application est un processus et je l'ai modélisé avec un diagramme d'activité.

Les différentes activités sont menées par des personnes de profils différents et ont des durées différentes :

| activité | profils | durée |
|----------|---------|-------|
| idée | varié | variable, une idée peut prendre des années pour germer |
| faisabilité | expert métier, expert estimation de coût d'application | 1-2 semaines ou plus tout dépend si des études complexes sont entreprises pour évaluer le ROI |
| préparation | chef de projet IT, analyste, expert métier | quelques jours à quelques mois, en fait très variables, suivant les situations |
| développement | chef de projet IT, analyste, développeur, testeur, expert métier, architecte IT, scrum master, administrateur DB, ingénieur système, ingénieur devops, ... | 2 mois à 2 ans, fonction de la complexité de l'application |
| mise en service | ingénieur system, devops | jour(s), en principe c'est rapide et cela a été testé précédemmment |
| maintenance | cf "développement" mais plus besoin d'un chef de projet | certaines applications ont plus de 50 ans de maintenance |
| démantellement | ingénieur système, administrateur DB | rapide sauf s'il faut récupérer les données |


### Autres modèles

Si le [modèle de référence](#modèle-de-référence) est très courant, il existe bien d'autres manières de gérer le cycle de vie d'une application, par exemples :
- **modèle en V** est proche du waterfall, il met l'accent sur la décomposition et les tests de chaque composant
- **modèle en Y** est proche du waterfall, il met l'accent sur le fait que l'analyse technique peut être faite presque indépendamment de l'analyse fonctionnelle
- **développement phasé** : consiste à délivrer en production plusieurs versions de l'application, afin de tirer au plus vite de la valeur. Nous pouvons phasé le modèle waterfall et le modèle itératif. 
- **MVP** : développement d'un MVP (Minimum Valuable Product) qui est mis en service suivi du développement du reste de l'application. C'est en fait un développement phasé en deux étapes avec un attention portée sur la valeur que l'application apporte au métier.
- **déploiement continu** : dans le cas extrême, nous développons une fonctionnalité et nous la mettons directement en service. Ensuite, nous mettons de nouvelles fonctionnalités en service dès qu'elles sont terminées. En général, le déploiement continu n'est appliqué qu'après avoir livré un MVP.


### Parties prenantes

Les stakeholders en anglais. Ce sont les personnes qui sont impliqués, ici dans le cycle de vie du logiciel.

Notons que le but ici n'est pas d'être exhaustif mais de donner une image concrête.

Les **sponsors** sont ceux qui paient et donnent la vision. Cela diffère d'une organisation à l'autre et d'un projet à l'autre mais on peut citer :
- un **représentant du métier**, cela peut-être le directeur du département qui bénéficiera de l'application, par exemple le directeur des ressources humaines pour une application RH
- un **représentant financier**, cela peut-être le CFO (Chief Financial Officier, le directeur financier)
- un **représentant de l'IT**, cela peut-être le CIO (Chief Informatic Officier, le directeur de l'informatique en langage ancien)
Les sponsors ont pour responsabilités de conduire le projet. Ce sont eux qui donne la vision, décide du budget et décide de continuer ou d'arrêter le projet.

L'**expert métier** est un ... expert du métier concerné par l'application. Il sera l'interlocuteur privilégier pour comprendre les processus, les concepts du métier et les fonctionnalités de l'application. Notons que parfois, il est nécessaire de travailler avec plusieurs experts métiers, chacun spécialisé dans un métier différent ou une partie différente du métier.

L'**expert évaluation des coûts** aidera à évaluer les coûts, en particulier pendant l'étude de faisabilité. Souvent, ce calcul est fait par un développeur sénior mais c'est réellement un spécialité et c'est très difficile.

Le **chef de projet** est responsable de la conduite au jour le jour du projet.

Les **analystes** sont responsable des ... analyses. Nous verrons cela en plus de détail dans le cours.
ss
Les **développeurs** développent l'application. Ils codent et parfois configure.

Les **testeurs** testent l'application. Souvent les analystes font aussi les tests.

Les **ingénieurs réseaux** sont souvent impliqués car il y a toujours des problèmes avec les réseaux.

Les **ingénieurs en cybersécurité** sont aujourd'hui presque toujours impliqués.

Les **ingénieurs système** gèrent les infrastructures, c'est-à-dire les serveurs, les machines virtuelles, les systèmes d'authentification et les systèmes d'exploitation. Parfois les développeurs font ce travail.

Les **ingénieurs DB** gèrent les ... DB. Parfois les développeurs font ce travail.

Les **ingénieurs devops** gèrent les déploiements automatisés des applications. Parfois les développeurs font ce travail. Notons que beaucoup d'applications sont encore déployées manuellement.

Le **SCRUM master** aide l'équipe à appliquer la méthode SCRUM. Il travaille sur plusieurs projets à la fois. C'est une fonction à la mode mais de plus en plus ce rôle est pris un des membres de l'équipe.

L'**architecte IT** est responsable de l'architecture de l'IT de l'entreprise. Il travaille à tous les niveaux, applicatif et infrastructure.

...


### Cycle de vie d'une application dans la litérature
Mon ALC (Application Live Cycle) est généralement appelé SDLC dans la littérature. Il existe de nombreux modèles et souvent le waterfall ou le modèle itératif sont considérés comme des SDLC. 

![illustration du SDLC](/assets/wikipedia-sdlc-simple.png)
*Modèle de SDLC, ref: wikipedia Systems Development Life Cycle*

![illustration du SDLC](/assets/wikipedia-sdlc-full.gif)
*Modèle de SDLC, ref: wikipedia Systems Development Life Cycle*

Dans le cas de l'ALC, je prends un vision très globale, applicable finalement à presque tous les projets de développement logiciel ou pas. Nous pouvons faire le parallèle avec des vacances. Imaginez que vous souhaitez aller au sommet de l'Europe, l'Elbrouz à 5642 mètres d'altitude, vous allez :
- avoir l'idée
- vérifier la faisabilité : ai-je assez d'argent, le temps, cela en vaut-il la peine pour cet argent (ROI)
- préparer : sans doute devrais-je faire un peu de sport (formation), je vais planifier, réserver, demander un guide (équipe)
- implémenter : enfin cela y est
Bien entendu, nous n'avons pas l'équivalent de la mise en service et de la maintenance.

Nous pouvons aussi appliquer ce processus à l'achat d'une voiture. Dans ce cas, la mise en service sera l'achat proprement dit et la maintenace, les entretients de la voiture. Par contre, l'implémentation sera courte : aller chez le revendeur et acheter.

Il est inspiré par le framework de gestion de projet PRINCE 2 en ajoutant la maintenance.

![illustration de Prince 2](/assets/wikipedia-prince-2.jpg)
*Framework prince 2, ref : [wikipedia prince 2](https://fr.wikipedia.org/wiki/PRINCE2)*

Voici la correspondance
| prince 2 | ALC |
|-|-|
| commande du projet | idée |
| SU | étudier de faisabilité |
| IP | préparer |
| Exécution | Développer & Metre en service |
| Clôturer | - |
| - | Maintenir |

Il est normal que la maintenance ne fasse pas partie de PRINCE 2 car c'est une méthode de gestion de projet. Par contre, on peut mentionner qu'en général, le projet fera un transfert vers les opérations (et donc la maintenance) typiquement pendant l'étape de clôture.

## ALC et stakeholders
Voici notre ALC surchargé par les parties prenantes et des délivrables typiques à chaque activité :
![ALC avec parties prenantes et livrables](/assets/application-development-process-stakeholders-delivrables.jpg)

Les parties prenantes sont en jaune et les livrables en magenta clair.
PO : Product Owner est responsable de l'application.
PM : Product Manager est responsable du développement de l'application.
Avertissement, le PO et le PM n'ont pas du tout le même rôle et le choix de travailler avec un PM ou PO est essentiellement une question de méthodologie.