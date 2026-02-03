[1-Introduction](./introduction.md)

# Cycle de vie d'une application

Comme toute chose, une application nait, se développe, vit et meure. 

#### Table des matières
- [Modèle de référence](#modèle-de-référence)
- [Autres modèles](#autres-modèles)
- [Parties prenantes](#parties-prenantes)
- [Cycle de vie d'une application dans la litérature](#cycle-de-vie-dune-application-dans-la-litérature)


### Modèle de référence

Nous pouvons modéliser ce cycle comme suit :
![cycle de vie d'une application](/assets/application-live-cycle.png)

Le point de départ est l'**idée**. Une ou plusieurs personnes ont une idée. Souvent ils ont l'idée qu'ils ont besoin d'une application pour les aider dans leur métier. Ou ils ont l'idée qu'une ancienne application ne répond plus aux besoins actuels et qu'il faut la remplacer. Ou remplacer une partie. Ou un mixte des deux. L'idée suit son cours et si elle semble bonne, il est possible qu'on décide d'investir de l'argent et du temps à cette idée.

Il faudra alors évaluer la **faisabilité** de l'idée. Il s'agit essentiellement de calculer le budget nécessaire au développement de l'application et vérifier sa valeur ajoutée. L'outil idéal est le ROI (Return Of Investment). Le principe est le suivant : si le retour de l'invetissement est positif, cela vaut la peine de passer à l'étape suivante.

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
- **développement phasé** : l'application est développée en plusieurs étapes avec une mise en services pour chaque étape
- **MVP** : développement d'un MVP (Minimum Valuable Product) qui est mis en service suivi du développement du reste de l'application. C'est en fait un développement phasé en deux étapes avec un attention portée sur la valeur que l'application apporte au métier
- **déploiement continu** : un MVP est développé et mis en service et chaque fonctionnalité complémentaire ou bug est déployé dès qu'il est développé et validé


### Parties prenantes

Les stakeholders en anglais. Ce sont les personnes qui sont impliqués, ici dans le cycle de vie du logiciel.

Notons que le but ici n'est pas d'être exhaustif mais de donner une image concrête.

Les **sponsors** sont ceux qui paient et donnent la vision. Cela diffère d'une organisation à l'autre et d'un projet à l'autre mais on peut citer :
- un **représentant du métier**, cela peut-être le directeur du département qui bénéficiera de l'application, par exemple le directeur des ressources humaines pour une application RH
- un **représentant financier**, cela peut-être le CFO (Chief Financial Officier, le directeur financier)
- un **représentant de l'IT**, cela peut-être le CIO (Chief Informatic Officier, le directeur de l'informatique en langage ancien)
Les sponsors ont pour responsabiliter de conduire le projet. Ce sont eux qui donne la vision, décide du budget et décide de continuer ou d'arrêter le projet.

L'**expert métier** est un ... expert du métier concerné par l'application. Il sera l'interlocuteur privilégier pour comprendre les processus, les concepts du métier et les fonctionnalités de l'application. Notons que parfois, il est nécessaire de travailler avec plusieurs experts métiers, chacun spécialisé dans un métier différent ou une partie différente du métier.

L'**expert évaluation des coûts** aidera à évaluer les coûts, en particulier pendant l'étude de faisabilité. Souvent, ce calcul est fait par un développeur sénior mais c'est réellement un spécialité et c'est très difficile.

Le **chef de projet** est responsable de la conduite au jour le jour du projet.

Les **analystes** sont responsable des ... analyses. Nous verrons cela en plus de détail dans le cours.

Les **développeurs** développent l'application. Ils codent et parfois configure.

Les **testeurs** testent l'application. Souvent les analystes font aussi les tests.

Les **ingénieurs réseaux** sont souvent impliqués car il y a toujours des problèmes avec les réseaux.

Les **ingénieurs en cybersécurité** sont aujourd'hui presque toujours impliqués.

Les **ingénieurs système** gèrent les infrastructures, c'est-à-dire les serveurs, les machines virtuelles, les systèmes d'authentification et les systèmes d'exploitation. Parfois les développeurs font ce travail.

Les **ingénieurs DB** gèrent les ... DB. Parfois les développeurs font ce travail.

Les **ingénieurs devops** gèrent les déploiements automatisés des applications. Les déploiements ne sont pas toujours le cas mais c'est à la mode. Parfois les développeurs font ce travail.

Le **SCRUM master** aide l'équipe à appliquer la méthode SCRUM. Il travaille sur plusieurs projets à la fois. C'est une fonction à la mode mais de plus en plus ce rôle est pris un des membres de l'équipe.

L'**architecte IT** est responsable de l'architecture de l'IT de l'entreprise. Il travaille à tous les niveaux, applicatif et infrastructure.

...


### Cycle de vie d'une application dans la litérature
TODO

