reformulons le sujet g

Lors d'une pause près du parking du commissariat, un agent de police trouve une clé USB sur le sol. Étant conscient des dangers potentiels que peuvent présenter les périphériques USB trouvés, l'agent décide de ne pas brancher la clé sur son ordinateur personnel et de la faire examiner par le service d'analyse forensique du commissariat.

L'objectif de l'analyse forensique sera de déterminer si la clé USB contient des fichiers malveillants ou des données sensibles qui pourraient mettre en danger le système informatique du commissariat ou les informations confidentielles.

Les analystes forensiques utiliseront une méthode scientifique rigoureuse pour examiner la clé USB et en extraire les données, tout en veillant à préserver l'intégrité des preuves. Les résultats de l'analyse seront ensuite présentés aux enquêteurs pour les aider à déterminer la marche à suivre.

lors de la reception du fichier nous allons proceder 

1- dezipper le dossier 

2- recuperer le fichier sans toutefois l'executer et scanner en ligne a  l'aide de l'outil VirusTotal pour voir a quel type de virus on a à faire 

![Capture](https://user-images.githubusercontent.com/80653459/218672985-23162e24-5d9d-4e14-8688-3ed50fc6b136.PNG)


3- en suite ouvrons le terminal et se rendre dans l arborescence du fichier et tapons la commande file #nom du fichier# pour voir le format

4- installer gtkhash #nom du fichier# pour verifier si le hash fourni dans le fichier README est exacte
![Capture 1](https://user-images.githubusercontent.com/80653459/218673880-d2bff66b-95ed-48f4-9492-a063c85fadb4.PNG)


5- installer foremost qui va nous permettre d analyser le fichier ensuite executer foremost #nom du fichier# etant dans l aborescence ou se trouve le fichier

" **SOUS UBUNTU** "

il existe plusieurs methodes pour le faire :

**PREMIERE METHODE**

6- un dossier output va se creer, se deplacer dans le dossier et vous aurez un fichier audit.txt et 02 dossiers jpg et png ses images aui seront uniauement visibles en ligne de commande 

7- entrer dans le chemin du png et taper la commande "eog nom image.png"

8- l'image sera accesssible et visible depuis le dossier en interface graphique
   
**DEUXIEME METHODE** 

9- le fichier output va se créer contenant le fichier audit.txt et 02 dossiers jpg et png, donner les droits d'execution de modificationet de lecture au dossier avec la commande "chmod 777 output"

10- entrer dans le dossier output et donner les memes droits au dossier png et jpg "chmod 777 nomdossier"

11-ouvrir le dossier png et les images seront accessibles grace a un double clique en interface graphique "deposé le dossier output dans un emplacement facilement accessible par vous"

12 - vous retrouverez le flag 'l'image en question'
![00016520](https://user-images.githubusercontent.com/80653459/218674158-01a307fd-69ea-428b-afed-09917317aa65.png)

" **SOUS KALI LINUX** "

apres avoir installer foremost et executer la commande "foremost USB_Image"

donner juste les droits d'execution, modificationet lecture aux Dossiers Output et Png en utilisant la commande "chmod 777 output" entrer dans output et saisiser "chmod 777 png"

aller dans la zoneou a été extrait son ZIP et aller jusqu'au fichier PNG les images seront visibles 

