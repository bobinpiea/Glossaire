# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général

1.	Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte

        Pour exécuter un script PHP, il faut un serveur web Apache qui gère PHP. 
         
        Laragon, WAMP -> Windows, 
        MAMP -> MacOS, et 
        LAMP -> Linux. 
        Ces packs facilitent l’installation de tout l’environnement nécessaire.

        Mots-clés :
            •	Serveur web Apache → gère PHP
            •	Laragon, WAMP, MAMP, LAMP → packs serveur + PHP

2.	Qu’est-ce qu’un algorithme ?  

   Un algorithme, c’est une suite finie d’instructions qu’on suit étape par étape, dans un ordre logique. 
   Il sert à résoudre un problème ou à obtenir un résultat. 
   Il peut y avoir des boucles ou des conditions, mais il doit toujours s’arrêter.
        Exemple :
        Recette de cuisine
        1- Ingrédients
        2- Ustensiles
        3- Mélange
        4- Préparation

            Mots-clés :
                Instruction
                Étape
                Problème / Résultat

3.	Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?

        Une variable, c’est un nom qu’on donne à une donnée pour la stocker en mémoire et pouvoir la réutiliser ou la modifier plus tard.
        Elle peut contenir du texte, un nombre, une date, un tableau, etc.
        En PHP, toutes les variables commencent par le symbole $.
            
            MOTS CLÉS : nom – donnée – mémoire – réutiliser / modifier 

4.	Qu’est-ce que la portée d’une variable ?

    La portée d’une variable, c’est la zone du code où elle est définie et où on peut l’utiliser.
        •	Si elle est déclarée en dehors d’un bloc (une fonction ou autre), elle est globale, accessible partout.
        •	Si elle est déclarée dans un bloc (fonction, condition, boucle), elle est locale à ce bloc.

    Pour utiliser une variable globale dans un bloc local, il faut la déclarer avec le mot-clé global.
    
    Mots-clés :
        •	Portée
        •	Globale
        •	Locale
        •	Bloc


5.	Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?

        Une constante, c’est un nom qu’on donne à une donnée dont la valeur ne change jamais pendant toute la durée du script.
        Contrairement à une variable, la constante a une valeur fixe, on ne peut pas la modifier.
        On ne met pas de  $  devant une constante comme pour les variables.
        Pour créer une constante en PHP, on utilise soit la fonction  define() , soit le mot-clé  const .

        Mots-clés :
            •	Constante
            •	Valeur fixe
            •	Pas de  $ 
            •	define() 
            •	const 

6.	Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation 

        Une superglobale, c’est une variable PHP toute prête à l’emploi, accessible n’importe où dans le code, même dans les fonctions ou classes, sans qu’on ait besoin de la déclarer.
        C’est un tableau associatif qui contient des informations importantes ou utiles selon la situation.

    Par exemple :
        •	$_GET récupère les infos passées dans l’URL, comme un identifiant qui suit dans la barre d’adresse.
        •	$_POST contient les données envoyées via un formulaire, souvent pour envoyer des infos au serveur.
        •	$_SERVER donne plein de détails sur le serveur et la requête en cours, comme l’adresse IP ou les chemins des fichiers.
        •	$_SESSION stocke des données persistantes, qui restent accessibles même quand on change de page.
        •	$_COOKIE contient les petits fichiers stockés dans le navigateur, pour garder des préférences ou des infos d’identité.
        •	$_FILES permet de gérer les fichiers qu’on envoie via un formulaire, comme les photos qu’on charge.

    Mots-clés :
    •	Superglobale → variable déjà dispo
    •	Accessible partout
    •	Tableau associatif
    •	Exemples → $_GET, $_POST, $_SERVER, $_SESSION, $_COOKIE, $_FILES


7.	Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)

    Un type primitif, c’est le type de valeur que peut contenir une variable.
        Exemple : 
        string → une chaîne de caractères (du texte)
        integer → un nombre entier
        float (ou double) → un nombre à virgule
        boolean → soit true (vrai), soit false (faux)
        array → un tableau (plusieurs valeurs dans une même variable)
        null → une variable qui ne contient rien (pas encore de valeur)

        Soit 6 ! 

        MOTS CLÉS : type – valeur – string – integer – float – boolean – array – null


