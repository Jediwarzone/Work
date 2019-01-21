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


## Lancer un nouveau projet à partir d'un existant et envoyer un fichier
1. Se mettre sur le bureau ou endroit où on souhaite entreposer le projet de l'autre
2. Faire un git clone à l'adresse du git visé => *git clone https://github.com/vincentcistoldi/Tuto*
3. Tu te rends dans le dossier importé depuis github => *cd NomDossier*
4. Créer un fichier que tu modifie => *mk MonFichier* ou *mkdir MonDossier*
5. Ensuite tu ajoutes à l'index => *git add .*
6. Puis la validation des modifications => *git commit -m "monmessage"*
7. Puis l'envoi des fichiers modifiés vers le dossier distant => *git push*

### Tips
- Déplacer un fichier d'un endroit à un autre **cp /chemin/de/ton/fichier espace /chemin/de/destination**
