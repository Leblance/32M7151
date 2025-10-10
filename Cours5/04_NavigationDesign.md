# Création de pages et navigation

## 1. Créer de nouvelles pages

Depuis l'espace de gestion de votre site, à gauche du tableau de bord, l'onglet "Pages" vous permet de voir la liste des pages de votre site, de les modifier et d'en ajouter de nouvelles :

1. Cliquer sur la page "Welcome".
1. Omeka S propose différents blocs prédéfinis pour enrichir la page. Quelques exemples :
    - HTML : Blocs de texte (éditeur WYSIWYG ou code HTML) ;
    - Aperçu des ressources : Liste de contenus choisis au hasard, présentés avec une vignette. Ce type de bloc insère également un lien vers la page de vos contenus ;
    - Média : Ajout d'images et de contenus issus de vos collections ;
    - Liste des pages ;
    - Saut de ligne ;
    - Etc.
1. Pour ajouter un nouveau bloc, il suffit de cliquer sur eux dans la liste. Ils peuvent être réorganisés par "glisser-déposer".
1. Chaque bloc est personnalisable, en cliquant sur les roues dentées (à côté de l'icône poubelle) :
    - Classe : Nom d'une classe pour l'utiliser dans une feuille de style ;
    - Alignement : Bloc et texte (gauche, droite, centrer) ;
    - Constraints : Imposer une hauteur et/ou une largeur à un bloc ;
    - Padding : Définir des marges intérieures pour votre bloc ;
    - Background : Définir une couleur ou une image de fond.
    
## 2. Gérer la navigation

L'onglet "Navigation", situé dans l'espace de gestion de votre site, vous permet de définir les onglets qui apparaîtront dans le menu de navigation de votre site, ainsi que leur ordre. Le panneau de droite liste l'ensemble des pages disponibles. Pour en ajouter une au menu, cliquer sur son nom dans la liste. Une fois une page ajoutée, Omeka vous propose de lui attribuer un libellé, c'est-à-dire de définir le nom de l'onglet dans le menu. L'ordre des onglets peut être changé par "glisser-déposer".

## 3. L'apparence du site et des pages
### 3.1. Les paramètres généraux du thème
Depuis l'onglet "Thème" (à gauche du tableau de bord, dans l'espace de votre site), vous avez la possibilité de facilement changer de thème. Chaque thème s'accompagne également de paramètres qui lui sont propres et que vous pouvez modifier en cliquant sur le bouton "Modifier les paramètres du thème". Vous pourrez ainsi choisir un logo ou une banière ou encore personnaliser le pied de page du site.

### 3.2. La personnalisation du site
Si vous souhaitez aller plus loin dans la personnalisation de votre site, Omeka S a développé le module [CSS Editor](https://omeka.org/s/docs/user-manual/modules/csseditor/), accessible dans l'espace de gestion de votre site.
Dans le champ de texte, vous pouvez écrire des règles CSS qui réécriront les règles de style par défaut.

**Point CSS**
Les règles CSS s'écrivent de la manière suivante : ```Sélecteur {propriété: valeur;}```
Exemples :
```
h1 { color: green ;
     font-size: 30pt ; }

p { font-family: Arial, Helvetica, sans-serif ; }

```

Quelques propriétés CSS :

- La police d’écriture : font-family (suivi de trois polices d'écriture) ;
- La taille du texte : font-size (pt, px, em, rem, etc.)
- L’alignement du texte : text-align (left | right | center | justify)
- L’italique : font-style (italic | oblique | normal)
- Les caractères gras : font-weight (bold | normal)
- Les couleurs : color ([Liste de couleurs](https://www.w3schools.com/cssref/css_colors.php))
    - Mots-clés : white, black, maroon, red, blue, orange, yellow, purple, olive, fushia…
    - Valeur hexadécimale : #0000FF (= blue)
    - Coordonnées RVB : rgb(255, 0, 0) 
