### Installation de l'environement


#### Prérequis
- **Java >=21** ([Installer](https://jdk.java.net/archive/))
  - Vous pouvez installer java [Open JDK 21](https://jdk.java.net/archive/). Il faut que la version soit 21 ou supérieur.
  - La variable d'environement `JAVA_HOME` doit être définis.
- Git
- Maven
  - Vous pouvez installer Maven sur [Le site officiel de maven](https://jdk.java.net/archive/](https://maven.apache.org/download.cgi)). Utiliser Apache Maven 3.9.12
  - Alternativement, si vous avez chocolatey vous pouvez rouler commande ```choco install maven``` dans une invite de commande
  - Configurer la vriable d'environement MAVEN_HOME pour qu'elle pointe vers le dossier bin de maven


#### Installation
```bash
# 1. Fork le repo sur GitHub
# 2. Clone votre fork
git clone git@github.com:<votre-pseudo>/dinosaur-exploder.git
cd dinosaur-exploder

# 3. Build et lancer
mvn clean install
mvn javafx:run

# Ou utiliser un IDE: 
# - Ouvrir le projet dans L'IDE
# - Rouler com.dinosaur.dinosaurexploder.DinosaurApp
```

### Contribuer

1. **Faire une branch**:  `git checkout -b issue/nom-de-l'issue`
2. **fait vos changements**
4. **Commit**: `git commit -m "Add: description de vos changements"`
5. **Push**: `git push origin issue/nom-de-l'issue`
6. **Ouvrir une Pull Request** sur GitHub

📖 **Guide complet:** [CONTRIBUTING.md](CONTRIBUTING.md)

MIT License - voir [LICENSE](LICENSE) pour les détailles.

