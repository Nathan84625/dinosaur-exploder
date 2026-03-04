## Description des issues

## 1. Les succèes qui ne sont pas réinitialiser entre les parties [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/308) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/342)

Dans le jeu, il existe des succès liés au fait de tuer un nombre x de dinosaures, qui se débloquent une fois la condition remplie. Le but de la PR était de faire en sorte qu’un succès complété ne puisse pas être obtenu de nouveau à chaque nouvelle partie. Au début, j’utilisais un fichier .properties pour gérer cela, mais après une discussion avec un membre du projet, nous avons convenu qu’un fichier .ser serait plus approprié. J’ai donc dû modifier le code pour l’adapter à ce nouveau format. De plus, j’ai effectué un test lié aux succès et j’ai remarqué par la suite que mes modifications faisaient échouer d’autres tests, que je suis ensuite allé corriger.


## 2. Ajouter des astéroids au jeu [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/260) [Voir la pr](https://github.com/jvondermarck/dinosaur-exploder/pull/359)

Pour ajouter de la difficulté au jeu, j’ai intégré des astéroïdes qui descendent de l’écran, de la même façon que les dinosaures. Les astéroïdes existent en trois tailles différentes et possèdent un nombre de points de vie proportionnel à leur grosseur. Ils ont également une vitesse aléatoire. Le principal défi dans cette tâche a été l’écriture des tests. Comme des tests unitaires classiques ne permettent pas de vérifier correctement les collisions, j’ai dû apprendre à utiliser la librairie Mockito pour les mettre en place. J’ai aussi rencontré des problèmes avec Maven, l’outil de build, et j’ai dû faire des recherches supplémentaires pour finaliser correctement mon installation.

## 3. Ajouter un nouveau bonus au jeu [Voir l'issue](https://github.com/jvondermarck/dinosaur-exploder/issues/263)

Cette issue n’est pas terminée, mais elle consiste à ajouter un pouvoir qui est rarement lâché par un ennemi. Ce pouvoir invoque un petit vaisseau allié qui combattra aux côtés du joueur pendant une durée limitée.Actuellement, le pouvoir peut être lâché par les ennemis et récupéré par le joueur. Une fois récupéré, aucun autre allié ne peut être lâché par les ennemis.Le vaisseau allié suit déjà le joueur lorsqu’il se déplace, mais il ne peut pas encore tirer ni être touché par les tirs ennemis.
