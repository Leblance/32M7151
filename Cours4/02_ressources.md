# Les ressources
Omeka S repose sur 4 types de ressources que vous pouvez gérer depuis la page principale du tableau de bord ou depuis l'espace "Ressources", dans le panneau à gauche du tableau de bord :

- Les contenus (*items*) : Éléments de base d'Omeka. Ils peuvent prendre la forme d'objets (*physical objects*), accompagnés de médias, ou d'entités (personnes, lieux, concepts).
- Les médias : Contenus multimédias (numérisations, vidéos, etc.). Ils sont toujours attachés à un contenu et ne peuvent exister indépendamment dans la base de données. Vous pouvez importer des images via une URL, via IIIF ou en téléversant un fichier. Omeka accepte les [formats suivants](https://omeka.org/s/docs/user-manual/content/media/#media-file-types) :
    - Images : JPEG, PNG, TIFF, WEBP.
    - Vidéos : MP4, WebM, Ogg.
    - Sons : MP3, AAC.
- Les collections (*item sets*) : Ensemble de contenus. Un contenu peut appartenir à plusieurs collections.
- Les modèles de ressource (*resource templates*) : Liste de métadonnées prédéfinies.

## 1. La liste des contenus
Lorsque vous cliquez sur l'onglet "Contenus", dans le panneau de gauche, vous accèdez à la liste de l'ensemble des contenus disponibles dans la base de données d'Omeka S, c'est-à-dire les vôtres, mais aussi ceux des autres. À côté du titre d'un contenu, trois icônes vous permettent d'interagir avec lui :

- Le crayon ![https://img.icons8.com/?size=20&id=59856&format=png&color=000000](https://img.icons8.com/?size=20&id=59856&format=png&color=525252) : Éditer un contenu.
- La poubelle ![https://img.icons8.com/?size=20&id=14237&format=png&color=000000](https://img.icons8.com/?size=20&id=14237&format=png&color=525252) : Supprimer un contenu.
- Les trois points horizontaux : Vue rapide des métadonnées. Pour une vue détaillée, il faut cliquer sur le titre du contenu.

La liste indique également la classe de la ressource, ainsi que son propriétaire. En effet, lorsqu'un utilisateur crée un nouveau contenu, il en devient son propriétaire (*owner*). En fonction de votre rôle utilisateur, vous n'aurez pas les mêmes droits. Par exemple, les administrateurs, les superviseurs et les éditeurs peuvent modifier et supprimer n'importe quel contenu. Les relecteurs et les auteurs ont des droits uniquement sur les contenus qu'ils ont créés.

Chaque contenu est décrit avec un ensemble de métadonnées appartenant à des vocabulaires issus du [Linked Open Data](https://lov.linkeddata.es/dataset/lov) : Dublin Core, BIBO et FOAF. Ces vocabulaires définissent de manière standardisée et contrôlée un ensemble de classes et de propriétés pour décrire des entités ou des types de contenus spécifiques. Pour cette formation, nous utiliserons uniquement le Dublin Core. Pour aller plus loin, je vous invite à consulter la [documentation d'Omeka S](https://omeka.org/s/docs/user-manual/content/vocabularies/).

**Point sur le Dublin Core**

Le Dublin Core est apparu en 1995 et devient une norme ISO en 2003. Il est maintenu par un consortium appelé le [DCMI](https://www.dublincore.org/). À l'origine, il proposait un ensemble minimal de quinze métadonnées applicables un large nombre de domaines. Ces quinze éléments sont tous facultatifs et répétables. En 2001, de nouveaux termes sont créés pour compléter les éléments d'origine. On parle alors de *Dublin Core Extended*. Rapidement, les éléments d'origine et les éléments "étendus" fusionnent. Ils sont aujourd'hui regroupés sous l'espace de nom suivant : http://purl.org/dc/terms/. La [liste de l'ensemble des termes](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/) du Dublin Core et leurs spécification est disponible sur le site du DCMI.

Les quinze éléments d'origine :

- dc.title : Nom donné à un contenu
- dc.creator : Entité principale responsable de la création du contenu (Personnes, organisations)
- dc.subject : Thèmes (Mots-clés)
- dc.description : Description du contenu intellectuel
- dc.source : Référence à une ressource dont le contenu est dérivée (institutions de conservation)
- dc.publisher : Entité responsable de la mise à disposition ou diffusion du contenu
- dc.date : Date d’un événement dans le cycle de vie de la ressource (ex : date de création, de mise à disposition, etc.)
- dc.contributeur : Entité responsable d'une contribution au contenu
- dc.rights : Informations sur les droits associés au contenu (Licence)
- dc.relation : Référence à une ressource apparentée
- dc.format : Manifestation (ou matérialisation) physique ou numérique
- dc.type : Type de contenu
- dc.language : Langue du contenu
- dc.identifier : Référence univoque au contenu
- dc.coverage : Périmètre ou domaine d’application du contenu, c’est-à-dire la couverture spatio-temporelle

Rien que pour le Dublin Core, Omeka S propose 55 propriétés différentes ! Pour éviter les erreurs et faciliter le travail de création et de description, il est recommandé de créer un modèle de ressource.


## 2. Les modèles de ressource
Les modèles de ressource vous permettent de prédéfinir une ensemble de métadonnées pour décrire un type de contenus (livre, gravures, médailles, images, sons, etc.). Vous pouvez ainsi cibler uniquement les champs de métadonnées dont vous avez besoin. La liste des modèles disponibles est accessible depuis l'onglet "Modèles de ressource" (panneau de gauche du tableau de bord). Pour créer un nouveau modèle, cliquez sur "Ajouter un nouveau modèle de ressource".

Le panneau à droite du tableau de bord propose la liste de l'ensemble des propriétés du Dublin Core disponibles. Pour ajouter une nouvelle propriété à votre modèle, cliquez simplement sur son nom. Le crayon vous permet de personnaliser chaque champ. Vous pouvez lui donner une description alternative, indiquer si le champ est requis ou privé, ainsi que spécifier le format de données autorisé (URI, texte, vocabulaires contrôlés, référentiels).
Lorsque vous avez choisi les propriétés nécessaires, cliquez sur le bouton "Ajouter" en haut à droite. Vous pourrez re-modifier le modèle plus tard si besoin.

## 3. Créer une collection
Lorsque vous affichez la liste des collections, en cliquant sur l'onglet correspondant dans le panneau de gauche, un bouton "Ajouter une collection" apparaît en haut à droite. Lorsque vous cliquez dessus, un formulaire avec des métadonnées s'affichent : 

1. Sélectionner les métadonnées nécessaires et remplissez les champs.
1. Depuis l'onglet "Vignettes", vous pouvez ajouter une petite image de couverture, illustrant votre collection et qui apparaîtra dans la liste des collections.
1. Pour valider votre collection, cliquez sur "Enregistrer" (en haut, à droite).


## 4. Ajouter des contenus
### 4.1. Méthode manuelle

1. Depuis la liste des contenus, cliquer sur le bouton "Ajouter un nouveau contenu", en haut à droite.
1. Dans l'onglet "Valeurs", sélectionner le modèle de ressources appelé "Gravures".
1. Remplir les champs avec les informations fournies sur la gravure que vous avez choisie.
1. Cliquer sur l'onglet Médias. Plusieurs options d'import vous sont proposées :
    - "Charger" : Importer un média depuis votre ordinateur ;
    - "URL" : Ajouter une image via un URL ;
    - "HTML" : Code HTML ;
    - "IIIF Image" : URL vers une image IIIF (Le lien doit pointer vers le fichier d'information de l'image ```info.json```).
    - "IIIF Presentation" : URL vers un manifeste IIIF.
1. Pour cet exemple, ajouter un média via un URL.
1. Dans l'onglet "Collections", associer votre contenu à une collection.
1. Dans l'onglet "Sites", spécifier le site où le contenu sera affiché.    
1. Pour valider votre contenu, cliquer sur "Ajouter" (toujours en haut, à droite).

Si vous vous rendez maintenant sur votre site, le contenu créé apparaîtra dans la liste des contenus de votre site, à la fois dans le back-end et le front-end.

### 4.2. Import par lot : CSV Import
Par défaut, Omeka propose un noyau de fonctionnalités (création de contenus, de sites et de collections ; liaison des données avec des vocabulaires de base ; affichage de médias) qui peuvent être enrichies et personnalisées grâce à des [modules](https://omeka.org/s/modules/).

[CSV Import](https://omeka.org/s/docs/user-manual/modules/csvimport/) est un module permettant d'importer en une fois plusieurs contenus et leurs métadonnées. Pour cela, les données doivent être structurées dans un fichier ```.csv```.

**La préparation des données**

Chaque ligne de votre fichier ```.csv``` correspond à un contenu, à une collection ou à un média ; chaque colonne, à une métadonnée. Pour faciliter le mapping entre les noms des colonnes et les propriétés Dublin Core sur Omeka, il est recommandé de nommer vos colonnes de la manière suivante : ```prefix:property```. Par exemple : ```dcterms:title```, ```dcterms:author```, etc.
Ce module autorise les imports soit de contenus, soit de médias, soit de collections, soit un mélange des trois (*mixed resources*). Si vous choisissez d'importer plusieurs types de ressources, votre fichier ```.csv``` doit inclure deux colonnes spécifiques :

- Une colonne indiquant l'identifiant du contenu auquel un média est lié (Pour rappel, un média doit obligatoirement être rattaché à un contenu).
- Une colonne indiquant le type de ressources (item, item set, media).

Pour un exemple de fichier CSV, voir le fichier xxxx.

----------

**Import des données dans Omeka**

- Étape 1 : Paramétrage de l'import
    - Importer le fichier ```.csv```
    - Indiquer le caractère utilisé pour séparer les colonnes (ici, le point-virgule)
    - Choisir le type d'import (ici, *Ressources diverses*)
    - Cocher la case *Correspondance automatique à partir des étiquettes simples* pour activer le mapping automatique des noms de colonnes avec les propriétés Dublin Core

- Étape 2 : Paramétrage du mapping
    - Indiquer le nom de la colonne contenant les informations sur les types de ressources ;
    - Pour chaque colonne du fichier, Omeka propose un mapping avec une propriété. Vous pouvez modifier le choix d'Omeka en cliquant sur le **+**. Un panneau coulissant s'affiche alors à droite de l'écran avec la liste de toutes les propriétés disponibles. C'est aussi dans ce panneau que vous pourrez configurer l'association des médias avec les contenus correspondants :
        - *Données spécifiques au contenu* indique la propriété contenant l'identifiant du contenu (dcterms:identifier, dcterms:title, etc.) ;
        - *Source du média* indique le type de média à importer (IIIF, URL, etc.)
    - Chaque champ de métadonnées est personnalisable. La clé à molette fait apparaître un nouveau panneau coulissant, à droite de l'écran. Vous pouvez appliquer un type de données spécifique (text, uri) ou indiquer qu'une cellule contient plusieurs valeurs en cochant la case *Utiliser un séparateur multivalué*.
        - Pour générer automatiquement des URI avec un label, dans votre fichier CSV, vous devez séparer l'URI et le label d'un espace ;
        - Pour créer plusieurs valeurs à partir d'une même cellule, ces valeurs doivent être séparer par une virgule.
    - L'onglet *Paramètres de base* offre des options de paramètrage supplémentaires. Vous pouvez appliquer à tous les contenus importés un modèle de ressource et une classe, décider si ces contenus seront publics ou privés, ou encore indiquer l'utilisateur propriétaire des données, la collection à laquelle elles appartiennent et le site où elles seront affichées.
    - Après avoir choisi les paramètres, cliquez sur "Importer" (en haut, à droite).