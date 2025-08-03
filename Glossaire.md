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

        Pour exécuter un script PHP, il faut deux éléments essentiels :
            1.	Un serveur web
                → C’est un programme (comme Apache ou Nginx) qui reçoit les requêtes envoyées par un navigateur,
                → traite la demande,
                → puis renvoie le résultat (page HTML, image, JSON…).

            Exemples de serveurs web :
            •	Apache
            •	Nginx

            2.	Un interpréteur PHP
                → C’est le programme qui lit le code PHP,
                → Exécute les instructions,
                → Produit un résultat (souvent en HTML) que le serveur web transmet ensuite au navigateur.

        Logiciels qui regroupent tout cet environnement

            Certains logiciels installent Apache + PHP + MySQL dans un seul pack, et permettent de lancer facilement un environnement local :
                •	MAMP (Utilisé sur Mac)
                •	XAMPP (Disponible sur Windows, macOS et Linux)

        MOTS CLÉS :
            •	Serveur web → reçoit – traite – renvoie
            •	Interpréteur PHP → lit – exécute – génère
            •	MAMP / XAMPP → environnement complet pour exécuter PHP en local

2.	Qu’est-ce qu’un algorithme ?  

    Un algorithme, c’est une suite d’instructions (finies), qu’on suit étape par étape, dans un ordre logique, pour résoudre un problème ou arriver à un résultat.
    Il peut y avoir des boucles, des conditions… mais il doit toujours finir.
        
        MOTS CLES : INSTRUCTION - ETAPE - PB ou RESULTAT

3.	Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?

        Une variable, c’est un nom qu’on donne à une donnée pour la stocker en mémoire et pouvoir la réutiliser ou la modifier plus tard.
        Elle peut contenir du texte, un nombre, une date, un tableau, etc.
        En PHP, toutes les variables commencent par le symbole $.
            
            MOTS CLÉS : nom – donnée – mémoire – réutiliser / modifier – $

4.	Qu’est-ce que la portée d’une variable ?

    La portée d’une variable, c’est l’endroit du code où elle “vit” et où on peut l’utiliser.
        •	Si elle est déclarée en dehors d’une fonction, on dit qu’elle est globale.
        •	Si elle est déclarée dans une fonction, elle est locale (visible uniquement dans cette fonction).

    Et si on veut utiliser une variable globale à l’intérieur d’une fonction, on doit l’appeler avec le mot global au début de la fonction.
        
        MOTS CLÉS : portée – globale – locale – fonction – global

5.	Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?

    Une constante, c’est comme une variable : c’est un nom qu’on donne à une donnée.
    Mais sa valeur ne change jamais : elle est fixe du début à la fin du script.
    On ne met pas de $ devant une constante.
    Et pour la créer, on utilise define() ou const.

    MOTS CLÉS : constante – valeur fixe – pas de $ (– define – const – ≠ variable)

6.	Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation 

en loccurance une super gbloable est une fonction native 


7.	Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)


8.	Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?

oui il existe plusieurs types de tableaux en php notamment 
les tableau. dit sompl e
tableaux associatif
et les tableau imbriqué 


9.	Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles


10.	Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?


11.	Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP
12.	Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
13.	Quelle est la différence entre les instructions « require » et « include » en PHP
14.	Comment effectuer une redirection en PHP ?
15.	Définir la partie « front-end » et « back-end » d’une application
16.	Définir le contrôle de version ? Qu’est-ce que Git ?
17.	Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

## Front-end
18.	Définir HTML
19.	Définir CSS
20.	Définir Javascript
21.	Définir JSON. Dans quel contexte ce format est-il utilisé ? 
22.	Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
23.	Qu’est-ce qu’un sélecteur CSS ?
24.	Quelle balise HTML permet de créer un lien hypertexte ?
25.	Qu’est-ce qu’une requête AJAX ?
26.	Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
27.	Définir le responsive design
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