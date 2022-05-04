# Feedback


- Le fichier JSON était mal formatter, cela renvoyait NULL lorsque j'essayait d'afficher son contenu. En effet, la *virgule* de fin n'est pas autorisée. Donc j'ai corriger le fichier.

- La clé **publishedDate** dans le fichier `jobteaser.json` contenait une date mal formatter et était une `string`. J'ai traiter la date pour la renvoyer au bon format, respectant le même format de date que dans le fichier `regionsjob.xml`.

- Ajout de la méthode `importJobsFromJson()` permettant d'importer les données contenu dans un fichier JSON. Avec l'ajout de cette méthode, j'ai choisi de rénommer la méthode `importJobs()` en `importJobsFromXml` pour qu'elle soit spécifique uniquement pour des fichiers XML.


Etant donnée qu'on dispose maintenant de deux méthodes pour importer des données en fonction du type de fichier, la commande pour lancer l'import devient :

```sh
./run-import.sh <filename>
```

Où **filename** correspond au nom du fichier au format JSON ou XML.

