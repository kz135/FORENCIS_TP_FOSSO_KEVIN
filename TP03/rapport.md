Préparation : objectifs et exigences


INTRODUCTION

le site Bosch-Cyber a été compromis et un attaquant aurait réussi à extraire des outils secrets très dangereux. l'administrateur systeme a pris des mesures en mettant le site en maintenance. il est dont question pour nous de découvrir les détails de l'exfiltration effectuée par l'attaquant.

METHODOLOGIE

dans le cadre de l'analyse de notre serveur qui a eu a hebergé notre site actuellement sur maintenant ne devons tout d'abord :

1- verifier le status de notre serveur apache2
2- apres avoir pris la main en ssh sur la VM nous avons un dossier qui attire notre attention nommé b0sch 
 - avec la commande ls -a nous allons lister les dossiers masquéqs et nous allons tomber sur .bash_history que nous allons ouvrir avec la commande cat suivant cette image 
 
3- etant donné que c'est le site qui a été compromis nous allons pplus nous attardé sur les log du serveur apache serveur sur lequel est hebergé le site nous avons principalement 2 journaux de logs :

 
