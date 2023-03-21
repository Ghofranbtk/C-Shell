# Projet_SE
 Ce mini-projet est à faire sous environnement UNIX en C. L’utilisation de l’appel system() de la
stdlib est proscrit. Votre shell devra utiliser des appels systèmes tel que open(), fork(), exec(),
wait()......
Le shell est un programme qui permet à l’utilisateur de lancer des programmes de manière
interactive. Des exemples de shell courants sont bash, ksh, tcsh, fish, zsh.
 Fonctionalités Basiques du Shell
Le shell doit présenter un prompt à l’utilisateur (terminé par %) puis lire
l’entrée de l’utilisateur. Le shell doit afficher le répertoire courant avant l’invite. Il crée un
processus pour chaque commande linux à exécuter. Puis retourne le prompt pour exécuter votre
prochaine commande.
Si l’utilisateur tape quit, le shell doit sortir.
Il y a deux modes d’exécution : mode interactif et mode batch. 
Dans le mode interactif vous allez taper une commande à exécuter.
Dans le mode batch vous allez fournir le nom d’un fichier batch qui contient des commandes (une par ligne).
Le shell va afficher les commandes et les exécuter une par une puis il se termine (lorsqu’il rencontre la commande quit ou eof).
Une commande peut être simple ou bien la composition de plusieurs commandes. La composition
peut être cmd1 ; cmd2 ou bien cmd1 && cmd2 ou bien cmd1 || cmd2
Vous aurez alors besoin d’un parseur simple qui décompose l’entrée de l’utilisateur en tokens. Les
tokens sont les mots de l’entrée qui sont séparés par des espaces ou des tabulations afin d’exécuter
les commandes composées.
Utilisation de makefile pour construire automatiquement le programme de votre Shell.

Fonctionalités avancées du Shell
a. Dans les deux modes d’exécution le shell doit être capable de rediriger les sorties
standards des commandes vers un fichier ou vers un tube sans noms.
Exemple : ls > fich1 et ls | wc
b. La gestion des erreurs :
Votre système doit afficher un message d’erreur sur la sortie stderr et sortir proprement dans les
cas :
- Fichier batch non existant
- Un nombre inadéquat d’arguments dans l’invite de commande
Le système doit afficher un message d’erreur sur la sortie stderr et continuer l’exécution :
- Une commande n’existe pas ou ne peut pas être exécutée
c. Historique : Donner à l’utilisateur de voir l’historique des commandes exécutées.
