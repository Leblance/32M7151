# L'affichage des collections

Omeka S propose plusieurs manières de parcourir les contenus sur l'interface publique de votre site :

- Navigation par contenus (*Browse items*) : solution proposée par défaut par Omeka S ;
- Navigation par collections (*Browse collections*) ;
- Navigation par facettes (*Faceted browse*) : mise en place de filtres pour permettre à l'utilisateur de cibler ses recherches.

## 1. La navigation par contenus et collections

La mise en place de la navigation par contenus ou par collections se fait à partir de l'onglet "Navigation" (Panneau de gauche du tableau de bord). C'est ici que vous pouvez gérer et organiser les onglets de votre menu de navigation. Pour l'instant, ce menu n'est composé que d'un onglet "Parcourir" (sous-entendu "les contenus"). Plusieurs types de page vous sont proposés à droite du tableau de bord. Parmi ceux-ci, vous trouverez une option de navigation par collections. Si vous cliquez dessus, un nouvel onglet s'ajoute automatiquement à la liste. Vous pouvez le personnaliser en changeant son nom. Pour changer l'ordre des onglets, faites un "glisser/déposer" en appuyant sur les trois barres horizontales, à gauche du nom de l'onglet.

L'affichage des contenus, lorsque l'utilisateur clique sur l'onglet "Parcourir" de l'interace publique, est paramétrable depuis l'espace "Paramétrage du site" > "Paramètres" > Section "Parcourir" :

- "Résultats par page" : Nombre de contenus que le site affiche par page ;
- "Configuration par défaut de la liste des contenus" : Options de tri par défaut ;
- "Propriété définissant le titre" : Métadonnée utilisée comme titre des contenus dans la liste (apparaîtra sous la forme d'un lien cliquable) ;
- "Propriété définissant le corps" : Métadonnée utilisée pour afficher des informations supplémentaires sur le contenu (apparaître en-dessous du lien cliquable).

Par défaut, Omeka S ne propose pas d'options de recherche par facettes dans les contenus. Il faut pour cela ajouter le module [Faceted Browse](https://omeka.org/s/docs/user-manual/modules/facetedbrowse/).

## 2. La recherche à facettes

Le paramétrage des facettes se fait depuis l'onglet "Navigation par facettes" (panneau de gauche du tableau de bord) :

1. Cliquer sur "Ajouter une nouvelle page" ;
1. Donner un titre à cette page (par exemple "Facettes générales"), puis cliquer sur "Enregistrer et..." > "Rester sur cette page" ;
1. Cliquer sur "Add category" ;
1. Dans la liste déroulante de la catégorie "Facettes", sélectionner "Valeur" et valider en cliquant sur le bouton "Ajouter"
1. Un panneau apparaît à droite :
 
    - Nom de la facette
    - Propriété DC ciblée par la facette
    - *Select type* :
      
        - *Single (list)* : L'utilisateur ne peut sélectionner qu'une facette (boutons radio)
        - *Multiple (list)* : L'utilisateur peut sélectionner plusieurs facettes (cases à cocher)
        - *Single (dropdown menu)* : L'utilisateur ne peut sélectionner qu'une facette dans une liste déroulante
        - *Text input* : L'utilisateur écrit sa requête dans un champ de texte simple
  
    - Type de requête : Forme de la requête (contient, est exactement, etc.)
    - *Truncate value* : Nombre de valeurs à afficher par défaut. Si le nombre de valeurs dépasse la valeur définie, les valeurs seront cachées. L'utilisateur pourra les consulter en cliquant sur un lien "Voir plus".
    - Valeurs : Liste des valeurs (manuelle ou automatique en cliquand sur Show all available values"
    - Cliquer sur *Set facet* pour valider vos paramètres

1. Sur l'interface publique, par défaut, Omeka S affiche la vignette et le titre des contenus. Cet affichage peut être personnalisé depuis cette page dans la catégorie "Colonnes" :
  
    - Sélectionner *Title (link to ressources)* dans la liste déroulante ;
    - Ajouter deux autres colonnes en fonction d'une valeur. Un panneau coulissant apparaîtra à droite vous permettant de sélectionner les métadonnées à afficher dans la colonne, sur la base des propriétés DC. 

1. Enregistrer vos modifications.

Vous pouvez maintenant ajouter cette nouvelle page à votre menu de navigation. Depuis la page "Navigation" de votre site, cliquer sur "Navigation par facettes" dans le panneau de droite. Après lui avoir donné un nom ("Libellé"), sélectionné la page correspondante (par exemple "Facettes générales") et sauvegardé vos changements, cette nouvelle page apparaîtra dans le menu de navigation de l'interface publique.

## Création de sous-ensemble

Le module *Faceted Browse* peut être utilisé pour créer des sous-ensembles de contenus sur la base de métadonnées communes :

1. Dans l'onglet "Navigation par facettes" (panneau de gauche), ajouter une nouvelle page et une nouvelle catégorie sur le même modèle que précédemment.
1. Dans le champ "Requête à rechercher", cliquer sur "Modifier".
1. Dans le panneau coulissant de droite, vous pouvez définir une requête. Par exemple, vous pouvez créer un sous-ensemble avec uniquement des contenus dont le sujet contient le mot-clé "animaux".
1. Le bouton "Aperçu", en bas du panneau, vous permet de vérifier que votre requête est correcte.
1. Une fois que vous êtes satisfait-e, cliquer sur "Appliquer".
1. Sur le même modèle que précédemment, vous pouvez ajouter des facettes et des colonnes.

Cette page peut également être ajoutée dans le menu de navigation.
