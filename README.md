## Introduction :
Après deux années de formation à Youcode, on est appelé à réaliser un projet pour consolider nos acquis théoriques et avoir une idée sur le monde professionnel.  
Dans ce cadre, on a réalisé un projet de la presse thématique (Environnement news).
## Présentation D’école :
Youcode est une école de programmation qui ouvre les chances à tout le monde. C'est le rêve de tout débutant en codage et développement web, nouvellement créée à Youssoufia avec la collaboration du Groupe OCP et du leader français de l'éducation numérique (Simplon).
## Identification de besoin
Après la réunion avec M. Jaafar DAHBI (personnel de IT6 à Rabat), organisée dans le cadre de l'identification des problèmes confrontés par les gens intéressés par les nouveautés de la technologie et de l’informatique. À ce stade on a pu identifier les difficultés au niveau du nombre énorme des sites informatiques, et la nécessité d’une plateforme qui facilite l'accès aux nouveautés proposés par ces sites.
## Description de l'existant
Si on prend par exemple le site web Yahoo créé en 1999 constitué de plusieurs catégories et parmi ses catégories on trouve l'actualité informatique, la façon dont le site web est composé perturbe la bonne expérience de l’utilisateur par le nombre de rubriques et de pages proposés par le site et la façon de présentation des articles.
Parmi les site web qui existe est attaque le même marcher en site ci-dessous quelque exemple :
1.	https://www.unenvironment.org/
2.	https://news.mongabay.com/
3.	https://www.thegef.org/
4.	https://www.wri.org/

## Definition du projet
Dans le cadre du projet on est appelés à réaliser un projet pour la validation des compétences. La presse spécialisée regroupe l’ensemble des publications par opposition à la presse généraliste abordent un domaine particulier ou traite d’un thème précis. Comme techniques, sportifs, musicaux, littéraires ou scientifiques.
Dans notre cas en vas réaliser un site web qui publie des actualités liées à l’environnement.
## OBJECTIFS
1.	Création du Platform web d’actualités Environnement.
2.	Création d’une interface Admin (Dashboard) :
a – La gestion des profils journaliste et rédacteur chef et droit utilisateur.
b – fonctionnalité CRUD (Modification, Supression,Consultation,Ajout).
c - L’automatisation du système de notification .
3.	Consommation des flux externe (rss , rest api ).
## CARACTÉRISTIQUES
## 1. Planification
   Une première analyse du projet nous a permis de définir une suite d’étapes à suivre pour sa réalisation.
 ## 2. Spécifications fonctionnelles
   Durant cette étape, nous allons définir ce qui doit être réalisé pour atteindre chaque objectif du projet, à savoir:

•	Un espace de blog ou d’actualités.
•	Un espace admin (Dashboard).
•	Un espace journaliste.
•	Un espace de rédacteur chef
•	Consommer des API ou flux d’actualités.
•	Un Formulaire de contact.
•	Partage des liens vers les réseaux sociaux.
•	Fonctionnalité de CRUD (Ajouter, Modifier, Supprimer, Consultation).
•	Espace Twitter #Relative avec l’environnement.
•	Les notifications par mail.
•	La météo.
•	Les publicities.


## Les technologies :
Dans le programme de la formation Youcode on a étudié plusieurs langages de programmation donc pour mettre en pratique ce que nous avons appris, on a travaillé avec ces techniques dans notre projet 
•	IHM et Design graphique:
-	Programmation HTML 5 et utilisation CSS3.
-	Framework et Bibliothèque JAVACRIPT / JQUERY / Bootstrap / Bibliothèque Graphique.
-	Framework: Angular.
•	Services et Applications:
-	Injection des Dépendances et mise en œuvre de MVC.
-	Configuration et Utilisation des Framework.
-	Utilisation des Contrôleurs REST API et mécanismes des Interfaces techniques.
•	Base de données:
-	SQL.
-	Utilisation du Framework entité Framework (ORM) pour la gestion des Entités.

## 5. Conception:
   - Conception de bases de données relationnelles avec UML. 
  ## •	Diagramme de Use Case :
  
 ## •	Diagramme de classe :
 ## •	Diagramme de séquence :
  ## Les packages installés
