# Mon expérience sur c projet

Durant ces exercices, j'ai travaillé uniquement avec le terminal, GitHub, GitHub CLI et à la fin le Vs code

## Exercice 1 : First Repo & Simple Commit
La première chose que j’ai faite a été de connecter mon terminal à mon compte GitHub. Pour cela, j’ai découvert qu’il me fallait l’outil GitHub CLI 'gh'. En vérifiant avec la commande : 'gh --version' Le terminal m’a renvoyé : command not found: gh Cela signifie que GitHub CLI n’était pas installé. J’ai donc commencé par installer Homebrew, un gestionnaire de paquets pour macOS, à l’aide de la commande suivante : '/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"' une fois Homebrew installé, j’ai installé GitHub CLI avec : 'brew install gh' ensuite, je me suis connecté à mon compte GitHub avec : 'gh auth login'
Le terminal m’a posé quelques questions, puis m’a fourni un code à usage unique. Après avoir appuyé sur Entrée, mon navigateur s’est ouvert sur GitHub. J’y ai collé le code et autorisé l’accès pour connecter GitHub CLI à mon compte. une fois connecté, j’ai directement créé mon dépôt avec : 'gh repo create git-learning-1 --public' Puis je l’ai cloné localement avec : 'gh repo clone ismael-s-soon/git-learning-1' Je suis ensuite entré dans le dossier avec : 'cd git-learning-1' J’ai créé un fichier README.md avec la commande : 'echo "My first projet Git" > README.md' Puis j’ai ajouté une autre ligne contenant mon nom et le numéro de mon Mac :'echo "ISMAEL iMAc : 11" >> README.md' Enfin, j’ai fait les étapes Git classiques : 'git add README.md' 'git commit -m "Ajout de mon nom et du numéro du Mac"' 'git push' Sur GitHub, j’ai ensuite vérifié l’historique des commits pour m’assurer que tout s’était bien passé.

**Expérience acquise** 

J’ai appris à connecter mon terminal à mon compte GitHub et à travailler localement.

J’ai appris à créer un dépôt et à le cloner sur mon Mac.

J’ai appris à créer un fichier README.md, à faire un commit et un push pour envoyer mon travail sur GitHub. 

**Difficulté rencontrée**

La seule difficulté que j’ai rencontrée a été l’installation de Homebrew.
L’installation a été perturbée plusieurs fois par des erreurs de connexion réseau, ce qui m’a obligé à relancer plusieurs fois la commande avant que tout fonctionne.

### Exercice 2 : Branching & Merging
Ici, la première étape a été de créer un nouveau dépôt GitHub avec la commande : 'gh repo create git-learning-2 --public' ensuite, je l’ai cloné localement avec : 'gh repo clone ismael-s-soon/git-learning-2' une fois dans le répertoire du projet : 'cd git-learning-2' j’ai créé une nouvelle branche appelée myself : 'git checkout -b myself' dans cette branche, j’ai ajouté un fichier contenant des informations personnelles : 'echo "Moi c’est Ismaël Soumana, je suis né à Maradi" > about.txt' Ensuite, j’ai effectué les étapes de sauvegarde et d’envoi : 'git add .' 'git commit -m "création de la branche myself"' 'git push -u origin myself' après cela, j’ai créé une pull request pour proposer la fusion de ma branche myself dans main : 'gh pr create --base main' puis, je suis retourné sur la branche principale : 'git checkout main' et enfin, j’ai fusionné les changements avec : 'git pull origin main' J’ai terminé en vérifiant l’historique des commits pour m’assurer que tout s’était bien passé.

**Expérience acquise**

J’ai appris à créer et gérer une nouvelle branche.

J’ai appris à faire une Pull Request entre deux branches.

J’ai appris à fusionner une branche dans la branche principale (main).

**Difficulté rencontrée**

Pendant le pull request, j’ai eu un petit problème car la branche principale main n’était pas encore reconnue sur mon dépôt local. Pour corriger cela, j’ai simplement mis à jour la branche principale avec :'git checkout main'
'git pull origin main' après ça, j’ai refait la commande du pull request et tout a bien fonctionné.

#### Exercice 3 : Gestion des conflits lors du fusionnement
J’ai d’abord créé un nouveau dépôt GitHub appelé git-learning-3 avec la commande : 'gh repo create git-learning-3 --public' ensuite, j’ai cloné le dépôt localement : 'gh repo clone ismael-s-soon/git-learning-3' 'cd git-learning-3' sur la branche main, j’ai créé un fichier notes.txt avec cette ligne : 'echo "Ligne écrite depuis la branche main" > notes.txt' 'git add notes.txt' 'git commit -m "ajout de la ligne depuis main"' 'git push' j’ai ensuite créé une nouvelle branche appelée conflict-test : 'git checkout -b conflict-test'
Depuis cette branche, j’ai modifié le fichier notes.txt :'echo "Ligne écrite depuis la branche conflict-test" > notes.txt' 'git add notes.txt' 'git commit -m "modification depuis conflict-test"' 'git push -u origin conflict-test' je suis revenu sur la branche main : 'git checkout main' et j’ai modifié à nouveau notes.txt : 'echo "Ligne écrite depuis la branche principale pour la seconde fois" > notes.txt' 'git add notes.txt' 'git commit -m "modification sur main pour la seconde fois"' 'git push' lorsque j’ai essayé de fusionner les deux branches : 'git merge conflict-test' le terminal a affiché une erreur de conflit, car les deux branches avaient modifié la même ligne du fichier notes.txt. pour ressoudre c erreur j’ai ouvert le fichier notes.txt dans VS Code avec la commande :'code notes.txt'
Le fichier contenait des balises de conflit comme : <<<<<<< HEAD
Ligne écrite depuis la branche principale pour la seconde fois
=======
Ligne écrite depuis la branche conflict-test
>>>>>>> conflict-test
j'ai garder les deux lignes comme la demmander l'ennoncé et j’ai sauvegardé le fichier ainsi : Ligne écrite depuis la branche principale pour la seconde fois  
Ligne écrite depuis la branche conflict-test
Ensuite, j’ai fait : 'git add notes.txt' 'git commit -m "résolution du conflit en gardant les deux lignes"' 'git push'
Enfin, j’ai vérifié sur GitHub et j’ai constaté que le fichier notes.txt contenait bien les deux phrases.

**Expérience acquise**

J’ai appris comment surviennent les conflits lors d’un merge.

J’ai appris à résoudre un conflit manuellement dans VS Code.

**Difficulté rencontrée**

La principale difficulté était le message d’erreur du merge, que je ne comprenais pas au début.
J’ai compris ensuite qu’il fallait ouvrir le fichier concerné, lire les différences, puis choisir manuellement les lignes à garder via ennoncé.

##### Conclusion générale
Ces trois exercices m’ont permis de comprendre et de pratiquer en profondeur Git, GitHub CLI et le GitHub :

  Connexion et configuration du terminal avec GitHub.

  Création et clonage de dépôts.

  Création de branches et Pull Requests.

  Gestion des commits et push pour suivre l’historique.

  Résolution des conflits lors de la fusion de branches.

Cette expérience m’a montré comment travailler même en utilisant uniquement le terminal.