8.	Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?

    Oui, en PHP, il existe plusieurs types de tableaux selon la façon dont les données sont organisées :

    Tableau simple (ou indexé) ==> Indices numériques
    → Les éléments sont rangés dans un ordre, avec des indices numériques (0, 1, 2…)
     Ex: 
     $jours = ["lundi", "mardi", "mercredi"];

    Tableau associatif ==>  Clé + Valeur
    → Chaque élément est associé à une clé personnalisée (au lieu d’un chiffre).
        $utilisateur = ["
            nom" => "Pierre", 
            "age" => 30
            ];

    Tableau multidimensionnel (ou imbriqué)
    → C’est un tableau dans un tableau, utile pour organiser des données complexes.
        $produits = [
            ["nom" => "Livre", "prix" => 10],
            ["nom" => "Stylo", "prix" => 2]
        ];

    MOTS CLÉS : tableau – simple – associatif – multidimensionnel – clé – valeur – index

9.	Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles

        Une structure de contrôle, c’est ce qui permet à ton code de :
            •	faire un choix (if / else)
            •	répéter des actions (boucles)
            •	gérer plusieurs cas (switch)


    Une structure de contrôle, c’est un outil qui permet de contrôler le déroulement du programme :
    On peut en citer 3 

    1. La condition → “Si quelque chose est vrai, alors on fait ça…”

        Permet de prendre une décision selon un cas.

        if ($age >= 18) {
            echo "Majeur";
        } else {
            echo "Mineur";
        }

    2. La boucle (répétition) → “Tant que ce n’est pas fini, je continue…”

        Permet de répéter une action plusieurs fois.

        Exemples de boucles :
            •	while (tant que)
            •	for (pour un nombre défini de fois)
            •	foreach (pour parcourir un tableau)

        for ($i = 1; $i <= 3; $i++) {
            echo "Tour $i\n";
        }

    3. L’alternative multiple (switch) → “Si c’est le cas 1, je fais ça ; si c’est le cas 2, je fais ça…”

        Permet de gérer plusieurs cas possibles.

            $note = 15;

            switch ($note) {
                case 20:
                    echo "Excellent";
                    break;
                case 10:
                    echo "Moyen";
                    break;
                default:
                    echo "Autre";
            }

        MOTS CLÉS : condition – boucle – répétition – choix – if – for – while – switch

        for : c’est une boucle qui répète un bloc de code un nombre précis de fois. Par exemple, afficher les nombres de 1 à 5.
        while : boucle qui répète tant qu’une condition reste vraie. Par exemple, continuer à demander un nombre tant que la valeur n’est pas correcte.
        break : sert à casser une boucle avant qu’elle ne soit terminée naturellement. Par exemple, sortir d’une recherche dès qu’on trouve l’élément.

10.	Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?

    strlen()

    On utilise la fonction strlen().
    Elle te renvoie un nombre qui te dit combien de caractères il y a dans ta chaîne.

    Exemple : 
    $nom = "Pierre";
    echo strlen($nom); // Affiche 6

    MOTS CLÉS : longueur – chaîne – texte – strlen() – nombre de caractères

    la fonction mb_strlen() qui compte les caractères correctement en UTF-8.

11.	Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP

        Une session en PHP sert à garder des informations sur l’utilisateur pendant qu’il navigue de page en page sur un site,
        sans tout stocker chez lui (contrairement aux cookies, ici tout reste côté serveur).
        PHP crée un identifiant unique pour chaque visiteur, et avec la superglobale  $_SESSION , on peut mémoriser des infos comme le nom, l’email ou le panier.
        Pour démarrer une session, il faut écrire  session_start();  tout en haut du script, avant d’utilise

    Ex: session_start();
        $_SESSION['nom'] = 'Paul';  // stocker une donnée
        echo $_SESSION['nom'];       // récupérer la donnée sur une autre page

    Exemple : Quand Je me connectes sur Facebook, mes infos (nom, id...) sont stockées dans une session. 
    Comme ça je reste connecté en naviguant de page en page.
    
    MOTS CLÉS : session – session_start() – $_SESSION – stockage serveur – navigation   

