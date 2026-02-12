[top](/README.md)

# Processus métier
Développer une application sans connaître les processus métier associés est courant cependant cela a un coût car sans cette connaissance, la compréhension des fonctions de l'application est bien plus difficiles. En conséquence, l'analyse fonctionnelle, le code et les tests seront de moins bonne qualité et personne ne le verra avant la mise en production. Ce sera des bugs qu'on aurait pu éviter.

#### Table des matières
- [Processus métier](#processus-métier)
      - [Table des matières](#table-des-matières)
  - [Introduction](#introduction)
  - [Modélisation](#modélisation)
  - [Le business analyst](#le-business-analyst)
  - [Découvrir les processus](#découvrir-les-processus)
    - [Exemple : suivi de stage](#exemple--suivi-de-stage)

## Introduction

> Définition
Un processus métier est un ensemble d'activités permettant à une organisation d'atteindre un objectif.
*basée sur [redhat La gestion des processus métier, qu'est-ce que c'est ?](https://www.redhat.com/fr/topics/automation/what-is-business-process-management).*
Processus d'affaraires, processus business (business process) sont aussi utilisés.

Regardons chaque terme important :
- processus :
    - (3) Suite ordonnée d'opérations aboutissant à un resultat (processus de fabrication); *ref: [Le Robert](https://dictionnaire.lerobert.com/definition/processus)*.
    - (2) Suite continue d'opérations, d'actions constituant la manière de faire, de fabriquer quelque chose (Les processus de fabrication deoivent être revus); *ref: [Larousse](https://www.larousse.fr/dictionnaires/francais/processus/64066).
    - En sciences de gestion, un processus est l'organisation d'un ensemble d'activités contribuant aux objectifs d'une organisation. Ces processus peuvent êter de nature commerciale, technique ou administrative, voir combiner l'ensemble des aspects. Les termes suivants sont couramment utilisés de façon interchangeable : processus métier, processus d'entreprise, ou processus d'affaires ("business process" en anglais); *ref : [wikipédia](https://fr.wikipedia.org/wiki/Processus#%C3%89conomie_et_gestion)*.
- métier :
    - (1) Genre de travail déterminé, reconnu ou toléré par la société et dont on peut tirer des moyens d'existence; *ref [Le Robert](https://dictionnaire.lerobert.com/google-dictionnaire-fr?param=m%C3%A9tier)*.
    - (1) Activité sociale définie par son objet, ses techniques, etc. : Qu'est-ce qu'il fait comme métier ?, *ref [Larousse](https://www.larousse.fr/dictionnaires/francais/m%C3%A9tier/50997)
    - Un métier désigne l'exercice par une personne d'un activité dans un domaine professionnel, en vue d'une rémunération. Par extension, un métier désigne le degré de maîtrise acquis par une personne ou une organisation du fait de la pratique sur une durée suffisante de cette activité comme l'expérience et le savoir-faire acquis et l'amélioration des pratiques. *Ref: [wikipédia](https://fr.wikipedia.org/wiki/M%C3%A9tier_(activit%C3%A9))*.
    - C'est la définition de wikipédia qui s'approche le plus du sens de métier dans notre contexte car toutes ces définitions sont insatisfaisantes car elles se concentrent sur une personne. Il s'agit ici du **domaine professionnel**, par exemple l'entretien de jardins, la gestion des ressources humaines, la fabrication de vélos, l'achat, l'exploration de l'espace, ...
- activité
    - (1) faculté ou fait d'agir; *ref [Le Robert](https://dictionnaire.lerobert.com/google-dictionnaire-fr?param=activit%C3%A9)*.
    - (2) Actes coordonnés et travaux d'origine humaine; *ref [Le Robert](https://dictionnaire.lerobert.com/google-dictionnaire-fr?param=activit%C3%A9)*.
    - (3) Action de quelqu'un, d'une entreprise, d'un pays dans un domaine défini; champ d'action : Activités professionnelles. Une usine qui étend son activité à de nouveaux secteurs; *ref [Larousse](https://www.larousse.fr/dictionnaires/francais/activit%C3%A9/947)*.
- organisation :
    - (2) association, groupement qui se propose des buts déterminés, une organisation syndicale; ref [Le Robert](https://dictionnaire.lerobert.com/google-dictionnaire-fr?param=organisation)
    - dans ce cours, une organisation est une entreprise, une association sans but lucratif, un ministère, ... comme dans la définition du Robert.

Nous avons donc quatre niveaux :
- organisation
    - processus
        - activité


*Attention, il ne faut pas confondre le processus métier et le processus informatique. Le processus informatique est une tâche en cours d'exécution. C'est une notion de système d'exploitation.*

## Modélisation
Les analystes utilisent en général des diagrammes BPMN commentés pour documenter les processus :
![Exemple de diagramme BPMN](/assets/wikipedia-bpmn-exemple.jpg)
*Exemple de schéma BPMN pour un processus métier, l'achat; ref [wikipédia](https://fr.wikipedia.org/wiki/Business_process_model_and_notation).
Les spécifications du BPMN sont gérées par l'OMG (Object Management Group) et son disponible online; [OMG BPMN](https://www.bpmn.org/).

![Exemple de diagramme BPMN](/assets/bpmn-specification-example.png)
*ref: [BPMN specification](https://www.omg.org/spec/BPMN/2.0.2/PDF)*.

[Exemple de diagramme BPMN](/assets/bpmn-specification-example-doctor.png)
*ref: [BPMN specification](https://www.omg.org/spec/BPMN/2.0.2/PDF)*.

Parfois, ils utilisent des diagrammes UML d'activités commentés. Parfois, ils utilisent des diagrammes libres.

Dans ce cours, nous choisissons d'utiliser les diagrammes UML d'activités car c'est un cours avant tout à destination des développeurs.

## Le business analyst
Les grandes organisations emploient souvent des analyste métier (business analysts). Ceux-ci analysent le métier de l'organisation ou d'une partie de l'organisation.

Leurs principales responsabilités sont :
- définir les règles métier
- modéliser les processus métier
- aider à l'amélioration du métier
- analyser les besoins du métier
- rédiger des business cases
- réaliser des études de faisabilité
- rédiger des spécifications
- faciliter la communication entre le métier et l'IT
- valider les changements, par exemple la mise en service d'une nouvelle application
- accompagner le métier dans le changement
- gérer le risque

Dans beaucoup d'organisations, l'analyste métier fait aussi l'analyse fonctionnelle des applications.

## Découvrir les processus
Dans de nombreuses organisations, les processus métiers sont documentés, soit par des business analystes, soit les experts de la qualité.

> Les experts de la qualité sont responsable de la qualité au sein de l'entreprise.
Ils ont la responsabilité de rédiger, maintenir et contrôler les procédures et processus qui sont suivis par l'entreprise. L'idée est que le respect de ces procédures et processus est un gage de qualité.

L'analyste fonctionnel demandera aux business analystes, aux quality experts les descriptions des processus. S'il n'y en a pas, il interviewera les experts du métier. Sur base de ces interviews, il cherchera les enchaînements de tâches. Ce sont les candidats "business process".

### Exemple : suivi de stage
Dans le cadre de l'analyse de suivi de stage, imaginons l'interview suivante entre un analyste (A) et un expert métier, un professeur coordinateur de stage (E).

*