## Liste des tests effectué

Lors de mon premier issue, j'ai modifié les achievement, j'ai donc créé le fichier AchievementTest et fait les 2 issues suivantes :
- achievementSaveInFile dans le fichier AchievementTest
- addAchievementInAlreadyExistingAchievements dans le fichier AchievementTest
Lors de mon deuxième issue, j'ai ajouté des astéroïdes, j'ai donc créé le fichier AsteroidsSpawnerTest et fait les 3 tests suivants :
- spawnAsteroids_LevelOtherThan10_spawnAsteroids dans le fichier AsteroidsSpawnerTest
- spawnAsteroids_levelMultipleOf10_doesNotSpawn dans le fichier AsteroidsSpawnerTest
- pauseAsteroidsSpawning_pausesTimer dans le fichier AsteroidsSpawnerTest
Pour les autres fonctionnalités faites, je n'ai pas fait de test, car tout ce qui utilise le moteur de jeu nécessite des tests d'intégration. La partie compliquée des tests était de comprendre la librairie Mockito utilisée pour les tests. Cela a pris un peu de temps, mais après avoir compris, tout a bien été.
