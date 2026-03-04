[top](/README.md)

# Backlog

Le backlog 

## User stories

![Fowler intro](/assets/user-story-martin-fowler.png)
*ref : [User Story Mapping, Jeff Patton with Peter Economy, O'Reilly](https://jpattonassociates.com/jeff-pattons-book-released-user-story-mapping/)*

### Canvas pour les user stories
Beaucoup utilisent un canvas standardisé pour les récits utilisateurs :
> En tant que [acteur]
> Je veux [action / fonctionnalité]
> Afin [bénéfice / valeur ajoutée]

Notons que ce canvas n'est pas obligatoire et qu'il est même parfois inadapté. Cependant il est utile car il est standard et il nous guide pour bien résumé la US.

Par exemple ...

### Qualité d'une user story
Pour vérifier la qualité de nos récits utilisateur, nous utiliserons les critères INVEST :
- Independant : la US doit être indépendante des autres, nous pouvons la développer sans devoir développer une autre
- Negociable : la US n'est pas un contrat figé, il doit être possible de négocier le détail fonctionnel de la US, le design de la solution et même le fait qu'on décide de ne pas l'implémenter
- Valuable : elle doit apporter de la valeur, si possible aux utilisateurs
- Estimable : il doit être possible d'estimer le coût du développement de la US
- Small : elle doit être la plus petite possible
- Testable : elle doit être testable
Tous les critères sont en fait des règles logiques qui permettent de faciliter et gérer le développement d'un logiciel et elles sont en générale suivie par les équipes excepté la règle *negociable*. Beaucoup d'organisations ont du mal à passer à de l'agile vrai. Elles continuent à planifier et refusent d'adapter les plans au fur et à mesure et elles considèrent que les fonctionnalités ne sont pas négociables. C'est aussi souvent le cas quand le logiciel est payé pour un prix fixe.

Prenons l'exemple de la US "demander un congé" :
En tant que travailleur, je veux pouvoir demander un congé afin de pouvoir planifier une activité privée.

Independant : nous n'avons pas besoin d'autres US pour jouer cette US. Bien sûr, nous aurons des préconditions, typiquement que le travailleur a un compte et qu'il s'est authentifié mais la dépence ne va plus loin qu'une précondition.

Negociable : il est possible de discuter de cette US (bien entendu, cela dépend beaucoup de la culture de l'organisation).

Valuable : elle a de la valeur pour le travail et l'entreprise. Pour le travailleur, ce n'est pas une valeur immédiate. Il attend la réponse. Mais cela a malgré tout une valeur car il sait qu'il aura une réponse. Pour l'entreprise, la US a une valeur car permet une meilleure organisation.

Estimable : il est possible d'estimer le coût des développement car nous avons une idée relativement précise de ce que c'est : il s'agit d'un formulaire, son contenu sera mis en DB et des notifications seront probablement envoyées. Pour estimer correctement la US, il faudra la détailler. Quelles sont les données ? Y-a-t-il de la validation des saisies utilisateurs ? Y-a-t'il des notifications ? Comment ? Y-a-t'il de l'audit ? Quelle est la performance attendue ? Quelle est la qualité de la UX ? Quelle est la qualité du design (branding, charte graphique) ? Y-a-t'il plusieurs langues ? Quelle est la distribution géographique des utilisateurs ?

Small : pouvons-nous diviser cette US ? Il est toujours possible de découper une US mais nous avons ici une unité qui est fonctionnellement logique. Nous ne la découperons que si elle ne peut pas être réalisée en un sprint.

Testable : elle est bien entendu testable, il suffit de la "jouer".



### Comment trouver les user stories
Comment puis-je trouver les user stories pour une nouvelle application ?
- lister les acteurs
- créer un user story map
- faire des ateliers
- analyser ce qui existe (documentation sur des applications semblables, la concurrence)
