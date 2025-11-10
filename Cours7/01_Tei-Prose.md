# Text Encoding Initiative : Kit de survie

## 1. Définition

La TEI (Text Encoding Initiative) est un langage XML pensé pour la représentation numérique de textes littéraires et historiques.
Elle est maintenu par un consortium, qui produit des guidelines et des outils :

- [Site Web du consortium TEI](https://tei-c.org/)
- Les [guidelines](https://tei-c.org/release/doc/tei-p5-doc/en/html/index.html)
    
La TEI définit plus de 600 éléments, regroupés en 23 modules c'est-à-dire des spécifications qui fournissent un ensemble d’éléments pour encoder certains aspects (poésie, théâtre, manuscrit, dictionnaire, etc.).

La TEI permet de structurer et de décrire des textes pour leur analyse, leur partage et leur publication (en ligne ou non). C'est un compromis entre les besoins de l’édition traditionnelle (forme, structure) et ceux des chercheurs en humanités (contenu, sens).
Cela implique deux niveaux d'encodage :

- Un encodage logique : Représentation de la structure du texte ;
- Un encodage sémantique (noms, lemmes, lieux, dates, etc.).

La TEI est actuellement l’un des seuls standards qui permet d’encoder le sens des textes. Elle apporte un autre éclairage, qui complète les méthodes de recherche traditionnelles.
Pour structurer des textes en TEI, vous aurez besoin :

- De connaître la syntaxe XML ;
- De respecter la sémantique des éléments TEI ;
- D’un éditeur XML (le plus utilisé étant Oxygen XML Editor).

## 2. La syntaxe XML
### 2.1. Une structure arborescente
XML repose sur une structure arborescente : Une racine, plusieurs nœuds.
```
<html>
    <head>
	   <title>Ma première page</title>
    </head>
    <body>
	   <p>Un paragraphe</p>
    </body>
</html>
```

### 2.2. Les éléments
Un élément se compose de deux balises :

- Une balise ouvrante qui commence par \< et finit par \> ;
- Une balise fermante qui commence par \</ et finit par \> ;
- Un élément doit **toujours** être fermé ;
- Les noms des éléments sont toujours écrits en minuscules.

```
<p>Un paragraphe</p>
```

:warning: Certains éléments sont constitués d’une seule balise et sont appelés des éléments vides. Ils ne contiennent pas de données. Exemple : ```<lb/>```

Les balises sont toujours imbriquées les unes dans les autres. Elles ne se chevauchent **jamais** !

```
<p><hi>Je suis une phrase mal encodée</p></hi>

<p><hi>Je suis une phrase bien encodée</hi></p>
```

### 2.3. Les attributs
Un attribut donne de l’information supplémentaire sur un élément (hauteur, largeur, langue…) :

- Les attributs fonctionnent toujours par paire : nom="valeur" ;
- Les attributs s’insèrent uniquement dans les balises ouvrantes ;
- Un élément peut avoir 0 à *n* attributs.

## 3. La structure d'un fichier TEI
```
<TEI xmlns="http://www.tei-c.org/ns/1.0">
    <teiHeader>…</teiHeader>
    <text>
	   <front>…</front>
	   <body>
	       <div>…</div>
	   </body>
	   <back>…</back>
    </text>
</TEI>
```

- L'élément racine est ```<TEI>```.
- Cet élément a deux principaux enfants :
  
    - ```<teiHeader>``` : Métadonnées bibliographiques, administratives et techniques de votre encodage ;
    - ```<text>``` : Le texte encodé.
      
- L'élément ```<text>``` a un enfant obligatoire ```<body>``` qui contient le corps du texte. Si le document sur lequel vous travaillez a une page de titre, une préface ou une dédicace, elles doivent être encodées avec l'élément ```<front>```. Les éléments annexes, telles que des tables ou des index, sont encodées avec ```<back>```.

La TEI considère qu’un texte se compose de plusieurs unités, appelées divisions : livres, parties, chapitres, tomes, poèmes, pièces, actes, etc. Ces divisions structurent le texte en plusieurs unités logiques avec ```<div>```. Vous pouvez enrichir cet élément avec plusieurs attributs, tels que :

- ```@n``` : Numéro d'une division ;
- ```@type``` : Type de la division

Le titre d’une division est encodé avec ```<head>```.

```
<div type="tragedie">
    <head>BERENICE</head>
    <div type="acte" n="1">
        <head>Acte I</head>
            <div type="scene" n="1">
                <head>Scène 1</head>
                <p>Texte de la scène 1</p>
            </div>
            <div type="scene" n="2">
                <head>Scène 2</head>
                <p>Texte de la scene 2</p>
            </div>
            …
    </div>
    <div type="acte" n="2">
        <head>Acte II</head>
        …
    </div>
    …
</div>
```

----------

Exercie 1 :

- Dans Oxygen, créer un nouveau fichier TEI ;
- Enregistrer le nouveau fichier sous miserables.xml ;
- À partir de miserables.txt, encoder la structure du texte à l’aide des éléments ```<div>``` et ```<head>```.
- Enfin, ajouter les attributs ```@n``` et ```@type```.

## 4. Encoder des textes en prose

- La structure du page :
    - ```<pb/>``` (*Page Beginning*) : indique le début d’une page ;
        - ```@n``` = Numéro de la page.
    - ```<fw>``` (*Form Work*) : indique les titres courants, les numéros de page, etc.
        - ```@type``` = pageNum, header, sig, catch.   
- Les blocs de texte :
    - ```<p>``` : indique les paragraphes ;
    - ```<lb/>``` (*Line Beginning*) : indique le début d’une ligne.
- Les italiques :
    - ```<hi>``` (*Highlight*) : Élément générique, qui vous permet d’encoder n’importe quel élément différent du reste du texte (italique, gras, majuscules, petites capitales, etc.).
        - ```@rend``` : italic, bold, uppercase, lowercase, etc.
    - ```<emph>``` (Emphasized) : Passage mis en évidence pour des raisons linguistiques ou rhétoriques. Ex. : C’est <emph>le</emph> livre de l’année !
    - ```<foreign>``` : Passage dans une autre langue.
        - ```@xml:lang``` : Pour indiquer la langue utilisée. 
    - ```<title>``` : Titre d’une œuvre.
    - ```<mentioned>``` : Mot autonyme. Ex. : ```<mentioned>Toujours</mentioned>``` prend toujours un « s ».

## 5. Les textes versifiés
 
 - Pour encoder des vers : ```<l>```
 - Pour encoder des strophes : ```<lg>```
    - ```@type``` : Type de poème, de strophe, etc.

```
<div type="sonnet">
    <head rend="center">
        <lb/>XVII
        <lb/›LA BEAUTE
    </head>

    <lg type="quatrain">
        <l>Je suis belle, ô mortels, comme un rêve de pierre,</l>
        <l>Et mon sein, où chacun s'est meurtri tour à tour,</l>
        <l>Est fait pour inspirer au poète un amour</l>
        <l>éternel et muet ainsi que la matière.</l>
    </lg>
    <lg type="quatrain"›
        <l>Je trône dans l'azur comme un sphinx incompris;</l>
        <l>J'unis un coeur de neige à la blancheur des cygnes;</l>
        <l>Je hais le mouvement qui déplace les lignes,</l>
        <l>Et jamais je ne pleure et jamais je ne ris.</l>
    </lg>
</div>    
```

**Pour aller plus loin :**

- L'encodage du théâtre : [https://teibyexample.org/tutorials/TBED05v00.htm](https://www.teibyexample.org/exist/tutorials/TBED05v00.htm)
- L'encodage de la poésie : [https://www.teibyexample.org/exist/tutorials/TBED04v00.htm](https://www.teibyexample.org/exist/tutorials/TBED04v00.htm)
- L'encodage de la correspondance : [https://encoding-correspondence.bbaw.de/v1/index.html](https://encoding-correspondence.bbaw.de/v1/index.html)
- L'encodage des dictionnaires : [https://dariah-eric.github.io/lexicalresources/pages/TEILex0/TEILex0.html](https://dariah-eric.github.io/lexicalresources/pages/TEILex0/TEILex0.html)





