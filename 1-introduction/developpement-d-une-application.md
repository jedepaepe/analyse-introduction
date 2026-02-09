[top](/README.md) / [1-Introduction](./introduction.md)

# Développement d'une application

Le développement proprement dit est la troisième activité de notre modèle du cycle de vie d'une application :
![cycle de vie d'une application](/assets/application-live-cycle.png)

Comme son nom l'indique il s'agit de développer l'application.

Il existe deux méthodes de référence pour développer une application.

#### Table des matières
- [Modèle waterfall](#modèle-waterfall)
- [Modèle itératif](#modèle-itératif)

## Modèle waterfall
Le modèle en cascade est un modèle très ancien, développé dans les années 1970.
Il en existe différentes versions qui toutes respectent un même esprit. J'ai donc choisi celui de wikipedia qui est largement accepté :

![Modèle Waterfall](/assets/waterfall-model-wikipedia.png).
Référence : [wikipedia](https://fr.wikipedia.org/wiki/Mod%C3%A8le_en_cascade).

Le modèle s'appelle waterfall car l'idée est celui de l'eau qui coule d'en haut pour tomber dans un premier bassin, puis dans un second, ... L'important dans cette métaphore, c'est que le second bassin ne commence à recevoir de l'eau que quand le premier est le premier est rempli.

Le modèle en cascade décrit le développement logiciel comme une suite d'activités :
1. Les **exigences** sont souvent une liste de besoins
1. L'**analyse** : l'analyse qui répond à la question **quoi ?**, que doit faire l'application. Personnellement, je l'appelle **analyse fonctionnelle**.
2. La **conception** : l'analyse qui répond à la question **comment ?**, comment l'application va-t-elle faire ? En anglais, on dit **design**. Personnellement, je préfère l'appeler **analyse technique**.
3. La **mise en oeuvre** : les développeurs code l'application. J'appelle cette étape **implémentation** ou **développement**.
4. La **validation** : on teste l'application pour vérifier qu'elle fonctionne comme prévu. Beaucoup appelle cette étape **tests**.
5. La **mise en service** : l'application est déployée sur les ordinateurs de production et les utilisateurs peuvent y accéder.

La particularité du modèle est qu'une activité démarre que quand la précédente est terminée. Notons que dans la pratique, aucun projet ne suit strictement le modèle waterfall.

Les points forts du modèle waterfall sont :
- il est très structuré
- toutes les activités mentionnées sont toujours exécutées d'une manière ou d'une autre, quelque soit l'approche

Les points faibles sont :
- l'aspect rigide : "une activité ne peut être démarrée que si la précédente est terminé". Notons qu'on peut très bien décider de ne pas suivre cette règle
- le fait que personne ne voit l'application fonctionner avant le début des tests. Or c'est souvent quand les utilisateurs voient fonctionner l'application qu'ils se rendent compte qu'ils ont oublié quelque chose, un cas particulier, une donnée, un détail, ...
- le manque de communication, car c'est un modèle très orienté documentation.

De nos jours, le modèle waterfall est accusé de faire raté les projets. Personnellement, je ne pense pas que ce soient les modèles qui font la différence, je crois que ce sont les équipes. Ceci dit, il est évident qu'une application rigide du modèle waterfall conduit à compliquer le déroulement du projet et dans la pratique, je n'ai jamais vu le modèle waterfall appliqué à la lettre.

## Modèle itératif
Le modèle itératif est utilisé dans les méthodes de développement agile. Le principe est simple, il s'agit de produire l'application par itérations courtes, généralement de deux semaines.

![Modèle itératif](/assets/iterative-model-summary.jpg)

D'abord, il faut **collecter les US**. Les US sont les user stories. Une user story est une description d'un besoin. C'est un travail préliminaire avant de démarrer les itérations.

Ensuite, l'équipe de développement va itérer les trois activités suivantes :
1. **sélectionner quelques US**. Ces US seront traitées pendant l'itération.
2. **analyser, designer, implémenter, tester** les US sélectionnée. Ces différentes actions sont effectuées plus ou moins séquenciellement.
3. **montrer l'application**. En fin d'itération, l'équipe fait une démo de l'application centrée sur les US sélectionnées.

Si l'application n'est pas "suffisantes", l'équipe commencera une nouvelle itération.
Dans le cas inverse, l'application pourra être **mise en service** et passera en mode maintenance.


## Autres modèles

Parmi les nombreux autres modèles citons :
- le modèle en V
- le modèle en Y
- la livraison continue
- le déploiement continue

Par ailleurs, les modèles vus précédemment peuvent être adaptés à des situations particulières. Le phasage est un cas très courant. Il consiste à mettre en service une première version de l'application. Tandis que la première version part en maintenance, l'équipe développe une seconde version. Quand la seconde version est déployée et part en maintenance, l'équipe développe une troisième version.

