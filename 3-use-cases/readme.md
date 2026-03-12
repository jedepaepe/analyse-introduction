[top](/README.md)
# Use cases

#### Table des matières
- [Use cases](#use-cases)
      - [Table des matières](#table-des-matières)
  - [Introduction](#introduction)
  - [Acteurs](#acteurs)
  - [Use cases](#use-cases-1)
    - [Bon use cases](#bon-use-cases)
  - [Scénarios](#scénarios)
  - [Wireframes](#wireframes)
  - [Données réelles](#données-réelles)

## Introduction
Les use cases ont été développé fin des années 1980 par Ivar Jacobson. L'idée est de lister les fonctionnalités, de représenter graphiquement leurs relations avec le monde extérieur et d'utiliser ces use cases pour gérer le développement de l'application.
Je donne ici un point vue personnel qui insiste sur la simplification et l'atomicité. Ainsi je recommande de ne pas utiliser les concepts avancés des use cases comme l'inclusion et l'extension car ils complexifient les diagrammes et par conséquent, les rendent moins efficaces pour la communication, tout cela pour une valeur ajoutée très discutable. L'atomicité consiste à chercher des fonctionnalités atomique. L'avantage est qu'elles sont souvent plus petites et permettent dès lors un meilleur suivi de l'avancement des travaux. Cela permet aussi d'avoir une directive claire dans la recherche des use cases, ce qui facilite le travail des débutants. Une fois expert, chacun pourra se faire son opinion et choisir l'approche convenant à son contexte.
Finalement, il faut mentionner que les use cases sont de moins en moins utilisés depuis une quinzaine d'années. Ils sont concurrencés par les user stories. J'ai choisi de présenter les use cases avant les user stories car les user stories sont attachées aux approches agiles et qu'elles doivent être présentées dans ce cadre là, même si leur usage c'est étendu ces dernières années. A mon sens, la différence principale entre use cases et user stories est que les use cases sont principalement orientés documentation alors que les user stories sont principalement orientées planification. Nous reviendrons sur ce point dans le chapitre consacré aux approches agiles.

## Acteurs
Un acteur représente une personne ou un système qui interragit avec l'application.
Une personne est donc un utilisateur de l'application. Nous n'allons pas nommé l'acteur par son nom bien entendu, nous allons catégoriser les utilisateurs. En effet, les applications ont généralement différents types d'utilisateurs. Par exemple, une application de vente en ligne aura sans doute les utilisateurs suivants :
- l'internaute qui accède à l'e-shop sans s'être authentifier, il consulte le catalogue, voit les promotions et peut remplir son panier
- le client qui a accès aux fonctionnalités listées ci-avant mais aussi à l'achat, la visualisation de ses facteurs passés, l'accès au service après-vente
- le vendeur qui s'occupe de modifier le catalogue, les prix, les étalages (la façon de présenter les produits), les promotions ...
- le service après vente qui prend en charge les demandes de support
Nous avons donc différents types d'utilisateurs. Ces utilisateurs ont accès à différentes fonctionnalités de l'application. Ils interragissent différemment avec l'application.

Beaucoup d'application interragissent avec d'autres systèmes, souvent d'autres applications parfois des systèmes électronique. Si nous reprenons le cas de notre e-shop, beaucoup d'entreprises connectent leur e-shop à l'application de gestion de l'entreprise, qu'on appelle ERP pour Enterprise Ressource Planning.

Lister les acteurs d'une application est donc essentiel pour comprendre une application. L'analyste débutera souvent son travail en cherchant les différents acteurs. Nous décrirons au minimum le rôle joué par l'acteur dans l'application. Une phrase suffit dans la majorité des cas car le détail de l'interaction entre les acteurs et l'application sera décrit dans les use cases.

Par exemple, dans une application de demande de congés nous pourrions avoir les acteurs suivant:
- salarié : un employé de l'entreprise, c'est lui qui effectue les demandes de congé
- manager : le manager du travailleur, c'est lui qui approuve ou refuse les demandes de congés
- rh : un membre des ressources humaines, c'est lui qui vérifie si le travailleur a droit à son congé
- administrateur : une personne qui gère les paramètres de l'application, ce peut être un expert des ressources humaines
- ERP : le système ERP de l'entreprise (Enterprise Ressource Planning), l'application reçoit la liste des employés et de leur manager.


## Use cases
Les use cases où cas d'utilisation sont exactement ce que leur nom indique : ce sont des utilisations du système. Un use case est une fonctionnalité de l'application mais toujours vue dans son interaction avec le monde extérieur, c'est-à-dire avec les acteurs.
Les use cases sont très généralement représenter dans le diagramme de use cases qui liste les use cases et leurs relations avec les acteurs.
![use case diagramme](/assets/use-case-diagram-demande-de-conges.png)

**ref: [anciennes notes](https://jedepaepe.github.io/analyse-introduction-legacy/AF02-use-cases/index.html)**

Les acteurs sont généralement représentés des "bons hommes" et les use cases par des ovals. Les liens indique qui est impliqué dans le use case. Par exemple le use case "consulte calendriers congés" implique le salarié.

Le diagramme de cases donnent une vue synthétique et graphique des fonctionnalités de l'application. Notons qu'une application complexe aura beaucoup de use cases et nous aurons avantage à réaliser plusieurs diagrammes de use cases différents. L'analyste classera les use cases par différents thèmes, typiquement par acteurs et par domaine. Une application a souvent différent domaine, par exemple l'authentification, le métier principal (ici la demande de congé), les rapports (le décisionnel).

Pour organiser les use cases, nous pouvons aussi utiliser la notion de package :
![use case diagram book shop](/assets/use-case-diagram-book-shop.jpg)**
**ref : [anciennes notes](https://jedepaepe.github.io/analyse-introduction-legacy/E01-book-shop/index.html)
Nous avons les packages :
- catalogue
- panier
- gestion compte
- achat
Les packages sont simplement sacs dans lesquels nous mettons les use cases.

Notons que les diagrammes de use cases ne sont pas les use cases. Un use case est une fonctionnalité du système. Le diagramme de use cases ne fait que lister les use cases de manière graphique. Il permet de visualiser rapidement le contexte de l'application, c'est-à-dire les acteurs, et les fonctionnalités de l'application, c'est-à-dire les use cases. Le diagramme ne suffit pas, il faut encore décrire chaque use case. Différentes approches sont possibles et nous en verrons deux ici : les scénarios et les wireframes. Nous verrons aussi comment vérifier les use cases à l'aide de données réelles.

### Bon use cases
Qu'est-ce qu'un bon use case. Les avis sont assez variés sur la question et je vais donner ici ma vision personnelle. Elle a l'avantage d'être facile à comprendre et sera un bon guide pour les débutants, je l'espère. Les experts feront à leur guise, toujours dans l'objectif d'adapter l'outil à leur contexte.

Un bon use case est atomique, indépendant et testable :
- atomique : il forme un tout, il est difficilement divisible sans compromettre la cohérence
- indépendant : il ne dépend pas des autres cas d'utilisation, on peut le jouer tout seul
- testable : on peut le jouer tout seul, vérifier les résultats du use case à partir des entrées (input) fournies lors de l'exécution du use case.

Voyons ceci avec un exemple, "le salarié demande un congé" :
- atomique : pouvons-nous diviser ce use case, peut-être si nous avons différents types de demande de congé qui nécessite des scénarios différents, par exemple "demander un congé normal", "demander un congé de maternité", "demander un congé éducation", ... Nous le verrons donc quand nous détaillerons le use case
- indépendant : nous pouvons jouer la demande de congé sans jouer un autre use case
- testable : nous pouvons exécuter le use case en vue de test, nous savons qu'il faudra introduire des données et nous savons que ces données pourront être consultées, par exemple en jouant le use case "visualiser le calendrier des congés".

Notons que ces directives sont proches de l'INVEST utilisé pour les user stories (voir par exemple [invest wikipedia](https://en.wikipedia.org/wiki/INVEST_(mnemonic))). 

## Scénarios
Les scénarios décrivent le déroulement d'un use case lorsqu'il est instancié, c'est-à-dire lorsque le use case est joué par les acteurs. Nous décrivons donc les interactions entre les acteurs et l'application, au cours du temps. Par exemple, le use case "le salarié demande un congé" suivra un scénario de type :
1. le salarié introduit son matricule
2. l'application affiche le nom et prénom du salarié et affiche le formaulre de demande de congé
3. le salarié introduit les dates de début et de fin de congé, le type de congé (choix dans une liste) et optionnellement un commentaire
4. l'application vérifie :
   - que la date de fin est plus grande ou égale à la date de début (et affiche un message d'erreur dans le cas contraire) 
5. l'application affiche le bouton "envoyer" si les données sont valides, sinon le salarié doit corriger les données invalides
6. le salarié envoie le formulaire
7. l'application envoie un email de confirmation au salarié avec un lien vers la demande de congé
8. l'application envoie un email de notification au manager de l'employé avec un lien vers l'approbation de la demande de congé

Notons qu'un use case peut avoir plusieurs scénarios. Nous parlerons souvent de scénario principal ou happy flow, c'est-à-dire le scénario attendu, celui qui apporte de la valeur et des scénarios particuliers ou d'erreurs.

Dans la suite, je présente un modèle pour les scénarios de use cases. Il a l'avantage de guider les débutants et le désavantage d'être un peu contraignant.


## Wireframes
Les wireframes sont une représentation graphique de l'interface utilisateur qui précise les composants graphiques principaux et nécessaires au fonctionnement de l'application sans trop se préoccuper de la présentation. Ce n'est donc pas une image exacte de l'interface utilisateur, d'ailleurs ils sont souvent fait en noir et blanc.

## Données réelles
L'analyste a tout intérêt à collecter des données si pas réelles, au moins réalistes. Sur cette base, il pourra écrire des scénarios avec données ce qui a de nombreux avantages :
1. vérifier ses scénarios (n'a-t'il rien oublié, le scénario fonctionne-t-il avec les données réelles ?)
2. écrire l'embryon des scénarios de test
3. fournir des données réelles aux développeurs qui pourront les utiliser pour alimenter leur base de données de test, qu'ils utiliseront lorsqu'ils testeront localement, sur leurs ordinateurs de développement, l'application
4. fournir des données réelles pour la base de données qui servira pour effectuer les tests

