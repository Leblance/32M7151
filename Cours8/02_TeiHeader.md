# Le TEI Header

Le ```<teiHeader>``` se compose de 4 principales catégories :
 
- ```<fileDesc>``` : Description du fichier XML-TEI (Balises minimales obligatoires) ;
- ```<encodingDesc>``` : Description du projet et des choix éditoriaux (corrections, particularités de l’encodage…) ;
- ```<profileDesc>``` : Description du contexte de production, de la langue, du sujet…
- ```<revisionDesc>``` : Historique des changements et des révisions du fichier TEI.

## 1. Le File Description

- ```<titleStmt>``` : Première balise dans ```<fileDesc>``` (Obligatoire). Elle permet de décrire le fichier électronique (titre, auteur, sponsors, responsabilités, etc.)
    - ```<title>``` : Titre du fichier électronique (ex : Les Misérables, l’édition numérique) ;
    - ```<author>``` : Auteur du texte encodé (ex : Victor Hugo) ;
    - ```<respStmt>``` : Nom des personnes qui sont intervenues dans l’édition du texte :
        - ```<name>``` : Nom de la personne ;
        - ```<resp>``` : Rôle(s) (ex : transcription, encodage, révisions, etc.).
```
<titleStmt>
    <title>Les Misérables : L'édition numérique</title>
    <author>Victor Hugo</author>
    <respStmt>
        <name>Elina Leblanc</name>
        <resp>Encodage</resp>
    </respStmt>
</titlestmt>
```

- ```<publicationStmt>``` : Donne des informations sur le contexte de diffusion de l’édition (responsable de publication, licence, etc.). Obligatoire.

    - Première solution :
        - ```<p>``` : Paragraphes donnant des informations sur la publication ;

    - Deuxième solution :
        - ```<authority>``` : Institutions/organisations responsables de l’œuvre numérique ;
        - ```<adress>``` : Adresse de l’institution ;
        - ```<availability>``` : Informations sur les modalités de diffusion :
            - ```<licence>```
        - ```<when>``` : Date de publication 

```
<publicationStmt>
    <authority>Centre d'Étude et de Recherche Éditer/Interpréter (CÉRÉdI)</authority>
    <address>
        <addrLine>Centre d'Étude et de Recherche Éditer/Interpréter (CÉRÉdI) </addrLine> <addrLine>UFR des Lettres et Sciences Humaines</addrLine>
        <addrLine>Université de Rouen</addrLine>
        <addrLine>Rue Lavoisier</addrLine>
        <addrLine>76821 Mont-Saint-Aignan Cedex</addrLine>
    </address>
    <availability status="free">
        <licence>Distribué sous licence Creative Commons
            <ref target="https://creativecommons.org/licenses/by-nc/4.0/">CC BY-NC 4.0 Attribution-NonCommercial 4.0 International</ref>/licence>
    </availability>
    <date when="2023-11-10">10-11-2023</date>
</publicationStmt>
```

- ```<sourceDesc>``` : Description de la source physique. Obligatoire.
    - Première solution :
        - ```<p>``` : Description de la source d’origine sous la forme de paragraphe ;

    - Deuxième solution :
        - <bibl> : Structuration légère.
            - Première option : Pas d’encodage explicite (comme avec ```<p>```).
            Exemple : ```<bibl>Les Fleurs du Mal de Charles Beaudelaire. Paris : Poulet-Malassis et de Broise, 1861</bibl>```            

            - Deuxième option : Encodage explicite de chaque information :

                ```
                <bibl>
                    <title>Les Fleurs du Mal</title> de <author>Charles Beaudelaire</author>.
                    <pubPlace>Paris</pubPlace> : <publisher>Poulet-Malassis et de Broise</publisher>, <date>1861</date>                    
                </bibl>
                ```
  
    - Troisième solution :
        - ```<biblFull>``` : Structuration avancée.
            - ```<titleStmt>``` : Titre et auteur(s) de la source physique.
                - ```<title>``` ;
                - ```<author>``` ;
                - ```<editor>``` (traducteur, illustrateur, éditeur, compilateur) ;
                - ```<respStmt>``` : Autres responsabilités (Imprimeur, libraire, etc.).
            - ```<editionStmt>``` : Description de l’édition.
                - ```<edition>``` : Caractéristiques principales (Nouvelle édition…).
            - ```<extent>```
            - ```<publicationStmt>``` : Information sur la publication.
                - ```<pubPlace>``` : Lieu de publication ;
                - ```<publisher>``` : Imprimeur ;
                - ```<date>``` : Date de publication ;
                - ```<idno>``` : Identifiant (cote).
            - ```<notesStmt>``` : Informations complémentaires sur la source.
                - ```<note>```.
    
    ```
    <sourceDesc>
        <biblFull>
            <titleStmt>
                <title>Bérénice, tragédie par Mr Racine</title>
                <author>Jean Racine</author>
            </titleStmt>
            <extent>64 pages</extent>
            <publicationStmt>
                <publisher>J. Ribou</publisher>
                <pubPlace>Paris</pubPlace>
                <date>1676</date>
            </publicationStmt>
            <notesStmt>
                <note>Conservé à la BnF (département Arts du spectacle, RESERVE 8-RF-4649) </note> ‹note>Numérisation disponible sur
                    <ref target="https://gallica.bnf.fr/ark:/12148/bpt6k1280636j">Gallica</ref>
                </note>
            </notesStmt>
        </biblFull>
    </sourceDesc>
    ```

