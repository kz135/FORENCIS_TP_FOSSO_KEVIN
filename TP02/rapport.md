j aimerais que les utiliseurs affiche le champ de chaque colonne si la colonne 2 egale a code_iris





awk '{ if($2==code_iris) print $1;}'  consommation-annuelle-residentielle-par-adresse.csv 





