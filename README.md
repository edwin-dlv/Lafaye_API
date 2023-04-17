# __LAFAYE API__

Code de l'API lafaye permettant de faire le lien entre la base de données et le leaderboard.

## __Getting Started__

Dans ce dossier vous trouverez l'API développée en python en utilisant la framework d'applications web Flask. 

Afin de pouvoir démarre l'API en local, vous devrez suivre les étapes d'installation suivantes.

1. Installer Python sur votre machine: disponible sur `https://www.python.org/downloads/`
2. Installer le framework Flask sur votre machine en utilisant la commande suivante dans votre terminal: `pip install flask` 



## __Appels à l'API__

Une fois l'API lancée vous pourrez faire différents appels permettant de récupérer les données nécessaire au leaderboard.



### __Liste des Meetings__

Appel permettant de récupérer la liste des Meetings enregistrés dans la base de données. 

Exemple de réponse:

`{"Meetings": [{"created_at": "Sun, 09 Apr 2023 23:00:16 GMT","end_date": "Fri, 21 Apr 2023 18:00:00 GMT","id": 2,"name": "Meeting2","updated_at": "Sun, 09 Apr 2023 23:00:16 GMT"},{"created_at": "Sun, 09 Apr 2023 21:44:22 GMT","end_date": "Thu, 20 Apr 2023 17:00:00 GMT","id": 1,"name": "Meeting1","updated_at": "Sun, 09 Apr 2023 21:44:22 GMT"}]}`



### __Liste des groupes__

Pour un Meeting donné, permet de récupérer la liste des groupes enregistrés dans la base de données.

Exemple de réponse:

`{"Groups": [{"created_at": "Sun, 09 Apr 2023 21:46:17 GMT","id": 1,"name": "Grp1","updated_at": "Sun, 09 Apr 2023 21:46:17 GMT"},{"created_at": "Sun, 09 Apr 2023 23:40:36 GMT","id": 6,"name": "Groupe2","updated_at": "Sun, 09 Apr 2023 23:40:36 GMT"}]}`



### __Leaderboard__

Pour un Meeting donné, permet de récupérer le classement général avec les groupes classés par ordre décroissant de points.

Exemple de réponse:

`{"Results": [{"nom": "Grp1","score": 12},{"nom": "Groupe2","score": 0}]}`


Enfin, vous pouvez accéder à l'API publique grâce au lien suivant: 

`http://ec2-52-47-158-117.eu-west-3.compute.amazonaws.com:8000/`
