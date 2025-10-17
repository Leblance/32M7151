# Visualisations des données

Le module [Data visualization](https://omeka.org/s/docs/user-manual/modules/datavisualization/) permet de générer des jeux de données à partir des contenus d’un site et de les représenter sous la forme de diagrammes. La création des diagrammes se fait au sein de chaque site. Ils peuvent ensuite être intégrés dans des pages.
Omeka S propose différents types de diagramme : histogramme, diagramme circulaire ou en barres (horizontales ou verticales), diagramme en arc ou en réseau. Si vous souhaitez travailler avec des dates, par exemple pour voir l’évolution d’un motif dans le temps, il est nécessaire d’installer le module [Numeric Data Types](https://omeka.org/s/docs/user-manual/modules/numericdatatypes/).

## 1. La création des visualisations

**Exemple 1 : La répartition des contenus par lieux de publication**

- Dans le menu de gauche du tableau de bord, dans la section réservée à votre site, cliquer sur « Visualisation des données », puis sur « Ajouter une nouvelle visualisation ».
- Sélectionner « Décompte des valeurs d’une propriété » et cliquer sur « Suivant ».
- Donner un titre à la visualisation.
- Par défaut, le diagramme sera réalisé à partir de tous les contenus présents dans votre site. Si vous souhaitez restreindre le jeu de données à une collection ou à une classe particulière, il faut définir une requête en cliquant sur le bouton « Modifier » de la section « Requêtes à rechercher ». Pour cet exemple, le jeu de données sera créé uniquement à partir de la collection « Gravures espagnoles ».
- Dans le champ « Propriété des valeurs », sélectionner la propriété Dublin Core dont les valeurs sont à compter (Ici, dcterms:spatialCoverage).
- Vous pouvez ensuite choisir le type de diagramme souhaité. Pour chaque diagramme, plusieurs options de personnalisation de l’affichage sont proposées. Par les diagrammes en barre, vous pouvez choisir la hauteur et la largeur, l’ordre d’apparition des données (croissant, décroissant) ou la couleur à l’aide d’une valeur hexadécimale.
- Une fois le paramétrage terminé, cliquer sur « Enregistrer et... ». Cocher la case « Générer un jeu de données », puis choisir entre retourner à la liste des visualisations ou rester sur la page.

----------

**Exemple 2 : Décompter le nombre de contenus en fonction de valeurs précises**

- Créer une nouvelle visualisation et sélectionner « Décompte des contenus avec des valeurs de propriétés ».
- Sélectionner la propriété Dublin Core que vous souhaitez analyser (Ici, dcterms:subject).
- Indiquer les valeurs que vous souhaitez compter dans votre diagramme, en les séparant par des retours à la ligne.
- Sélectionner le type de diagramme. Pour cet exemple, je choisis l’option « Diagramme circulaire ». De nouvelles options apparaissent. La principale différence avec les diagrammes en barre est la gestion des couleurs. Celle-ci passe par des palettes prédéfinies que vous pouvez appeler avec des [mots-clés](https://d3js.org/d3-scale-chromatic/categorical).
- Enregistrer les paramètres pour générer le jeu de données et le diagramme.

----------

**Exemple 3 : Analyser les relations entre gravures et imprimeurs**

Pour générer des diagrammes en arc ou des réseaux, il est nécessaire d’avoir des ressources liées dans ses collections. Omeka S permet en effet de lier des contenus entre eux. Par exemple, vous pouvez lier des personnes avec des objets et indiquer leurs relations à l’aide de propriétés.
La liaison des ressources peut se faire manuellement ou lors de l’import CSV. Pour cet exemple, chaque imprimeur est un contenu associé à la collection « Imprimeurs espagnols ». Ces imprimeurs ont ensuite été liés aux gravures via la propriété dcterms:editor.

- Pour analyser des relations entre des contenus, cliquer sur « Ajouter une nouvelle visualisation », puis sélectionner « Item relationships ».
- Dans la section « Configuration du jeu de données », indiquer la méthode de regroupement : classe de ressource (image, événement, agent, personne, etc.), modèle de ressource ou valeurs d’une propriété. Pour ce cas, l’option « Classe de ressource » a été sélectionnée afin d’analyser toutes les relations entre les classes « image », c’est-à-dire les gravures, et « personne », c’est-à-dire les imprimeurs.
- Sélectionner le type de diagramme (Ici, network graph) et personnaliser les couleurs et la taille si vous le souhaitez.
- Enregistrer et générer le jeu de données.

## 2. La publication des visualisations sur le site

- Lorsque vous éditez une page de votre site web, dans la liste des blocs de contenus, à droite de l’écran, cliquer sur « Visualisation des données ».
- Sélectionner la visualisation dans la liste déroulante et enregistrer. Elle apparaîtra désormais sur la page. Vous pouvez l’enrichir avec du texte et ajouter d’autres visualisations.