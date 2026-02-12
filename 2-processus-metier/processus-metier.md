[top](/README.md)

# Processus métier
Développer une application sans connaître les processus métier associés est courant cependant cela a un coût car sans cette connaissance, la compréhension des fonctions de l'application est bien plus difficiles. En conséquence, l'analyse fonctionnelle, le code et les tests seront de moins bonne qualité et personne ne le verra avant la mise en production. Ce sera des bugs qu'on aurait pu éviter.

#### Table des matières
  - [Introduction](#introduction)
  - [Modélisation](#modélisation)
  - [Exemple de processus](#exemple-de-processus)
  - [Découvrir les processus](#découvrir-les-processus)
    - [Exemple : le suivi de stage](#exemple--suivi-de-stage)
  - [Le business analyst](#le-business-analyst)

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

![Exemple de diagramme BPMN](/assets/bpmn-specification-example-doctor.png)
*ref: [BPMN specification](https://www.omg.org/spec/BPMN/2.0.2/PDF)*.

Parfois, ils utilisent des diagrammes UML d'activités commentés. Parfois, ils utilisent des diagrammes libres.

Dans ce cours, nous choisissons d'utiliser les diagrammes UML d'activités car c'est un cours avant tout à destination des développeurs.

## Exemple de processus
La demande de congé est une exemple simple de processus.

![Exemple la demande de congé](/assets/ddc-business-process.png)
Nous avons trois intervenants :
- worker : le travailleur qui fait la demande de congé
- manager : le chef du travailleur
- rh : un membre de l'équipe RH (Ressources Humaines)

Les différentes étapes sont :
1) Le worker demande un congé
2) Le manager vérifie si il peut se passer du travailleur pour la période concernée
3) Le manager approuve ou refuse le congé
4) En cas d'approbation, le RH vérifie le solde des congés
5) Ensuite le RH approuve ou refuse le congé

C'est en fait un processus de demande à double approbation.

## Découvrir les processus
Dans de nombreuses organisations, les processus métiers sont documentés, soit par des business analystes, soit les experts de la qualité.

> Les experts de la qualité sont responsable de la qualité au sein de l'entreprise.
Ils ont la responsabilité de rédiger, maintenir et contrôler les procédures et processus qui sont suivis par l'entreprise. L'idée est que le respect de ces procédures et processus est un gage de qualité.

L'analyste fonctionnel demandera aux business analystes, aux quality experts les descriptions des processus. S'il n'y en a pas, il interviewera les experts du métier. Sur base de ces interviews, il cherchera les enchaînements de tâches. Ce sont les candidats "business process".

### Exemple : suivi de stage
Dans le cadre de l'analyse de suivi de stage, imaginons l'interview suivante entre un analyste (A) et un expert métier, un professeur coordinateur de stage (E).

*A : explique les stages
E : les étudiants ont un stage de 360 h minimum en dernières années;
ils doivent avoir réussi les cours PANI, BD, Programmation, Math, Stat, ... pour y accéder
A : comment l'étudiant est-il informé du déroulement du stage?
E : il a accès à la plateforme moodle et il est invité à assister à une séance d'information
A : quand se déroule la séance ?
E : une fois par an, généralement en novembre
A : que présente la scéance
E : nous avons deux power points, les veux-tu ?
A : oui
E : nous avons aussi un vademecum qui est disponible sur le moodle, je vais te donner accès
A : super, on va maintenant essayer de prendre de la hauteur et comprendre les stages de manières générale.
A : quels sont les étapes d'un stage ?
E : l'étudiant doit chercher une entreprise
A : comment fait-il ?
E : c'est un travail en autonomie, un peu comme une recherche d'emploi
A : que ce passe-t-il quand il trouve l'entreprise ?
E : il fait compléter par l'entreprise une document appelé proposition de stage
A : et ensuite ?
E : il poste ce document sur le moodle. Le professeur coordinateur de stage vérifie si cela rentre bien dans le cadre
...*

Nous voyons apparaitre des étapes :
- véfication des conditions d'accès
- séance d'information
- recherche
- proposition

Nous avons donc un premier candidat processus :
```
  conditions accès ===> séance info ===> recherche ====> proposition
```

Mais des questions apparaissent :
A : qui fait la vérification des conditions d'accès ?
E : le secrétaire
A : que se passe-t-il quand le professeur refuse le stage ?
E : l'étudiant doit chercher une autre entreprise

Maintenant, nous pouvons modéliser le processus :

![draft du processus stage](/assets/internship-process-draft.jpg)
Les intervenants sont :
- le secrétaire : de la section de l'école
- l'étudiant : qui suit le cours
- le maître est stage : la personne au sein de l'entreprise où se déroule stage qui est responsable du stage
- le coordinateur de stage : le professeur responsable de la coordination du stage

Les étapes sont :
1) vérifie l'égibilité du stage : le secrétaire vérifie que l'étudiant a bien terminé avec succès les cours prérequis au stage
2) l'étudiant assiste à la séance d'information (notons que cette étape est optionnelle)
3) l'étudiant cherche une entreprise qui accepte un stage
4) l'entreprise remplit la proposition de stage
5) l'étudiant envoie la proposition au coordinateur de stage
6) le coordinateur de stage vérifie si le stage respecte les conditions
7) le coordinateur accepte ou refuse le stage
Si le coordinateur accepte : 
8) l'étudiant continue le stage (la partie qui suit n'a pas encore été analysée)
Si le coordinateur refuse :
8) l'étudiant recommence la recherche d'une entreprise qui accepte un stages

## Le business analyst
Les grandes organisations emploient souvent des analystes métier (business analysts). Ceux-ci analysent le métier de l'organisation ou d'une partie de l'organisation.

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
