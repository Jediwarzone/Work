# Installation git

1. télécharger sur gitforwindows.org
2. lancer l'installation
3. laisser les paramètres par défaut
4. Une fois terminé

## Les commandes git
- **git config** : lancement de la configuration de git
  - **git config** --global user.name "John Doe"
  - **git config** --global user.email johndoe@example.com
- **git init** : créer un repository
- **git add** . : ajouter des fichiers à l'index ("." signifie Tous les fichiers !!)
- **git commit** : valider les modification apportées (se fait après un add)
- **git commit -m "mon message"**: faire un commit en rajoutant un message
- **git push** : envoyer sur les modifications apportées à la branche principale associée (peut nécessiter une connexion)
- **git status** : affiche la liste des fichiers modifiées ainsi que les fichiers qui doivent encore être ajoutés ou validés.
- **git checkout -b <nom-branche>**: permet de créer des branches
- **git checkout <nom-branche>** : permet de passer d'une branche à une autre
- **git remote** : permet à un utilisateur de se connecter à un dépôt distant
- **git branch** : peut être utilisée pour répertorier, créer ou supprimer des branches
- **git branch -d <nom-branche>** : Pour supprimer une branche
- **git pull** :  Pour récupérer le travail distant
- **git merge <nom-branche>** : Pour fusionner une branche dans la branche active
- **git diff --base <nom-fichier** Permet de lister les conflits
- **git fetch origin** : Permet à un utilisateur d’extraire tous les fichiers du dépôt distant qui ne sont pas actuellement dans le répertoire de travail local
