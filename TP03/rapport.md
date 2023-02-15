Préparation : objectifs et exigences


INTRODUCTION

le site Bosch-Cyber a été compromis et un attaquant aurait réussi à extraire des outils secrets très dangereux. l'administrateur systeme a pris des mesures en mettant le site en maintenance. il est dont question pour nous de découvrir les détails de l'exfiltration effectuée par l'attaquant.

METHODOLOGIE

dans le cadre de l'analyse de notre serveur qui a eu a hebergé notre site actuellement sur maintenant ne devons tout d'abord :

1- verifier le status de notre serveur apache2
2- apres avoir pris la main en ssh sur la VM nous avons un dossier qui attire notre attention nommé b0sch 
 - avec la commande ls -a nous allons lister les dossiers masquéqs et nous allons tomber sur .bash_history que nous allons ouvrir avec la commande cat suivant cette image :
 - 
 ![image](https://user-images.githubusercontent.com/80653459/219064376-171c67c6-2396-4580-b41f-414ca2e2a313.png)
 
cette image qui nous montre qu'on a une personne qui c'est introduit dans le fichier host en suite passwrd et a egalement touché au fichier html du site 
nous constatons egalement qu'il y'a un dossier qui a été zippé avec un mot de passe puis le mot de passe a été supprimer par la site et enfin l'utilisation de crontab -e quipermet d'executer les taches en intervalle de temps regulier 
 
3- etant donné que c'est le site qui a été compromis nous allons pplus nous attardé sur les log du serveur apache serveur sur lequel est hebergé le site nous avons principalement 2 journaux de logs :

![image](https://user-images.githubusercontent.com/80653459/219066453-5682db72-a0da-4357-a762-2c84d1578747.png)

4- nous devons lister les logs de access.log car contient les log des acces et des modification apporté comme étant donné que le fichier long est volumineux nous allons le filtrer pour retouver le password supprimer avec la commande grep et nous remarquerons que c'est l'adresse ip recuperer au debut qui creer ce fichier zip avec un mot de passe

![image](https://user-images.githubusercontent.com/80653459/219068249-f2804c23-d999-46ca-acc7-33cfb3a4d4be.png)

mot de passe en question

![image](https://user-images.githubusercontent.com/80653459/219070454-2be1fafe-bb78-43bb-964f-e5afcb422d7e.png)


5-nous allons egalement lister les erreurs de connection nous pouvons deduire de cette image que l'attaquant a pu avoir plusieurs adresse ou a utiliser un VPN

![image](https://user-images.githubusercontent.com/80653459/219069293-752aaa93-ceca-4941-a74c-d53636b25a99.png)

6- on va se rendre dans le dossier ou se trouve le  zip et dezipper mais nous n'avons pas le droit de l'extraire dans le dossier opt/leak nous allons le faire dans home/bosh
avec la commande :

![image](https://user-images.githubusercontent.com/80653459/219071245-946d3230-3ec9-49ff-8fad-2ae857b6dc26.png)
![image](https://user-images.githubusercontent.com/80653459/219071326-3d4d4625-1681-4ba3-9a5c-053352706334.png)


contenu du fichier zip

![image](https://user-images.githubusercontent.com/80653459/219071723-393af2ef-85c9-46e4-8120-b87da152e837.png)

CONCLUSION 

en somme il etait question pour nous de voir toutes les modification dont notre cite a subit pendant sont attaque nous avons remarqué le creation d'un dossier qui contenait un fichier txt 



 
