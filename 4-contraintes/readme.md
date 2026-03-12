[top](/README.md)
# Contraintes

#### Table des matières
- [Contraintes](#contraintes)
      - [Table des matières](#table-des-matières)
  - [Introduction](#introduction)
  - [Infrastructure](#infrastructure)
  - [Système d'exploitation](#système-dexploitation)
  - [Langage](#langage)
  - [Low code](#low-code)
  - [Database](#database)
  - [Interopérabilité](#interopérabilité)
  - [Données](#données)
  - [Performances](#performances)
  - [Robustesse](#robustesse)
  - [Sécurité](#sécurité)
  - [Authentification](#authentification)
  - [Internationnalisation](#internationnalisation)
  - [Utilisabilité](#utilisabilité)
  - [Charte graphique](#charte-graphique)
  - [Testabilité](#testabilité)
  - [Maintenabilité](#maintenabilité)
  - [Modularité](#modularité)
  - [Portabilité](#portabilité)
  - [Indépendance](#indépendance)
  - [Qualité](#qualité)
  - [Style Guides](#style-guides)
  - [Déploiements](#déploiements)

## Introduction
Si les use cases permettent de définir les fonctionnalités de l'application,
ils ne précisent rien quant à la solution technique 
or de nombreuses solutions techniques pour un set de fonctionnalités données.

Une première étape consiste à lister des contraintes sur les solutions techniques
afin limiter les solutions possibles.

> Définition CONTRAINTE
> Dans notre contexte, 
> une contrainte est une condition non négociable qui limite le choix de conception.

Notez que nous pouvons aussi lister des préférences, mais c'est plus rare.

Les contraintes sont décidées par les organisations propriétaires de l'organisation.
Elles sont généralement un équilibre entre les spécificités de l'application et la cohérence de l'IT de l'organisation.

Dans les petites organisations, les contraintes seront posées par l'équipe IT ou un prestataire extérieur.
Dans les grandes organisations, ces contraintes seront souvent l'oeuvre des architectes IT et des responsables de la sécurité.

La suite de ce châpitre liste quelques contraintes qui sont classiquement mise en oeuvre.

## Infrastructure
L'entreprise devra choisir sur quelle infrastructure sera déployée l'application. Les choix actuels sont en résumé :
- machines physiques : l'applic
- machines virtuelles
- containers docker
- serverless

## Système d'exploitation
L'entreprise utilisera-t-elle Linux, Windows, Unix ou Mac. 
Ensuite viennent les OS spécialisés pour les systèmes embarqués et temps réels.
Si nous limitons la réflexion sur les applications de gestion, ce sera Linux ou Windows.
L'entreprise choisira en général en fonction de ses compétences du parc d'ordinateurs existants.
Cependant, depuis l'arrivée de docker, Linux prend de plus en plus d'importance.
L'entreprise peut aussi choisir des services cloud de haut niveau comme de l'hébergement d'application web, de docker ou serverless, dans quel cas, c'est le fournisseur cloud qui décide de l'OS.

## Langage
Les organisations imposent généralement le langage de programmation sur base des compétences de l'organisation.
Ainsi si l'organisation a une équipe de développement java, elle développera de manière préférentielle en java.
Bien entendu, l'application peut avoir des spécificités qui peuvent moduler cette contrainte,
car chaque langage de programmation a ses niches. Voici quelques indications dans ce sens :
- java est très utilisés pour les applications de gestion d'organisations (entreprises, grande asbl, ministères, ...), et aussi pour les applications androïd; 
- c# est le concurrent Microsoft de java, il est utilisé pour les même raison et est préféré par les organisations qui choisissent la technologie microsoft; il est aussi utilisé dans les jeux vidéos grace au moteur Unity;
- python est très utilisés pour la data science et l'IA car il possède d'excellentes librairies dans ces domaines (Pandas, TensorFlow, Scikit-Learn);
- c++ pour les jeux vidéos, les systèmes d'exploitations, les systèmes embarqués et les applications à haute performance (finance temps réel) car il est très performant;
- rust prend des parts de c++ car il présente l'avantage d'avoir une gestion de la mémoire automatique;
- javascript est utilisé dans quasiment toutes les applications web car il est le seul langage exécuté par le browser (à l'exception de web assembly); il est utilisé par de petites entreprises mais aussi par des géants du net surtout dans des environnements cloud
- c est toujours utilisé principalement pour des systèmes embarqués et des OS, par exemple Linux est programmé en c. C'est seulement récemment que rust est aussi utilisé.
- typescript est une "alternative" au javascript, il permet d'augmenter la qualité. En pratique, le typescript est transpilé en javascript car les browsers ne savent pas interpréter le typescript.
- php pour des applications web, principalement simples (même si le PHP moderne permet de bien structuré des applications complexes) et étendre les principaux CMS (Content Management System, comme WordPress, Drupal, ...);
- swift pour le développement d'applications pour iOS (pour iPhone et iPad), macOS (ordinateurs apple), watchOS (montre), tvOS, FreeBSD et Ubuntu;
- kotlin pour la programmation Androïd;
- go pour la programmation profitant de la puissance du cloud;

## Low code
L'organisation peut aussi de choisir de développer l'application sur une plateforme low code...

## Database
L'organisation imposera souvent le système de gestion de base de données.

Nous divisons les SGBD en deux groupes :
- SQL : les DB Simple Query Langage;
- NoSQL : les DB Not Only SQL.

Les DB SQL sont divisées en deux groupes :
- les DB server, comme Oracle, SQL Server, Sybase, Posgresql, mariadb, mysql, ...
- les DB embarqués (ou in-process), comme sqlite, dukeDB

Le monde NoSQL est très varié car il existe de nombreux types de DB NoSQL chacune ayant ses avantages et inconvénients.

Si dans la décénie 2010, NoSQL a fait le buz, SQL reste le leader des SGBD, grâce à la garantie ACID.
Le défaut de SQL est qu'il est difficile scalable, à cause justement de l'ACID.

NoSQL est utilisé pour régler des problèmes particuliers, par exemple :
- le temps réel et le cache : redis
- les documents : MongoDB
- le big data : Cassandra et Elisticsearch

Le cloud offre des DB "as a service", par exemple :
- DynamoDB de AWS qui une DB clé/valeur
- Cosmos DB de Azure ...
- Firebase de Google ...

Voici un petit schéma récapitulatif SQL / NoSQ :
| critère | choix |
|-|-|
| popularité | SQL car ancien, standard et beaucoup de compétences disponibles |
| flexibilité | NoSQL car le schéma est plus libre |
| prototypage | NoSQL pour la même raison |
| fiabilité des données | SQL grâce à ACID |
| mise à l'échelle massive | NoSQL car permet l'architecture distribuée |

Notons l'existance du NewSQL qui allie les avantages du SQL (fiabilité) et du NoSQL (mise à l'échelle).

Pour terminer, notons quelques questions à se poser pour le choix SQL ou NoSQL :
- les entités sont-elles stables ou, dit autrement, sommes-nous sur un métier bien maîtrisé ou en pleine évolution ? Plus les entités sont stables, plus SQL est intéressant
- peut-on faire de la cohérence éventuelle (eventually consistent), c'est-à-dire que si vous modifiez les données via un update, un create ou un delete, il n'est pas nécessairement répercuté partout de suite ? Si oui, nous pourrons utiliser les DB NoSQL. Il s'agit ici de choisir entre une DB qui respecte les principes [ACID](https://fr.wikipedia.org/wiki/Propri%C3%A9t%C3%A9s_ACID) ou une DB qui suit les principes [BASE](https://pasksoftware.com/acid-vs-base/#What_Is_BASE).
- grands volumes : des DB NoSQL prévues pour les grands volumes auront l'avantage
- besoin de performance d'interrogation ? les DB NoSQL pourront être avantagées
- besoin de documents qui ne peuvent pas être modifiés, par exemple facture ? Les DB NoSQL de type document offre une solution simple à ce problème. Notons que les DB SQL offre maintenant des tables qui permettent de stocker facilement des documents
- distribution mondiale de la base de données : SQL ne peut pas fournir une réplication de données sur le monde entier sans une dégradation des performances catastrophique (notons que le NewSQL apporte des réponses à ce problème).

## Interopérabilité
Si une application interface une autre application ou des composants électroniques,
il faudra décrire l'interface et les échanges d'un point de vue technique.

On renverra souvent aux documentations de ces applications ou composants électroniques.
S'il n'y en a pas, il faudra documenter pour compléter le dossier d'analyse.

Cela peut être fait dans les contraintes,
puisque nous avons la contrainte d'utiliser telle application ou tel composant électronique.

Parfois, le projet comprendra la modification de l'application en question.
Dans ce cas, il sera préférable de prévoir un chapitre de l'analyse technique
à l'interface avec cette application
et un sous projet pour la modification de cette application.

Parfois, les composants électroniques font partie du projet.
Dans ce cas, il faudra prévoir un chapitre consacré à la description de ces composants
et de leur interface avec l'application.

## Données
Les données sont aujourd'hui sujettes à des contraintes légales : en Europe, le RGPD; au Etats-Unis le CCPA.
Il faudra aussi prêter attention aux droits d'auteurs.
Ensuite nous imposerons, mais c'est plutôt une évidence, l'intégrité et la confidentialité des données.
Nous pouvons aussi exiger que les données soient stocker dans un pays ou une région.

## Performances
L'application devra répondre à des contraintes de performance, typiquement :
- temps de réponse
- quantité de transactions traitées
- quantité de données stockées

## Robustesse
Des contraintes de robustesse pourront être imposées à l'application, par exemple :
- disponibilité généralement exprimée en % (par exemple 99,5% correspond à environ 4h de non disponibilité par an);
- résistance aux pannes hardware
- capacité à redéployer l'application

## Sécurité
L'application devra répondre aux contraintes de sécurité. 

Pour les applications web, les contraintes sont au minimum :
- HTTPS partout, TLS 1.3 obligatoire
- Utiliser les requêtes préparées pour éviter le SQL Injection
- Pas de secret (mot de passe, cléf d'accès) dans le code source
- Utiliser des librairies à jour
- Chiffrement des données sensibles de la DB
- Validation stricte côté serveur (type, longueur, format)
- Echappement en sortie : encoder les données avant l'affichage dans le navigateur pour prévenir le XSS (Cross-Site Scrypting)

Vérifier votre application par rapport au [top 10 de l'OWASP](https://owasp.org/Top10/2025/).


## Authentification
Les applications d'organisation nécessitent presque toujours une authentification.
En général, l'organisation aura un système d'authentication, comme l'Active Directory, Microsoft Entra ID, JumpCloud, Okta, Samba, FreeIPA, OpenLDAP, ... et l'imposera.

Rarement, une application gèrera l'authentification elle même. 
La solution de bases consiste à stocker les utilisateurs et leurs mots de passe criptés dans une base données.

## Internationnalisation
L'internationnalisation a deux aspects :
- les langues supportées par l'application
- les localisations où l'application fonctionne

La gestion des langues se fait au sein de l'application de manière assez simple et via des librairies existantes.

La localisation par contre est un problème de déploiement qui peut impacter l'application, en particulier pour la cohérence des données.
Imaginons une organisation qui a des filiales partout dans le monde, Afrique, Amériques, Asie, Europe et Océanies (et pourquoi Antartique) et que l'application doit être disponible partout... 

## Utilisabilité
Les organisations tenteront de définir la qualité de la UX (User eXperience),
cependant ce n'est pas un sujet simple.

Nous parlerons de "self learning application", c'est-à-dire d'applications qu'on apprend en les utilisant.

Il existe aussi des standards d'accessibilité WCAG/RGAA ou la norme [ISO 25002](https://www.iso.org/fr/standard/78175.html).

## Charte graphique
La plupart des organisations ont une charte graphique qui sera très probablement imposée à l'application.

## Testabilité
L'organisation peut imposer que l'application soit testable ou mieux, 
imposer que des tests unitaires soient écrits.
Nous parlons alors de couverture du code par les tests en %.
L'organisation peut aussi imposer que des tests utilisateur soit écrits. 

## Maintenabilité
L'organisation peut imposer que l'application soit maintenable.
Le problème consiste à définir de manière objective ce qu'est une application maintenable.

## Modularité
L'organisation peut imposer que l'application soit modulaire.
Ici encore, le problème consiste à définir les critères objectifs.

## Portabilité
L'organisation peut imposer que l'application soit portable, 
c'est-à-dire qu'elle est facilement déployable dans d'autres environnements.
Les environnements sont le hardware, donc le type de processeur, les services cloud,
les OS, les DB, les systèmes d'authentification, ...
L'idée est de rendre l'application indépendante de ces environnement.
Mon expérience personnelle est que chaque fois 
que j'ai vu cette contrainte appliquée,
cela a conduit à une augmentation des coûts des développements et la complexité de l'application
sans apporter de valeur ajoutée.
En en effet, cela n'a servi à rien
car soit l'application n'a jamais été portée sur quoique soit d'autre,
soit l'effort pour préparer le portabilité était insuffisant
et il a quand même fallu réécrire.

Bref, si la portabilité peut être un enjeu dans certains cas,
il faut être prudent quant à son implémentation
et mon opinion est qu'un code de qualité et simple est un code plus facile à porter
qu'un code préparé à la portabilité.

Notons que la portabilité peut être une contrainte inhérente au business model.
Par exemple, un éditeur de logiciel souhaitra souvent 
que ses applications fonctionnent sur le plus d'environnements possibles.  

## Indépendance
Il est souvent demandé au logiciel d'être le plus indépendant possible des librairies qu'ils utilisent.
L'idée est de pouvoir facilement changer de librairie.
La technique utilisée est l'écriture de wrapper, du code qui encapsule la librairie.
Ainsi l'application dépend du wrapper et pas directement de la librairie.
Si on veut changer la librairie, il faut seulement modifier le wrapper.
Si cette approche peut fonctionner, elle est exigente et complifie le code.
Il faut donc des développeurs de haut niveau.

## Qualité
L'organisation peut imposer que l'application soit d'une certaine qualité.
Il est possible pour cela de faire vérifier l'application par des analyseurs statiques ou dynamiques.
Le plus connu est sans doute Sonar.

## Style Guides
L'organisation peut imposer des conventions de codage,
c'est-à-dire des règles pour nommer les variables, les classes, ... 
organiser les codes, ...

Souvent, les grands acteurs de l'informatique fournissent des conventions.
L'entreprise aura tout intérêt à les reprendre et éventuellement à les adapter légèrement.
Voici quelques exemples :
- [Apache Java, shell script, Python and database naming conventions](https://cwiki.apache.org/confluence/display/CLOUDSTACK/Coding+conventions);
- [Oracle Java Naming Convention](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html);
- [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)

Il en existe pour tous les langages.

## Déploiements
L'organisation peut imposer des méthodes de déploiements :
- manuelle (souvent une copie d'un zip à travers le réseau et quelques configurations)
- automatisée (un script effectue le déploiement)
- pipeline (le déploiement est automatisé avec des outils qui effectuent différentes étapes)

La dernière méthode est très à la mode
car elle permet d'augmenter la qualité.
Elle est donc quasiment incontournable pour la livraison continue (continous delivery).

Le problème d'un déploiement manuel est qu'il repose entièrement sur la compétence des informaticiens qui le pratique :
- l'application a-t-elle bien été construite (build : compilation, linkage, packaging) ?
- l'application est-elle de la qualité demandée ?
- l'application est-elle sécurisée (pas de failles de sécurités) ?
- l'application respecte-t-elle les critères de qualité, le "style guideline" ?
- l'application a-t-elle bien été testée ?
- y-a-t'il des régressions ?
- déploie-t-on ce qu'on croit ?
- la version (release) déployée est-elle bien documentée (release notes) ?
- le déploiement a-t-il été testé (en déployant sur des machines de tests) ?
- y-a-t'il un plan de rollback (retour à la version précédente) ?
- le rollback a-t-il été testé ?
- le package déployé est-il sauvé quelque part, disponible ?

Lorsqu'on fait un déploiement manuel, toutes ces opérations doivent être faite ... manuellement.
C'est un travail considérable 
et en conséquence, l'application ne sera pas déployée tous les jours, mais plutôt tous les 3 mois.

Avec les pipelines, toutes les opérations mentionnées ci-avant peuvent être automatisées.