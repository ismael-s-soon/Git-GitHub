# Mon expérience sur c projet

Durant ces exercices, j'ai travaillé uniquement avec le terminal, GitHub, GitHub CLI et à la fin le Vs code

## Exercice 1 : First Repo & Simple Commit
La première chose que j’ai faite a été de connecter mon terminal à mon compte GitHub. Pour cela, j’ai découvert qu’il me fallait l’outil GitHub CLI 'gh'. En vérifiant avec la commande : 'gh --version' Le terminal m’a renvoyé : command not found: gh Cela signifie que GitHub CLI n’était pas installé. J’ai donc commencé par installer Homebrew, un gestionnaire de paquets pour macOS, à l’aide de la commande suivante : '/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"' une fois Homebrew installé, j’ai installé GitHub CLI avec : 'brew install gh' ensuite, je me suis connecté à mon compte GitHub avec : 'gh auth login'
Le terminal m’a posé quelques questions, puis m’a fourni un code à usage unique. Après avoir appuyé sur Entrée, mon navigateur s’est ouvert sur GitHub. J’y ai collé le code et autorisé l’accès pour connecter GitHub CLI à mon compte. une fois connecté, j’ai directement créé mon dépôt avec : 'gh repo create git-learning-1 --public' Puis je l’ai cloné localement avec : 'gh repo clone ismael-s-soon/git-learning-1' Je suis ensuite entré dans le dossier avec : 'cd git-learning-1' J’ai créé un fichier README.md avec la commande : 'echo "My first projet Git" > README.md' Puis j’ai ajouté une autre ligne contenant mon nom et le numéro de mon Mac :'echo "ISMAEL iMAc : 11" >> README.md' Enfin, j’ai fait les étapes Git classiques : 'git add README.md' 'git commit -m "Ajout de mon nom et du numéro du Mac"' 'git push' Sur GitHub, j’ai ensuite vérifié l’historique des commits pour m’assurer que tout s’était bien passé.

Expérience acquise 

J’ai appris à connecter mon terminal à mon compte GitHub et à travailler localement.

J’ai appris à créer un dépôt et à le cloner sur mon Mac.

J’ai appris à créer un fichier README.md, à faire un commit et un push pour envoyer mon travail sur GitHub. 

Difficulté Rencontrer

La seule difficulté que j’ai rencontrée a été l’installation de Homebrew.
L’installation a été perturbée plusieurs fois par des erreurs de connexion réseau, ce qui m’a obligé à relancer plusieurs fois la commande avant que tout fonctionne.
