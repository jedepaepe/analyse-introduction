[top](/README.md) / [1-Introduction](./introduction.md)

# L'analyse dans l'ALC

Quand fait-on de l'analyse ?
En début de projet ?
Pendant la maintenance ?

En pratique, on fait de l'analyse à toutes les étapes de l'ALC (Application Live Cycle). Cependant il est des moments où en fait plus et des moments où on en fait moins.

D'une manière générale, nous pouvons schématiser l'usage de l'analyse comme suit

| activité | intensité | description |
|----------|-----------|-------------|
| faisabilité | f | pour vérifier la faisabilité, nous devons évaluer le budget du projet et donc nous devons avoir une idée des fonctionnalités et de l'architecture de l'application |
| préparation | m | il faut avoir une évaluation plus précise et donc mieux définir l'application tant fonctionnellement que techniquement |
| développement | F | il faut analyser chaque fonctionnalité et chaque solution technique |
| mise en service | 0 | normalement tout a été analysé, c'est une pure exécution d'un plan |
| maintenance | f | l'analyste est nécessaire pour aider les utilisateurs, pour certains bugs très métier et pour des changements |
| démantellement | f | l'analyste est nécessaire s'il y a un projet de migration des données |

(légende f:faible, m:moyenne, F:forte)

Le diagramme suivant illustre la même idée avec une sorte de % de l'activité d'analyse, avec une approche un peu particulière puisque le 100% est atteint à la fin du développement.
![analyse dans l'ALC](/assets/analysis-alc-percent.png)

Les penseurs de la méthode RUP (Rational Unified Process) ont modélisé le type d'effort par itérations :
![RUP Iterative Process](/assets/rup-iterative-wikipedia.png)
Ref : [wikipedia - Rational unified process](https://en.wikipedia.org/wiki/Rational_unified_process)
Evidemment, RUP utilise d'autres noms mais on peut faire correspondre les différentes étapes de RUP avec mon modèle ALC :
- inception : pendant la préparation, éventuellement début des développements
- élaboration : fin de la préparation et début des développements
- constrution : développer
- transition : développer, valider, déployer, former, corriger les bugs

Les différents types d'activités sont :
- business modeling : décrire le métier, elle documente les processus métier, les concepts métier
et les règles métiers
- requirement : capture et formalisation des besoins
- analysis & design : analyse fonctionnelle et technique
- implementation : développement
- test : test
- deployment : installation de l'application sur les systèmes de production
