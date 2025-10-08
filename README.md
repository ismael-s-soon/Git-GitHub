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
