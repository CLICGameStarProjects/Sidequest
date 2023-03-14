# Tournois-Divers
Site hébergeant les Tournois Divers, des petits tournois locaux ayant lieu ponctuellement

## How-To
Note : les modifications se font automatiquement sur le site Internet lorsque le commit est push.

### Archiver un ancien tournoi
1. Copier le fichier `index.html`, et le coller dans le dossier `old`.
2. Renommer cette copie avec le format `nom-du-tournoi-XXXX.html`, avec XXXX correspondant à l'année du tournoi.
3. Dans cette copie, remplacer tous les `./` par des `../` (pour ne pas casser le lien avec le fichier CSS et les images).

### Créer un nouveau tournoi
D'abord, dans le Drive, créer un nouveau document de bracket. Ensuite, modifier le fichier `index.html` avec les informations du tournoi :
1. Sous `<!-- Informations générales -->` :
    * Balises `<h2>`, le titre (e.g., Tournoi : Nom du jeu).
    * Balises `<p>`, les phases et dates du tournoi (e.g., Qualifications en ligne).
2. Sous `<!-- Règles -->` :
   * S'il y a des règles générales (= pour tous les tournois) à ajouter, les ajouter sous `Règles générales`.
   * Ajouter les règles spécifiques sous `Règles spécifiques au jeu`.
3. Sous `<!-- Arbre de participation -->`, changer le lien du Google Spreadsheets vers celui du tournoi effectif.
4. Si nécessaire, compléter la partie `<!-- Foire Aux Questions -->`.

### Utiliser la page du tournoi
Pour chaque phase/tour, il faut manuellement mettre à jour le site avec la raison et la date de fin. Pour cela, tout en bas, après `<!-- Information du tour en cours -->`, il faut modifier la variable `endDateBase` avec la date de fin de la phase, et la variable `reason` avec le nom de la phase.
