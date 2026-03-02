README - Mode d'emploi du Launcher
----------------------------------

Ce dépôt contient un utilitaire permettant de lancer facilement différentes applications Windows depuis une interface simple. 
Le fonctionnement est entièrement basé sur un fichier de configuration externe.

CONTENU DU DÉPÔT
----------------
- Launcher.exe : l'application principale.
- config.ini   : le fichier de configuration utilisé pour générer les boutons.

UTILISATION
-----------
1. Téléchargez les fichiers Launcher.exe et config.ini.
2. Placez-les dans le même dossier.
3. Lancez Launcher.exe.
4. Les boutons apparaissent automatiquement en fonction des informations présentes dans le fichier config.ini.
5. Cliquez sur un bouton pour ouvrir l'application correspondante.

CONFIGURATION (config.ini)
--------------------------
Chaque application est définie sous la forme :

[AppX]
caption=Nom du bouton
path=C:\chemin\vers\mon\programme.exe
debug=0

PARAMÈTRES :
- caption : texte affiché sur le bouton
- path    : chemin complet vers un fichier .exe ou .lnk
- debug   : 0 = bouton classique, 1 = bouton debug (icône à droite + demande le numéro de branche locale de debug)

EXEMPLE :
[App1]
caption=Config MTS
path=C:\...\ConfMTS.lnk
debug=0

[App2]
caption=Debug Manufacturing
path=C:\dev_git\XRP-HR-Sprint\Delphi\...\eCGPS5.exe
debug=1

REMARQUES IMPORTANTES
---------------------
- Les boutons sont générés automatiquement à partir des sections du fichier config.ini.
- L’ordre d’affichage suit l’ordre numérique des sections (App1, App2, App3, etc.).
- Les icônes sont automatiquement récupérées depuis les fichiers EXE ou LNK associés.

SUPPORT
-------
En cas de problème, suggestion ou amélioration, merci d’ouvrir une issue sur le repository.