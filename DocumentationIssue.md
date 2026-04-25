## Description des issues

## 1. Les succèes qui ne sont pas réinitialiser entre les parties [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/308) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/342)

Dans le jeu, il existe des succès liés au fait de tuer un nombre x de dinosaures, qui se débloquent une fois la condition remplie. Le but de la PR était de faire en sorte qu’un succès complété ne puisse pas être obtenu de nouveau à chaque nouvelle partie. Au début, j’utilisais un fichier .properties pour gérer cela, mais après une discussion avec un membre du projet, nous avons convenu qu’un fichier .ser serait plus approprié. J’ai donc dû modifier le code pour l’adapter à ce nouveau format. De plus, j’ai effectué un test lié aux succès et j’ai remarqué par la suite que mes modifications faisaient échouer d’autres tests, que je suis ensuite allé corriger.


## 2. Ajouter des astéroids au jeu [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/260) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/359)

Pour ajouter de la difficulté au jeu, j’ai intégré des astéroïdes qui descendent de l’écran, de la même façon que les dinosaures. Les astéroïdes existent en trois tailles différentes et possèdent un nombre de points de vie proportionnel à leur grosseur. Ils ont également une vitesse aléatoire. Le principal défi dans cette tâche a été l’écriture des tests. Comme des tests unitaires classiques ne permettent pas de vérifier correctement les collisions, j’ai dû apprendre à utiliser la librairie Mockito pour les mettre en place. J’ai aussi rencontré des problèmes avec Maven, l’outil de build, et j’ai dû faire des recherches supplémentaires pour finaliser correctement mon installation.

## 3. Ajouter un nouveau bonus au jeu [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/263) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/378)

Cette issue consiste à ajouter un pouvoir qui est rarement lâché par un ennemi. Ce pouvoir invoque un petit vaisseau allié qui combattra aux côtés du joueur pendant une durée limitée. Actuellement, le pouvoir peut être lâché par les ennemis et récupéré par le joueur. Une fois récupéré, aucun autre allié ne peut être lâché par les ennemis. Le vaisseau allié suit le joueur quand il se déplace et tourne quand le joueur tourne en mode expert. De plus, l'allié peut tirer en même temps que le joueur et possède 2 points de vie. Le vaisseau perd des points de vie comme le joueur. Un défi inattendu lors de cette issue a été l'ajout du mode expert pendant que je travaillais dessus. Le mode expert permet au joueur de bouger sur 360 degrés, ce qui signifie que j'ai dû aller comprendre comment la rotation fonctionnait et ajuster le code.


## 4. Ajouter des particules de flammes quand le vaisseau est touché [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/261) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/386)

Cette issue consiste à ajouter des particules de flamme sur le personnage quand il perd des points de vie. Si le joueur a perdu 2 points de vie, le feu est plus intense et si le joueur se soigne, les flammes disparaissent. La librairie de jeu possède une fonctionnalité pour faire des particules de feu, cependant il y avait beaucoup de variables à comprendre. Après avoir pris du temps dans la documentation et fait des tests pour comprendre comment faire le feu, j'arrivais à faire des particules, mais aucun résultat n'était satisfaisant. Je suis donc allé "brainstormer" avec une IA pour m'aider à rendre les particules un peu plus vivantes. J'ai dû modifier ce qu'elle me proposait, mais cela m'a permis d'atteindre un résultat satisfaisant. Après ça, j'ai fini en essayant de documenter le code, mais j'ai fini par laisser la documentation assez simple en documentant uniquement les fonctions et les variables importantes. La PR a mis beaucoup de temps à se faire vérifier, car le propriétaire était parti en vacances. À son retour, nous avons discuté du ticket et j'ai dû adapter le code pour que les particules de flammes fonctionnent aussi quand on prend le bonus en début de partie qui nous donne 2 points de vie de plus.