12.	Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP

        Un cookie, c’est un petit fichier texte que le site web demande au navigateur de stocker sur l’ordinateur ou le téléphone de l’utilisateur.
        Ce fichier garde des infos comme ses préférences, sa langue choisie, ou un identifiant, pour que le site puisse se souvenir de lui quand il revient.
        En PHP, on crée un cookie avec la fonction  setcookie() . 

        setcookie('theme', 'sombre', time() + 86400, '/'); // cookie qui garde le thème sombre pendant 24h

    MOTS CLÉS : cookie – côté client – setcookie() – $_COOKIE – préférences – navigateur

    La différence importante avec session : session = serveur, cookie = navigateur !

13.	Quelle est la différence entre les instructions « require » et « include » en PHP

    Les deux servent à inclure un fichier PHP dans un autre (genre pour réutiliser du code), mais ils réagissent différemment en cas de problème :
    include :
    → Si le fichier n'existe pas, PHP affiche un warning (avertissement)
    → MAIS le script continue quand même !
    require :
    → Si le fichier n'existe pas, PHP affiche une erreur fatale
    → Et le script S'ARRÊTE complètement !

        Exemple concret :
        phpinclude 'menu.php';     // Si menu.php n'existe pas → warning mais la page continue
        require 'config.php';   // Si config.php n'existe pas → STOP, page blanche !
        
    Astuce pour retenir :

    require = "j'ai BESOIN de ce fichier" (required = obligatoire)
    include = "ce serait bien de l'avoir mais c'est pas grave"

    On utilise require pour les fichiers critiques (connexion BDD, config...) et include pour le moins important (footer, pub...).
    MOTS CLÉS : include – warning – continue / require – erreur fatale – stop


14.	Comment effectuer une redirection en PHP ?

    Pour rediriger vers une autre page en PHP, on utilise la fonction header() avec Location:

    Syntaxe :
    phpheader('Location: page.php');
    exit();  // Important ! Toujours mettre exit() après

    Pourquoi exit() ? Pour arrêter le script immédiatement après la redirection, sinon le code continue de s'exécuter !

    MOTS CLÉS : header() – Location – exit() – redirection – avant HTML

15.	Définir la partie « front-end » et « back-end » d’une application

    Front-end :
        → C'est ce qu'on voit et ce avec quoi on interagit sur un site
        → L'interface, le design, les menus, tout le côté visuel
        → Langages : HTML, CSS, JavaScript
        → La partie "visible" de l'application

    Back-end :
        → C'est ce qu'on ne voit pas, le cerveau de l'application
        → Tout ce qui tourne sur le serveur : calculs, stockage, sécurité
        → Langages : PHP, Python, Java, Node.js...
        → La partie "invisible" qui fait fonctionner le tout

    Exemple :
    Quand on se connecte sur un site :

    Front : Le formulaire avec les champs login/mot de passe
    Back : La vérification du mot de passe dans la base de données

    MOTS CLÉS : front = ce qu'on voit | back = ce qu'on ne voit pas (le cerveau)


16.	Définir le contrôle de version ? Qu’est-ce que Git ?

    Le contrôle de version :
        → C'est un système qui enregistre toutes les modifications de mon code au fil du temps
        → Je peux voir tout l'historique de mon projet depuis le début
        → Si je fais une erreur, je peux revenir à une version précédente qui fonctionnait

    Git :
        → C'est le logiciel de contrôle de version le plus populaire
        → Il permet de sauvegarder mon travail étape par étape
        → Je peux collaborer avec d'autres sans qu'on écrase le travail de chacun

    Exemple :
    Je développe un site web :

    Je sauvegarde ma version stable avec git commit
    J'ajoute une nouvelle fonctionnalité qui crée des bugs
    Je peux facilement revenir à ma version stable d'avant

    Comparaison :

    C'est comme les points de sauvegarde dans un jeu → je sauvegarde avant un passage difficile pour pouvoir recommencer si besoin
    Commandes essentielles :

    git add → sélectionner les fichiers à sauvegarder
    git commit → créer un point de sauvegarde
    git push → envoyer sur GitHub/GitLab

    MOTS CLÉS : contrôle de version – historique – Git – sauvegarde – collaboration – commit

    Git est un exemple de système de contrôle de version décentralisé crée en 2005 par Linus Torvalds
    (fondateur de Linux).

