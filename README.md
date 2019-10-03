# Tutoriel-Git
Lier son projet sur vs code avec son repositorie en ssh

PROCEDURE DE CONNEXION SSH GITHUB / Projet en local
Création d'un repositorie (on dit aussi dépôt)
On y dépose les fichiers de son projet
On configure git sur sa machine si ce n'est pas déjà fait en tapant le commandes suivantes:

git config  --global user.name "votre nom"       
git config  --global user.email "votre email"

On génère une clé ssh en utilisant le mail de la config git

ssh-keygen -t rsa -b 4096 -C "votre mail"

On appuie sur Entrée en réponse à toute les questions
ensuite on saisi :

cat /home/votrenom/.ssh/id_rsa.pub

on copie la clé : à partir du mot  "ssh-rsa" à la fin de votre "adresse mail"
on crée une nouvelle clé ssh sur github
rendez vous dans "settings" en developpant le menu de votre avatar
ensuite dans SSH and GPG keys
cliquez sur new ssh key
coller la clé précédemment copiée et donner un nom à cette clé
Valider
Rendez vous dans votre repositorie
copier alors la passphrase: git@github.com:votrenom etc...
faites :    

git clone votre passphrase           pour installer le dépôt en local (souvent dans le workspace)

Et vous avez votre repositorie local lié en ssh à son dépôt d'origine
Ouvrez le projet sous visual studio code (sur le footer bleu il doit y avoir l'icone branche avec master écrit à côté)
ajouté un fichier au projet ou modifier le code d'un autre
une pastille apparaitra alors sous l'icone "contrôle de code source"
le fichier concerné sera vert (selon votre thème de coloration syntaxique ca peut être une autre couleur)
il y a un U à côté de son nom
cliquez sur l'icone
un dock apparait a gauche avec le ou les fichiers modifiés
on clique sur le fichier  et sur le signe +  qui apparaitra a côté
on réitère la procédure du + autant de fois que vous avez de fichier à traiter. le ou les fichiers sont alors en attente
on clique alors sur activer (icône :white_check_mark:  en gris et blanc)
On rédige un commit (c'est un descriptif synthétique mais précis des changements éffectués)
On appuie sur entrée et c'est bon, vous savez utiliser github pour la gestion de votre développement
