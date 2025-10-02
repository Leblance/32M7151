# Introduction à Omeka S

## 1. Présentation générale
Omeka a été développé par le Roy Rosenzweig for History and New Media (RRHNM, George Fairfax University, Virginie) en 2008. Il a été spécifiquement conçu pour la diffusion de larges collections d'objets patrimoniaux (manuscrits, lettres, photographies, inscriptions, etc.). Son organisation reprend celles des fonds d'archives, avec des contenus structurés en collections et sous-collections.
Omeka est très utilisé par les institutions patrimoniales et de recherche, en raison de sa facilité d'utilisation et de sa mise en place. Il peut également être enrichi et personnalisé à l'aide de nombreux modules et thèmes, développés par la communauté des utilisateurs.

Trois versions sont disponibles :

- [Omeka Classic](https://omeka.org/classic/) : Version à installer sur serveur (Une instance = un site) ;
- [Omeka.net](https://www.omeka.net/) : Version en ligne pour une publication immédiate (nombre limité de modules, de thèmes et d'espace de stockage) ; 
- [Omeka S](https://omeka.org/s/): Version à installer sur serveur. Refonte d'Omeka classic : tourné vers le multisite et les données liées.

Omeka S, et la suite Omeka d'une manière générale, bénéficie d'une communauté très active, qui produit de nombreuses documentations et ressources pour découvrir et utiliser Omeka :

- [Manuel d'utilisation](https://omeka.org/s/docs/user-manual)
- [Liste des modules](https://omeka.org/s/modules/)
- [Liste des thèmes](https://omeka.org/s/themes/)
- [AUFO](https://omeka.fr/fr) (Association des Usages Francophones d'Omeka)

## 2. Showcase : Ce qu'Omeka S permet de faire
- [Fabrique de l'art](https://fva-fmv.inha.fr/s/fva/page/accueil) : Bibliothèque numérique thématique (programme de recherche de la BnF, 2021-2023)
- [Genovefa](https://genovefa.bsg.univ-paris3.fr/s/genovefa/page/accueil) : Bibliothèque numérique de la bibliothèque Sainte-Geneviève (collections numérisées, expositions, éditions numériques)
- [Digital Muret](https://digitalmuret.inha.fr/s/accueil-muret/page/accueil) : Indexation et liaison des données (programme de recherche de la BnF, 2017-2021)
- [Correspondance d'Henri Poincaré](https://henripoincare.fr/s/correspondance/page/accueil) : Édition de lettres, index, données liées
- [Ghent Mapped](https://kaart.gentgemapt.be/) : Représentation de la ville de Ghent avec une carte interactive montrant son évolution à travers le temps
- [French theater Calendar 1799-1804](https://reve.warwick.ac.uk/s/revev1_3/page/home) : Index et données liées

NB : Le site de l'AUFO propose une [liste de projets francophones](https://omeka.fr/fr/csv/annuaire-sites/) utilisant Omeka S et Omeka classic. Un [répertoire similaire](https://omeka.org/s/directory/) est également disponible sur le site d'Omeka S.

## 3. Création d'un site web
### 3.1. Le dashboard
Pour se connecter à l'instance d'Omeka S de l'Université de Genève (avec son mail universitaire) : [https://dh.unige.ch/omeka/login](https://dh.unige.ch/omeka/login).

Une fois connecté, le dashboard d'Omeka S apparaît. Il s'agit du *back-end*, uniquement visible par les personnes ayant un compte.

- Au centre, Omeka vous donne un aperçu du nombre de ressources disponibles dans la base de données, ainsi que la liste des sites déjà existants.
- À gauche, un panneau d'administration vous permet de gérer les sites, les ressources, les modules installés et l'administration générale du CMS. L'onglet "Admin" apparaît uniquement pour les utilisateurs qui ont des droits d'administrateurs.

**Point sur les rôles utilisateurs**
Omeka permet d'assigner des rôles différents aux utilisateurs. Ils définissent et limitent les actions qu'une personne peut faire. Par exemple, le *global administrator* a tous les privilèges. Le *supervisor* peut créer/supprimer tous les contenus et tous les sites, alors que le *reviewer* peut uniquement supprimer les contenus qu'il a créé. Vous trouverez la liste de tous les rôles et privilèges dans le manuel d'utilisation : [https://omeka.org/s/docs/user-manual/admin/users/#roles-and-permissions](https://omeka.org/s/docs/user-manual/admin/users/#roles-and-permissions).
Pour cette formation, vous aurez le rôle de superviseurs (*supervisor*). Vous avez tous les privilèges sur les ressources et les sites, c'est-à-dire que vous pouvez créer/éditer/supprimer vos contenus/sites... et ceux des autres. :warning: Soyez vigileants !


### 3.2. Créer son site

1. Cliquer sur l'onglet "Sites" dans le panneau de gauche, puis sur le bouton "Ajouter un nouveau site", en haut à droite.
1. Remplisser le formulaire :
   - Titre : Le titre de votre site
   - Identifiant pour l'URL (ou *slug*) :  Partie finale de l'URL
   - Description : Courte présentation du site 
   - Vignette : Image ou logo de votre projet
1. Au-dessus du formulaire, cliquer sur l'onglet "Thème" et choisissez un thème dans la liste.
    - L'instance de l'Université de Genève vous propose 4 thèmes. Vous pouvez demander l'installation d'un nouveau thème en vous référant à cette [liste](https://omeka.org/s/themes/). 
1. En haut, à droite, cliquer sur l'icône ![https://img.icons8.com/?size=20&id=84871&format=png&color=000000](https://img.icons8.com/?size=20&id=84871&format=png&color=525252) afin de passer votre site en privé. Vous pourrez le rendre public plus tard.
1. Enfin, cliquer sur le bouton "Ajouter".

### 3.3. Administrer son site
Une fois votre site créé, de nouveaux onglets apparaissent dans le panneau de gauche. Ils sont spécifiques à votre site. Si vous cliquez sur l'icône ![https://img.icons8.com/?size=100&id=83168&format=png&color=525252](https://img.icons8.com/?size=20&id=83168&format=png&color=525252), à côté du nom de votre site, vous accèdez à l'interface publique (*front end*), celle que verront vos utilisateurs finaux.
Dans "sites admin", vous pouvez modifier les informations données lors de la création du site. L'onglet "Settings" offre des paramètres plus avancés :

- Décocher la case "Auto-assign new items". Si cette case est active, tous les nouveaux contenus qui seront importés dans la base de données seront automatiquement associés à votre site, peu importe les utilisateurs qui les ajoutent.
- Décocher la case "Show page navigation". Lorsqu'elle est activée, cette option permet d'afficher des boutons "Previous" et "Next" en bas de chaque page de votre site.
- Dans la section "Langue", vous pouvez définir la langue de votre site.

Pour l'instant, votre site est une coquille vide, avec seulement une page d'accueil. La prochaine étape est donc d'ajouter des contenus !


