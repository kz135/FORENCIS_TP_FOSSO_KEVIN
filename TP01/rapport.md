reformulons le sujet 

Lors d'une pause près du parking du commissariat, un agent de police trouve une clé USB sur le sol. Étant conscient des dangers potentiels que peuvent présenter les périphériques USB trouvés, l'agent décide de ne pas brancher la clé sur son ordinateur personnel et de la faire examiner par le service d'analyse forensique du commissariat.

L'objectif de l'analyse forensique sera de déterminer si la clé USB contient des fichiers malveillants ou des données sensibles qui pourraient mettre en danger le système informatique du commissariat ou les informations confidentielles.

Les analystes forensiques utiliseront une méthode scientifique rigoureuse pour examiner la clé USB et en extraire les données, tout en veillant à préserver l'intégrité des preuves. Les résultats de l'analyse seront ensuite présentés aux enquêteurs pour les aider à déterminer la marche à suivre.

lors de la reception du fichier nous allons proceder 

1- dezipper le dossier 
2- recuperer le fichier sans toutefois l executer et scanner en ligne grace a l outil VirusTotal pour voir a quel type de virus on a a faire 
3- en suite ouvrons le terminal et se rendre dans l arborescence du fichier et tapons la commande file #nom du fichier# pour voir le format
4- installer gtkhash #nom du fichier# pour verifier si le hash fourni dans le fichier README est exacte 
5- installer foremost qui va nous permettre d analyser le fichier ensuite executer foremost #nom du fichier# etant dans l aborescence ou se trouve le fichier
6- un dossier output va se creer, se deplacer dans le dossier et vous aurez un fichier audit.txt et 02 dossiers jpg et png ses images aui seront uniauement visibles en ligne de commande 
7- entrer dans le chemin du png et taper lq commande eog #nom image.png#
8- l image sera accesssible  
   

