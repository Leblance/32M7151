# Introduction à Omeka S

## 1. Présentation générale
(Origine, développeurs, différences entre les trois outils, modules, ressources utiles)

## 2. Showcase : Ce qu'Omeka S permet de faire
- [Humazur](https://humazur.univ-cotedazur.fr/s/humazur/page/accueil) : Bibliothèque numérique de l'Université de Côte d'Azur avec gestion de grandes collections et géolocalisation
- [Genovefa](https://genovefa.bsg.univ-paris3.fr/s/genovefa/page/accueil) : Bibliothèque numérique de la bibliothèque Sainte-Geneviève (collections numérisées, expositions, éditions numériques)
- [Correspondance d'Henri Poincaré](https://henripoincare.fr/s/correspondance/page/accueil) : Édition de lettres, index, données liées
- [Ghent Mapped](https://kaart.gentgemapt.be/) : Représentation de la ville de Ghent avec une carte interactive montrant son évolution à travers le temps
- [French theater Calendar 1799-1804](https://reve.warwick.ac.uk/s/revev1_3/page/home) : Index et données liées

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
1. En haut, à droite, cliquer sur l'icône ![https://img.icons8.com/?size=20&id=84871&format=png&color=000000](https://img.icons8.com/?size=20&id=84871&format=png&color=525252) afin de passer votre site en privé. Vous pourrez le rendre public plus tard.
1. Enfin, cliquer sur le bouton "Ajouter".

### 3.3. Administrer son site
Une fois votre site créé, de nouveaux onglets apparaissent dans le panneau de gauche. Ils sont spécifiques à votre site. Si vous cliquez sur l'icône ![https://img.icons8.com/?size=100&id=83168&format=png&color=525252](https://img.icons8.com/?size=20&id=83168&format=png&color=525252), à côté du nom de votre site, vous accèdez à l'interface publique (*front end*), celle que verront vos utilisateurs finaux.
Dans "sites admin", vous pouvez modifier les informations données lors de la création du site. L'onglet "Settings" offre des paramètres plus avancés :

- Décocher la case "Auto-assign new items". Si cette case est active, tous les nouveaux contenus qui seront importés dans la base de données seront automatiquement associés à votre site, peu importe les utilisateurs qui les ajoutent.
- Décocher la case "Show page navigation". Lorsqu'elle est activée, cette option permet d'afficher des boutons "Previous" et "Next" en bas de chaque page de votre site.
- Dans la section "Langue", vous pouvez définir la langue de votre site.

Pour l'instant, votre site est une coquille vide, avec seulement une page d'accueil. La prochaine étape est donc d'ajouter des contenus !