17.	Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

    Un CMS (Content Management System) :
        → C'est un système de gestion de contenu en français
        → C'est un logiciel qui permet de créer et gérer un site web sans coder
        → Tout se fait avec une interface visuelle : j'ajoute du texte, des images, je crée des pages...
        → Pas besoin de toucher au HTML/CSS/PHP, le CMS s'occupe de tout
    
    Exemples de CMS :
        WordPress → Le plus populaire, 40% des sites web l'utilisent
        Joomla → Plus complexe mais plus flexible
        Drupal → Pour les gros sites avec beaucoup de contenu
        Shopify → Spécialisé pour les boutiques en ligne
        Wix → Super simple, tout se fait en glisser-déposer

    Exemple :
        Au lieu de coder mon blog from scratch, j'installe WordPress :

    Je choisis un thème (le design)
    J'écris mes articles dans un éditeur (comme Word)
    WordPress génère tout le code automatiquement

    Avantage : Rapide et facile pour créer un site
    Inconvénient : Moins de liberté qu'en codant tout soi-même

    MOTS CLÉS : CMS – gestion contenu – sans coder – WordPress – Joomla – interface visuelle


## Front-end

18.	Définir HTML

    HTML (HyperText Markup Language) :
    → C'est le langage de base pour créer la structure d'une page web
    → Ce n'est pas un langage de programmation, c'est un langage de balisage
    → Il définit le squelette de la page : titres, paragraphes, liens, images, formulaires...
    → Tout se fait avec des balises qui entourent le contenu

            Analogie :
        HTML = la structure de la maison (murs, portes, fenêtres)
        CSS = la décoration (peinture, style)
        JavaScript = l'électricité (interactivité)

        MOTS CLÉS : HTML – structure – balises – squelette – page web – langage de balisage

19.	Définir CSS

        CSS (Cascading Style Sheets) :
            → C'est le langage qui gère tout l'aspect visuel et la mise en forme d'une page web
            → Il donne du style au HTML : couleurs, polices, tailles, espacements, animations...
            → CSS sépare le contenu (HTML) de la présentation (le design)
            → Une seule feuille CSS peut styliser tout un site

        MOTS CLÉS : CSS – style – design – couleurs – mise en forme – sélecteurs – présentation

20.	Définir Javascript

        JavaScript (souvent abrégé JS) :
            → C'est LE langage de programmation du web côté client (dans le navigateur)
            → Il rend les pages web interactives et dynamiques
            → Contrairement à HTML/CSS qui sont statiques, JavaScript peut réagir aux actions de l'utilisateur
            → Il peut modifier le HTML et CSS en temps réel sans recharger la page

        Analogie (suite) :

        HTML = la structure de la maison
        CSS = la décoration
        JavaScript = l'électricité et la domotique (les interrupteurs, l'alarme, les portes automatiques)

        MOTS CLÉS : JavaScript – interactivité – dynamique – client – événements – DOM – temps réel

21.	Définir JSON. Dans quel contexte ce format est-il utilisé ? 

        JSON (JavaScript Object Notation) :
        → C'est un format de données léger pour échanger des informations entre systèmes
        → C'est du texte simple, facile à lire pour les humains et les machines
        → Même si ça vient de JavaScript, tous les langages peuvent l'utiliser (PHP, Python...)
        → Structure basée sur des paires clé-valeur et des listes

    MOTS CLÉS : JSON – format données – échange – API – clé-valeur – json_encode – json_decode

22.	Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

    Oui, c'est possible avec Node.js !
    Node.js :
    → C'est un environnement qui permet d'exécuter JavaScript sur le serveur (pas dans le navigateur)
    → Avant Node.js, JavaScript ne fonctionnait que côté client
    → Maintenant on peut faire du back-end en JavaScript, comme on fait avec PHP
    → Créé en 2009, basé sur le moteur V8 de Chrome

    MOTS CLÉS : Node.js – JavaScript serveur – back-end – V8 – Express – full-stack JavaScript


