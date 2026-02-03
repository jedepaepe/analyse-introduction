[1-Introduction](./introduction.md)

### Dossier d'analyse

En développement logiciel, un dossier d'analyse est un dossier ou un document ou un site web qui documente l'application. Nous expliquons ici ce qu'est un dossier d'analyse et présentons différentes approches.

##### Table des matières
- [Le pragmatique](#le-pragmatique)
- [Le réduit agile](#le-r%C3%A9duit-agile)
- [Le visuel](#le-visuel)
- [L'académique](#lacad%C3%A9mique)
- [La UX Design](#la-ux-design)
- [Description des sections](#description-des-sections)

Mentionnons quatre objectifs essentiels :

* **Délimiter le périmètre (le scope) de l'application** 
C'est un accord entre le métier (les personnes qui vont bénéficier de l'application) et l'équipe de développement sur ce qui doit être fait.  
Il est important de délimiter ce que fait une application et comment elle le fait pour éviter tout développement inutile, pour pouvoir les coûts et planifier les travaux.

* **Obtenir l'approbation des sponsors** 
Les sponsors sont les personnes qui paient l'application, qui définissent la vision et garantissent l'adéquation entre l'application et la stratégie de l'application. Ils savent à quels besoins l'application répond et en connaissent la valeur (ce que l'application va rapporter à l'organisation).

* **Documenter l'application pour les développeurs et les testeurs** 
Les développeurs ont besoin de description pour savoir ce qu'ils doivent coder.

* **Faciliter le démarrage des nouveaux venus** 
Ils pourront consulter le dossier d'analyse pour comprendre l'application.

> **Note : Approches agiles** 
> De nos jours, beaucoup de projets sont réalisés sur base d'un dossier d'analyse très réduit, mais suffisant pour estimer un budget. Ensuite, les développements sont démarrés et l'analyse est réalisée de manière itérative, en quasi concomittance avec les développements. Cette approche privilégie la communication entre les parties prenantes du projet (stakeholder, principalement les sponsors, les représentants du métier et l'équipe de développement) sur la documentation écrite.

##### Quelques vérités :

* Le dossier d'analyse n'est pas une œuvre d'art, c'est un outil de communication qui doit être rentable.
* Le dossier d'analyse est terminé quand il répond au besoin pas quand il est totalement cohérent et complet.
* Le dossier d'analyse n'est qu'un ensemble de information et de modèles de l'applications, il est toujours faux.
* Le dossier d'analyse est toujours sujet à modification, car l'application est toujours sujette à modification.
* Un dossier d'analyse trop complet n'est pas utilisé.
* Un dossier d'analyse trop simple est inutile.
* La complexité nécessaire d'un dossier d'analyse dépend de la complexité de l'application et des profils des parties prenantes.
* La complexité nécessaire d'un dossier d'analyse balance entre précision et communication.

##### Conseil pour les débutants

* Faisons que ce que nous comprenons.
* Donc utilisons uniquement les modèles que nous comprenons et que l'ensemble des parties prenantes comprennent.

Dans le cours, nous verrons cinq approches différentes de dossiers d'analyse :

* Le pragmatique
* Le réduit agile
* Le visuel
* L'académique
* L'UX design

Voici une courte description de ces approches à titre d'introduction.

---
### Le pragmatique

Le pragmatique est un dossier d'analyse basé sur la pratique telle que je l'ai observée en entreprise. Il est peu respectueux des approches académiques et il fait la part belle à la paresse : en faire le moins possible tout en obtenant un maximum de valeur. Il est aussi basé sur ma pratique de l'analyse dont les débuts datent de 1994 et sur mon expérience de ce cours que je donne depuis 2014.

**Sections du dossier pragmatique :**

1.  Introduction
1.  Processus métier
1.  Backlog
    * Acteurs
    * User stories
    * Scénarios
    * Wireframes
    * Navigation
1.  Contraintes techniques
1.  Design de la DB
1.  Design de l'application
1.  Déploiement
1.  Vérification avec des données réalistes
1.  Glossaire

C'est l'approche qui servira de colonne vertébrale au cours.

**Quand choisir "Le pragmatique" ?**
* Pour une équipe débutante car elle est suffisamment structurée (gardes-fous) et simple (apprentissage rapide).
* Pour une équipe experte souhaitant une approche légère adaptée aux applications de petite et moyenne taille.

---
### Le réduit agile

C'est un dossier réduit au minimum qie pour démarrer un développement itératif :

1.  Introduction
2.  Processus métier
3.  Analyse fonctionnelle (Acteurs, Backlog)
4.  Contraintes
5.  Design de l'application
6.  Déploiement
7.  Glossaire

Cette approche convient bien pour les équipes qui travaillent en agile. Elle permet de démarrer très rapidement les développements et d'avoir les premiers écrans fonctionnels en quelques semaines.

Mais attention, car c'est contre-intuitif, seules des équipes expérimentées réussiront leurs projets avec une telle approche. Et ces même équipes seront souvent amenés à complèter le dossier en cas d'application complexe. En particulier, elles seront souvent amenées à ajouter me design DB.

Notons que la plupart des organisations oublient les processus métier pourtant sans la compréhension de ses processus, un projet est un peu comme un bateau sans gouvernail.

**Quand choisir "Le réduit agile" ?**
* Pour une équipe expérimentée
* Pour une équipe agile, en particulier, il faut un représentant du métier très disponible
* Pour développer rapidement des écrans de l'application et en tirer un feedback

---
### Le visuel

Le visuel est une approche pragmatique basée sur la description de l'interface utilisateur. Elle est très ancienne appliqué par beaucoup d'organisation :

1. introduction
2. processus métier
3. wireframes
4. navigation
5. contraintes
6. design de la DB
7. design de l'application
8. déploiement
9. glossaire

Cette approche a l'avantage d'éviter un maximum les diagrammes abstraits qui peuvent présenter une difficulté pour certaines parties prenantes, en particulier les représentants du métier.

Notons que cette méthode est proche du concept de design first (conception première). Citons les références suivantes :

* [Atomic Design (Brad Frost)](https://atomicdesign.bradfrost.com/chapter-2/)
* [Lean UX (Jeff Gothelf)](https://jeffgothelf.com/blog/leanuxcanvas-v2/)
* [Nielsen Norman Group](https://www.nngroup.com/courses/?_gl=1*1mpzlgp*_up*MQ..*_ga*ODEwODI1MTM5LjE3NzAxMjM5MTY.*_ga_630S9ESVKM*czE3NzAxMjM5MTUkbzEkZzAkdDE3NzAxMjM5MTUkajYwJGwwJGgw&topics=ui-web-design)

**Quand utiliser l'approche "Le visuel"**
* pour des parties prenantes ne supportant pas l'abstraction
* pour des équipes débutantes

---
### L'académique

L'académique est une approche très structurante mais complexe et en conséquence, elle est peu appliquée en entreprise.

1. introduction
2. analyse métier
    1. processus
    2. besoins
    3. classes métier
3. analyse fonctionnelle
    1. contexte
    2. acteurs
    3. use cases
        1. diagrammes de use cases
        2. scénarios
4. analyse technique
    1. UI (User Interface)
        1. wireframe
        2. navigation
    2. contraintes
    3. design de la DB
    4. design de l'application
    5. déploiement
5. glossaire

C'est une approche solide, très cohérente mais complexe et couteuse en temps.

**Quand utiliser l'approche "L'académique" :**
* pour les grands projets
* pour des équipes bien formées aux différents concepts
* à éviter pour les débutants
* à éviter (ou adapter) pour les parties prenantes ne supportant pas l'abstraction
* quand c'est imposé, ce qui est le cas dans beaucoup de grande organisation car ils considèrent que c'est un gage de qualité

---
### La UX Design

L'approche UX (User eXperience) Design est très orientée sur l'interface utilisateur. Elle est applicable pour les sites internets de type vitrine ou institutionnel. Cependant il est possible de l'augmenter des outils des autres méthodes et vis versa. Elle est particulièrement utile là où l'expérience de l'utilisateur est essentielle, par exemple pour le développement de sites e-commerce ou d'application pour smartphone.

1. sketchs
2. wireframes
3. mockups
4. prototype
5. contraintes
6. design de l'application
7. déploiement
8. glossaire

Si l'application est complexe, nous aurons avantage à modéliser la database, à utiliser les user stories et la méthode du user story mapping.

Notons que :

* les mockups coûtent chers
* le prototype est optionnel

**Quand utiliser l'approche "La UX Design" ?**

* pour des applications de marques
* pour des applications à faible complexité fonctionnelle

Il est important de noter que l'approche "UX Design" est différente de l'approche "Le visuel" :
- UX Design est orienté design graphique et peu fonctionnel
- Le visuel est orienté fonction et le design graphique est secondaire

---
### Description des sections

Voici une courte description des différentes sections. La plupart d'entre elles seront vues de manière détaillée par la suite.

* **introduction** : donne le contexte dans lequel l'application est développée
* **analyse métier** : analyse dont le but de documenter le métier, sans référence à l'application excepté qu'on limitera l'étude du métier aux domaines concernés par l'application
* **processus** : des diagrammes d'activités commentés pour décrire les processus (s'il y en a), utilise le diagramme UML d'activité ou BPMN
* **classes métier** : description des concepts métier (ex: client, facture, ...) et leur relations statiques, utilise le diagramme de classe métier
* **analyse fonctionnelle** : analyse des fonctions de l'applique, ce que fait l'applique (=> le quoi)
* **acteur** : un acteur est un utilisateur de l'application ou un système qui interragit avec l'application, on décrira ce qu'ils sont (en dehors de l'application) et leur rôle dans l'application
* **backlog** : liste de user stories à implémenter
* **user story** : une user story décrit une fonctionnalité de l'application
* **use case** : un use case décrit une fonctionnalité de l'application, utilise le diagramme de use cases
* **scénario** : un scénario décrit le déroulement d'une user story ou d'un use case, différentes approches : textuelles, avec le diagramme de séquences
* **analyse technique** : décrit comment l'application est construite
* **sketch** : dessin généralement à main levé d'une interface utilisateur (page, fenêtre, partie de page)
* **wireframe** : dessin non animé dune page/fenêtre de l'application, en général en noir et blanc
* **mockup ou maquette** : dessin animé d'une page/fenêtre de l'application précise au pixel prêt et colorée
* **prototype** : version sans logique exepté la logique de navigation mais qui fournit les affichages avec des données réaliste 
* **navigation** : enchainement des pages/fenêtres, généralement documenté par un sitemap
* **database** : un diagramme ERD commenté
* **contraintes** : quelques contraintes techniques (language, db, framework, performance, quantités de données, transactions, ...)
* **design de l'application** : description de comment