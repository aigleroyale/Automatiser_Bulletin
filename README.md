# Automatiser_Bulletin

Projet de création et de génération automatique des bulletins en pdf.

## Objectif du projet 

Ce projet à pour but de créer des bulletins de note sous format pdf en utilisant _RMarkdown_ .
Ce projet intéressant notamment pour les professeurs et le personnel de scolarité car il va permettre d'optimiser leur temps 
en ce qui concerne la mise en oeuvre de bulletins pour un grand nombre d'étudiants (ou élèves). 
Pour générer ces bulletins, nous pouvons procéder de deux manières. 

## Partie 1

### Méthode 1 

Création de base de données excel contenant noms, prénoms et moyennes dans différentes matières des étudiants (ou élèves)
A partir de ce fichier : mise en place d'un code permettant d'avoir les moyennes des étudiants ainsi que leurs rang par ordre croissant. 

### Explication du code de la partie 1

Pour excecuter les codes, nous importons les bibliothèques, _numpy_ ; _pandas_  et tkinter (permet d'ouvrir une fenetre de dialogue pour chercher notre DataFrame).
A partir de cette dernière bibliothèque nous importons _askopenfilename_ et _Tk_ 
Une fonction "automate" est créée et va permettre de regrouper les codes permettant d'accéder au chemin d'accès et au nom de notre fichier. 
Avec " root = Tk()" on  affiche notre fenetre de dialogue, 
puis avec "liste = []" on prend l'ensemble de fichiers importés. 
Ensuite, avec la fonction input on demande à l'utilisateur de donner le nombre de matières.
Des boucles *for* sont créées afin d'importer chacune des matières
Enfin, les moyennes, le rang et le DataFrame sont affichés. 

## Partie 2

### Méthode 2

Demander directement à l'utilisateur d'entrer avec la fonction _input_ les différents éléments relatifs à sa classe. 
La différence avec la première méthode est qu'ici une base données n'est pas importée mais c'est un dictionnaire de données que l'on crée.

### Explication du code de la partie 2

Une fonction est créée pour pouvoir obtenir une base de données en demandant à l'utilisateur de donner les noms et prénoms des étudiants et 
leurs moyennes dans différentes matières. 

Pour chaque étudiant, nous obtenons leurs moyennes dans chaque matière, c'est après cela que nous formons un dictionnaire contenant ces différents éléments. 
Ce dictionnaire est par la suite transformé en DataFrame et nous procédons à partir de ça de la meme façon que pour la méthode 1, 
c'est à dire, le calcul des moyennes générales et rangs par ordre croissant. 

## Partie 3

Cette dernière partie consiste à importer les différents éléments cités ci-dessus sur le logiciel R, plus précisément sur RMarkdown 
afin de générer des bulletins de notes sous format pdf. 

### Explication du code de la partie 3

Avec RMarkdown, nous donnons l'apperçu d'un exemplaire de bulletin de notes. 
En utilisant le package _KableExtra_ nous avons la possibilité d'avoir la base de données utilisée sous forme de tableau. 
Avec le packages _readxl_ nous pouvons importer un fichier excel. 

On génére un bulletin a partir d'un dataframe en donnant les noms des matières, les moyennes et les rangs. 

#### Pour générer un exemplaire de bulletin de notes (pour un étudiant)

On crée le DataFrame contenant le nom et le prénom de l'étudiant et les différentes matières étudiées.
Pour générer le fichier pdf on crée une boucle _for_ et en utilisant les codes : 
- _kable_styling_ pour avoir une apparence automatique avec des lignes
- _add_header_above_ pour avoir des en têtes 
A partir d'un _Knit_ nous obtenons notre bulletin de note. 

#### Pour générer plusieurs exemplaires de bulletins de notes (pour plusieurs étudiants)

Nous procédons de la meme manière que pour l'exemplaire unique, à la différence près.
C'est-à-dire qu'il suffit d'ajouter les noms et prénoms des étudiants et suivre le meme raisonnement. 

## Limites et amélioration possible du projet 

Le principal problème au niveau de notre projet est qu'il n'est pas possible de générer plusieurs exemplaires de bulletins à la fois (à cause du fichier excel utilisé).
Il faut noter qu'il est possible d'améliorer l'apparence de ces bulletins de notes en y intégrant les noms des professeurs pour chaque matière, les coefficients pour chaque UE, etc.







 