23.	Qu’est-ce qu’un sélecteur CSS ?

    Un sélecteur CSS :
        C'est ce qui permet de "cibler" les éléments HTML qu'on veut styliser
        C'est la partie qui vient AVANT les accolades dans le CSS
        Ça dit au navigateur : "applique ce style à CET élément"

            Types principaux :

            Élément -> h1, p, div (tous les éléments de ce type)
            Classe -> .nomclasse (peut être utilisé plusieurs fois)
            ID -> #nomid (unique sur la page)
            Universel -> * (TOUT sélectionner)

            MOTS CLÉS : sélecteur – cibler – élément – classe (.) – id (#) – CSS

24.	Quelle balise HTML permet de créer un lien hypertexte ?

    C'est la balise <a> (anchor = ancre)

    MOTS CLÉS : <a> – href – lien hypertexte – ancre – target – HTML

25.	Qu’est-ce qu’une requête AJAX ?

    AJAX (Asynchronous JavaScript And XML) :
    → C'est une technique qui permet d'échanger avec le serveur SANS recharger la page
    → JavaScript envoie une requête en arrière-plan et récupère la réponse
    → La page se met à jour dynamiquement, sans le rechargement complet
    → Aujourd'hui on utilise plus JSON que XML, mais le nom est resté
    Avant AJAX :

    Je clique sur "Voir plus" → toute la page se recharge
    C'est lent et ça fait clignoter

    Avec AJAX :

    Je clique sur "Voir plus" → seule la partie concernée se met à jour
    C'est fluide et rapide !

    MOTS CLÉS : AJAX – sans recharger – asynchrone – JavaScript – dynamique – fetch – JSON

26.	Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?

    Pour sélectionner une classe → le point .

    → Sélectionne TOUS les éléments avec class="maClasse"
    → Peut être utilisé plusieurs fois sur la même page
    Pour sélectionner un ID → le dièse #

    → Sélectionne L'élément avec id="monId"
    → Doit être unique sur la page (un seul élément)

    MOTS CLÉS : classe → point (.) | ID → dièse (#) | sélecteur CSS

27.	Définir le responsive design - V

   Le responsive design, c'est faire en sorte qu'un site s'adapte à toutes les tailles d'écran 
   de manière agréable et harmonieuse - ordinateur, tablette, téléphone.

   Avec les media queries en CSS qui changent le style selon la taille
   
   MOTS CLÉS : responsive – s'adapter – toutes tailles d'écran – agréable – ordi/tablette/téléphone – media queries


28.	Qu’est-ce que le templating ?
29.	Qu’est-ce qu’une fonction anonyme en Javascript ?
30.	Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
31.	Qu’est-ce qu’un « media query » ?
32.	Qu’est-ce qu’un pseudo élément en CSS ?
33.	Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
34.	Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes

## UX UI
35.	Quelle est la différence entre UX Design et UI Design ?
36.	Qu’est-ce qu’un wireframe ? 
37.	Qu’est-ce qu’un prototype ? 
38.	Qu’est-ce que la hiérarchie visuelle en UI Design ?
39.	Qu’est-ce que l’accessibilité en UX Design ? 
40.	Qu’est-ce qu’une grille de mise en page ?
41.	Qu’est-ce que la notion d’affordance en UX Design ?
42.	Qu’est-ce qu’un « mobile first design » ?

## Programmation orientée objet (POO)
43.	Donner une définition de la programmation orientée objet 

    La programmation orientée objet (POO), c’est une façon d’écrire du code en voyant chaque chose comme un “objet”, un peu comme dans la vraie vie.
    Chaque objet a ses propres infos (attributs) et peut faire ses propres actions (méthodes).
    Ça permet de mieux organiser son code, surtout quand il devient gros, et/ou complexe.

    MOTS CLÉS : Objet – Attribut – Méthode – Organiser le code

44.	Qu’est-ce qu’une classe ? Comment la déclare-t-on ?

Une classe, c’est comme un plan ou un moule qu’on utilise pour fabriquer des objets.
Elle contient les informations (attributs) et les actions possibles (méthodes).
Une fois qu’on a une classe, on peut créer plein d’objets à partir d’elle, un peu comme une recette qu’on suit plusieurs fois.

Déclaration :
On déclare une classe en PHP avec le mot-clé class, suivi du nom de la classe.

Exemple : 

class MaClasse {
    //  je mets les attributs et méthodes ici
}

45.	Qu’est-ce qu’un objet ?

Un objet, c’est ce qu’on crée à partir d’une classe (l’instanciation).
C’est une chose "physique" qui peut utiliser les méthodes et les attributs de la classe dans laquelle il a été créé.
Chaque objet peut avoir ses propres valeurs, même s’il vient du même moule.

MOTS CLÉS : objet – instanciation – classe – utiliser – méthode – attribut

46.	Définir la notion de propriété / attribut / méthode

Un attribut, c’est une variable déclarée dans une classe.
Quand cette variable est accessible depuis l’extérieur (avec un getter ou un setter), on parle de propriété.

Une méthode, c’est une fonction écrite dans une classe.
Elle sert à faire une action avec les données de l’objet (comme afficher, calculer, modifier…).

MOTS-CLÉS :
    •	Attribut = variable interne à la classe
    •	Propriété = version accessible (via getter/setter)
    •	Méthode = action d’un objet ou d’une classe
    •	CLASSE = contient attributs + méthodes
    
47.	Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité

Brouillon 

La visibilité d’une méthode serait sa faculté à être visible selon certains endroits.
Privée : dans la classe uniquement.
Publique : à l’extérieur de la classe.
Protégée : en cas d’héritage.


48.	Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?

A continuer

le constructeur 

49.	Qu’est-ce que l’encapsulation ?

50.	Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple

Brouillon 
La conception clé est l’héritage, c’est-à-dire qu’on a une classe parente et qu’on veut créer une classe enfant.
Dès lors, afin que cette dernière ait ses attributs et ses fonctions, on doit alors utiliser le terme “extends” pour dire qu’elle hérite des données qu’il y a à l’intérieur.


51.	Définir l’opérateur de résolution de portée
52.	Définir une méthode / propriété statique
53.	Définir le polymorphisme en POO
54.	Définir une méthode / classe abstraite ?
55.	Définir le chaînage de méthodes
56.	Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
57.	Qu’est-ce qu’un « autoload » ?
58.	Comment appelle-t-on en français les « getters » et les « setters » ?
59.	Qu’est-ce que la sérialisation en PHP ? 

## Architecture 
60.	Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
61.	Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
62.	Qu’est-ce que l’architecture MVC ?
63.	Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
64.	Quels sont les avantages de l’architecture MVC ?
65.	Existe-t-il des variantes à l’architecture MVC ?
66.	Qu’est-ce qu’une API ? Définir l’architecture REST

## Modélisation - Base de données
67.	Qu’est-ce que la modélisation de données ? Définir la méthode Merise
68.	Quelles sont les 3 étapes principales de la méthode Merise ? 
a.	Analyse, conception et réalisation
b.	Planification, exécution et contrôle
c.	Création, modification et suppression
69.	Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
70.	Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
71.	Donner la définition des mots suivants :
a.	Entité
b.	Relation
c.	Cardinalité
d.	Clé primaire / clé étrangère
72.	Que devient une relation de type « Many To Many » dans le modèle logique de données ?
73.	Qu’est-ce qu’une base de données ?
74.	Définir les notions suivantes : 
a.	SQL
b.	MySQL
c.	SGBD (donner 2 exemples de SGBD)
75.	Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de lignes appelées ___ et de colonnes appelées ___
76.	Quelle est la différence entre une base de données relationnelle et non relationnelle ?
77.	Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
78.	A quoi sert une vue dans une base de données ?
79.	Qu’est-ce que l’intégrité référentielle dans une base de données ?
80.	Quelles sont les fonctions d’agrégation en SQL ?
81.	Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
82.	Quelles sont les clauses qui permettent de :
a.	Insérer un nouvel enregistrement dans une table
b.	Modifier un enregistrement dans une table
c.	Supprimer un enregistrement dans une table
d.	Supprimer la base de données
e.	Filtrer les résultats d’une requête SQL
f.	Trier les résultats d’une requête SELECT
g.	Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
h.	Concaténer 2 chaînes de caractères 
83.	Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

## Symfony
84.	Qu’est-ce que Symfony ?

symfony est une framework php q


85.	Sur quel langage de programmation et design pattern repose Symfony ? 

langage de programmation phph et le design pattern est le MVC



86.	Quelle est la dernière version en date de Symfony ?





87.	Qu’est-ce qu’un bundle ? 




88.	Quel est le moteur de template utilisé par défaut dans Symfony ?



89.	Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?



90.	Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?



91.	Que permet le bundle Maker au sein de Symfony ? 



92.	Quel est le langage de requêtage exploité au sein d’un projet Symfony ?



93.	Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?




## Sécurité
94.	Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
95.	Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
96.	Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
97.	Définir l’attaque par force brute et l’attaque par dictionnaire
98.	Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
99.	A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
100.	Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
101.	Qu’est-ce qu’une politique de mots de passe forts ?
102.	Qu’est-ce que l’hameçonnage ?
103.	Définir la « validation des entrées »

## RGPD
104.	Qu’est-ce que le RGPD ?
105.	Quel est son objectif principal ?
106.	Quelle est la date d’entrée en vigueur du RGPD ?
107.	Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
108.	En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
109.	Quel est le consentement valide selon le RPGD ?
110.	Qu’est-ce qu’une politique de confidentialité ?
111.	Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
112.	Quels sont les droits des utilisateurs selon le RGPD ?
113.	Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO
114.	Qu’est-ce que le SEO ? 
115.	Quel est l’objectif principal du SEO ?
116.	Existe-t-il plusieurs types de référencement ? Lesquels ?
117.	Qu’est-ce que la densité de mots-clés en SEO ?
118.	Qu’est-ce qu’une balise « alt » ?
119.	Qu’est-ce que la balise « meta description » ?
120.	Qu’est-ce que le « nofollow » en SEO ?
121.	Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
122.	Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
123.	Quelle est la recommandation pour les URL d'un site web bien référencé ?
124.	Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
125.	Qu'est-ce que l'optimisation des images pour le référencement ?
126.	Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps
127.	Qu’est-ce que la gestion de projet ?	
128.	Qu’est-ce qu’une méthode Agile de gestion de projet ? 
129.	Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
130.	A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
131.	Qu’est-ce que la planification itérative ?
132.	Citer 3 méthodes Agiles dans le cadre d’un projet informatique
133.	Qu’est-ce qu’une réunion de revue de projet ?
134.	Qu’est-ce qu’un livrable dans un projet ? 
135.	Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
136.	Qu’est-ce que le DevOps et quel est son objectif principal ?
137.	Qu’est-ce que l’intégration continue ? 
138.	Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
139.	Qu’est-ce qu’un test unitaire ? 
140.	Quelle est l'unité de code testée lors d'un test unitaire ?
141.	Quelles sont les caractéristiques d'un bon test unitaire ?
142.	Qu'est-ce qu'une assertion dans un test unitaire ?
 
## English
1)	What does JavaScript enable you to do on a website ?
a.	Add interactive behavior and dynamic content
b.	Define the layout and design of web pages
c.	Handle server-side operations
2)	Which programming language is primarily used for server-side web development ?
a.	PHP
b.	JavaScript
c.	HTML
3)	What is the purpose of a web browser ?
a.	To render and display web pages
b.	To execute serve-side code
c.	To manage databases
4)	What is the difference between GET and POST methods in HTTP ?
a.	GET retrieves data from a server, while POST submits data to a server
b.	GET submits data to a server, while POST retrieves data from a server
c.	GET and POST methods are interchangeable
5)	What is the purpose of version control systems (e.g., Git) in web development ?
a.	To track changes and manage collaborative development
b.	To optimize website loading speed
c.	To handle server-side scripting
6)	What is the purpose of a framework in web development ?
a.	To provide a structured environment for building web applications
b.	To handle network protocols and data transfer
c.	To create visual designs and layouts for websites
7)	What does NoSQL stand for ?
a.	Not Only SQL
b.	Non-Structured Query Language
c.	New Object-Oriented Language
8)	Which of the following is a characteristic of NoSQL databases ?
a.	Strict schema enforcement
b.	Support for complex transactions
c.	Scalability and flexible data models