• Microsoft.AspNet.WebApi.Cors
• Microsoft.AspNet.Identity.Core
• EntityFramework
• Miscrosoft.Owin.Cors
Conception de Code
Projet ASP.NET utilisant identité et entité Framework
Pour réalise nous projet en a divise la solution a 3 partie
• Partie RESTAPI tourisme qui contient des contrôleurs et des models.
• Partie DATA sous forme d’une bibliothèque de classe qui contient un ADO lié avec notre base de données
• Partie LOGIQUE qui contient des traitements hors métiers.
Les API à consommer
## AUTHENTIFICATION :
Api/account/logup
Pour consommer API de registrement (journaliste ,redaction en chef , gestiooner ) il faut utiliser le lien:
Api/account/logup a Authorize Gestionner 
ainsi qu’envoyer les informations au body
Nom(String), Prenom(String), Email(String),Tele(int), Statu(Bool),Role(‘journalistes’ ou ‘Gestionner’), Password(String), ConfirmPassword(String).

  ## Api/Token
• Pour s’identifier il faut utiliser /token et envoyer au body :(Post)
"username=" + Le nom d’utilisateur + "& password d’utilisateur=" + password + "&grant_type=password” ;
• Et envoyer au header une autorisation (Post)
var reqHeader = new HttpHeaders({ 'Content-Type': 
## 
## HOME:
## api/ Article /Article
• Pour avoir liste des 10 Article dans body de page Home il faut utiliser le lien (get) :
## api/ Article /Article
Int ID , date date , string Titre ,string body , string img , string video ,string NomJournaliste
## api/ Article /Articleslide
Et pour avoir 3 article dans le slide odre par date il faut utiliser le lien (get) :
## Api/article/Articleslide
Int ID , date date , string Titre ,string body , string img , string video ,string NomJournaliste
## api/Article/DaysArticle
Pour avoir liste des les Article order par 4 jours dans footer de page Home il faut utiliser le lien (get)
## api/Article/DaysArticle
Int ID , date date , string Titre ,string body , string img , string video ,string NomJournaliste
## api/ Article /DetaileArticle/id
Pour avoir detaile d’Article il faut utiliser le lien (get) avec id:
## api/ Article /DetaileArticle/id

Int ID , date date , string Titre ,string body , string img , string video ,string NomJournaliste
## api/Article/ToutArticles/id
pour avoir tous les articles a touts les status(‘posted’ , ‘onposte’,’noposted’,’archiver’) utiliser le lien get avec id (‘posted’ , ‘onposte’,’noposted’,’archiver’) :
## api/articles/toutArticles
Int ID , date date , string Titre ,string body , string img , string video ,string NomJournaliste
## api/ Article /ArticleEnPost
Pour poster un Article il faut utiliser le lien (post) :
## api/ Article /ArticleEnPost
 
## api/ Article / ArticleEnPut
pour editer article utiliser le lien (put) :
api/article/articleEnPut
api/ Article / commentEnPost
pour poster un commentair utiliser li lien (post) :
api/article/commentEnPost

##  api/ Article / comment
pour geter un monnemtair utiliser le lien (get) :
api/article/comment/id
## api/ journalist / journalistSelect/id
Pour avoir detaile de journaliste et les article ecrite il faut utiliser le lien (get) avec id:
 api/ journalist /DetaileArticle/id

 Int ID , string nom , string prenom ,string email , string tele, int nombrearticle , string img
## api/ journalist / listJournalist
Pour avoir detaile de journaliste et les article ecrite il faut utiliser le lien (get) avec id:
 api/ journalist /listJournalist
Int ID , string nom , string prenom ,string email , string tele, int nombrearticle ,
## api/ journalist / journalisteEdite
pour editer le statu de journaliste ou redaction en chef utiliser le lien(put) :
api/journalist/ journalisteEdite


## api/ RedactionEnChef / RedactionEnChef
Pour avoir detaile de redaction en chef il faut utiliser le lien (get) avec id:
 api/ RedactionEnChef/ RedactionEnChef
Int ID , string nom , string prenom ,string email , string tele, int nombrearticle ,
## api/ RedactionEnChef / RedactionEnChefs
Pour avoir liste des redaction en chef evec les article ecrit utiliser le lien (get) :
api/redactionEnChef/ redactionEnChefs
## api/ RedactionEnChef / journalisteEdite
pour editer le statu de journaliste ou redaction en chef utiliser le lien(put) :
api/journalist/ journalisteEdite

## Perspectives
Comme étant des jeunes ambitieux, nous avons biensur des perspectives en espérant que notre site web "Environnement news" soit ergonomique, avec un design attrayant, un contenu utile et intéressant puis avoir la possibilité de l'héberger en ligne pour le rendre plus pratique.
Enfin, nous espérons que notre travail sera à la hauteur de la confiance qui nous a été accordée.


 
  
  
  
  
  
  
  
  