## 2. L'Encoding Description
```<encodingDesc>``` : Vient juste après ```<fileDesc>```. Il communique des informations sur le projet et sur le travail d’édition :

- 1re solution :
    - ```<p>``` : Description sous forme de texte libre.
- 2e solution :
    - ```<projectDesc>``` : Description du projet avec ```<p>``` ;
    - ```<editorialDecl>``` : Principes et méthodes d’édition ;
        - ```<correction>``` : Le texte a-t-il été corrigé ? Comment ?
        - ```<normalization>``` : Le texte a-t-il été normalisé ? Comment ?
        - ```<punctuation>``` : La ponctuation d’origine a-t-elle été conservée ?
        - ```<hyphenation>``` : Comment les césures ont-elles été traitées ?

```
<encodingDesc>
    <projectDesc>
        <p>Cet encodage a été réalisé dans le cadre du cours d'Encodage et traitement des données
            (M1 Humanités Numériques, Université de Rouen, promotion 2023-2024)
        </p>
    </projectDesc>
    <editorialDecl>
        <normalization>
            <p>La graphie d'origine a été respectée.</p>
        </normalization>
        <punctuation>
            <p>La ponctuation d'origine a été conservée.</p>
        </punctuation>
    </editorialDecl>
</encodingDesc>    
```

## 3. Le Profile Description
```<profileDesc>``` : Information sur le fichier numérique (langue, mots-clés par ex.).

    - ```<langUsage>``` : Langue(s) utilisée(s) dans le texte ;
        - ```<language>``` + ```@ident```
            - Ex : fr pour le français ; es pour l’espagnol ; ja pour le japonais ; de pour l’allemand ; etc.
            - NB : C’est un élément répétable.

    - ```<textClass>``` : Description du texte avec des mots-clés issus d’un vocabulaire contrôlé ;
        - ```<keywords>```
            - ```<term>```

```
<profileDesc>
    <langUsage>
        <language ident="fr">Français</language>
    </langUsage>
    <textClass>
        <keywords xml:base="https://catalogue.bnf.fr/ark:/">
            <term corresp="12148/cb11939701x">Théâtre (genre littéraire)</term>
            <term corresp="12148/cb11968717p">Tragédie</term>
            <term corresp="12148/cb120419182">Dix-septième siècle</term>
            <term corresp="12148/cb119328036">Rome</term>
        </keywords>
    </textClass>
</profileDesc>
```

## 4. Le Revision Description
```<revisionDesc>``` : Dernier élément du ```<teiHeader>```. Permet de garder une trace de toutes les modifications apportées au fichier TEI :

    - ```<change>``` : Indique toutes interventions ou tous changements apportés au document.
        - ```@when``` : Date du changement ;
        - ```@who``` : Identifiant de l’auteur du changement. Il pointe vers un identifiant défini dans la partie ```<titleStmt>```, avec un ```@xml:id``` associé à ```<respStmt>```.

```
<revisionDesc>
    <change when="2024-02-01" who="#EL">Création du fichier TEI et encodage du corps du texte</change>
    <change when="2024-02-08" who="#EL">Encodage du TEI Header</change>
</revisionDesc>
```
