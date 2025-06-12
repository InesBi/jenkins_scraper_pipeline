Le fichier scraper.py contient un script Python qui extrait automatiquement la liste des langages de programmation depuis Wikipédia et les sauvegarde dans un fichier CSV nommé data.csv.

Objectif: 
- Modifier ce projet pour l’intégrer dans un pipeline Jenkins.
- Créer un fichier Jenkinsfile à la racine du projet qui automatise les étapes suivantes :

      - Installer les dépendances Python à partir de requirements.txt
      - Exécuter le script scraper.py
      - Archiver le fichier data.csv comme artefact dans Jenkins
