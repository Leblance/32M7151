# Création de cartes avec Omeka S

## 1. La géolocalisation des contenus

- Le module [Mapping](https://omeka.org/s/docs/user-manual/modules/mapping) enrichit Omeka S avec des options de géolocalisation et de création de cartes interactives.
- Chaque contenu peut se voir attribuer des coordonnées géographiques :
    
    - Manuellement depuis l’onglet « Carte », qui apparaît lors de la modification d’un contenu ;
    - Automatiquement lors de l’import CSV :
  
        - Option 1 : Import de contenus et des coordonnées
            
            1. Le fichier .csv doit avoir une colonne dédiée à la latitude et à la longitude sous le format suivant : latitude/longitude ;
            1. Après avoir chargé le fichier .csv, dans la liste des options de mapping avec les données du CSV et celles d’Omeka S, cliquer sur le + à côté du nom de la colonne contenant les coordonnées géographiques. Dans le panneau qui apparaît à droite de l’écran, dans la section « Carte », sélectionner l’option « Latitude/Longitude » ;  
            1. Cliquer sur « Importer ».
            1. Les contenus importés s’accompagneront tous d’une carte.
              
        - Option 2 : Ajouter des coordonnées à des contenus préexistants dans la base de données
        
            1. Créer un fichier .csv avec une colonne correspondant à l’identifiant d’un contenu sur Omeka (cote, numéro d’inventaire, titre, etc.), puis ajouter des colonnes supplémentaires pour chaque information que vous souhaitez ajouter aux contenus sur Omeka. Voir [lovers_map.csv](lovers_map.csv) pour un exemple ;
            1. Charger le fichier .csv et le paramétrer pour le mapping, comme expliqué précédemment ;
            1. Avant d’importer, cliquer sur l’onglet « Paramètres avancés » :
              
                - Dans « Actions », choisir l’option « Append » ; 
                - Sélectionner le nom de la colonne où se trouve l’identifiant du contenu ;
                - Sélectionner la propriété Dublin Core qui contient cet identifiant sur Omeka ;
                - Cocher la case « Ignorer la ligne ».
          
           1. Cliquer sur « Importer ».
           1. Les contenus sont maintenant enrichis avec des coordonnées géographiques et une carte.
           
## 2. Affichage des cartes sur le site

1. Première solution : Le parcours des contenus par une carte
    - Depuis les paramètres de navigation de votre site, cliquer sur « Map Browse » dans le panneau de droite pour ajouter un nouvel onglet à votre site affichant une carte avec l’ensemble des contenus de votre site.
    - Indiquer le nom de l’onglet dans le champ « Libellé » ;
    - Choisir le fond de carte dans « Basemap provider ».
1. Seconde solution : Ajouter une carte à une page
    - Lors de l’édition d’une page, il est possible d’ajouter deux « blocs » pour créer une carte :
        - « Carte par requête » : Affichage des contenus sur la carte en fonction d’une requête (par classe, par collection, par type de propriétés ou de valeurs) ;
        - « Carte par sélection » : Sélection manuelle des contenus à afficher sur la carte.
    - Dans les deux cas, une fois le type de carte choisi, des options vous permettent de les personnaliser : choix du fond de carte et du niveau de profondeur du zoom.

Omeka permet de combiner cartes et timelines. Pour cela, il faut activer le module [Numeric Data Types](https://omeka.org/s/docs/user-manual/modules/numericdatatypes/).

