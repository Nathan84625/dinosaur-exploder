## Liste des tests effectué

Lors de mon premier issue, j’ai modifié la gestion des succès. J’ai donc créé le fichier AchievementTest et réalisé les deux tests suivants :
- achievementSaveInFile dans AchievementTest
- addAchievementInAlreadyExistingAchievements dans AchievementTest
Lors de mon deuxième issue, j’ai ajouté les astéroïdes. J’ai alors créé le fichier AsteroidsSpawnerTest et réalisé les trois tests suivants :
- spawnAsteroids_LevelOtherThan10_spawnAsteroids dans AsteroidsSpawnerTest
- spawnAsteroids_levelMultipleOf10_doesNotSpawn dans AsteroidsSpawnerTest
- pauseAsteroidsSpawning_pausesTimer dans AsteroidsSpawnerTest
Pour les autres fonctionnalités, je n’ai pas écrit de tests, car tout ce qui utilise directement le moteur de jeu nécessite des tests d’intégration. La partie la plus complexe a été de comprendre la librairie Mockito utilisée pour les tests. Cela m’a pris un peu de temps, mais une fois assimilée, tout s’est bien déroulé.

