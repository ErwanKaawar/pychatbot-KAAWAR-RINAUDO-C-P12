# pychatbot-KAAWAR-RINAUDO-C

Projet demandé par EFREI PARIS, développé par Erwan KAAWAR et Lucas Rinaudo, étudiants de L1 GROUPE C PROMO 2028.

Procédure d'installation et d'utilisation des fichiers:

    -    Merci de bien regrouper l'ensemble des fichiers/dossiers dans un même dossier pour le bon fonctionnement des différents programmes.
    
    -    les fichiers cleaned et speeches ne doivent pas être renommés pour le bon fonctionnement du programme
    
    -    le dossier speeches doit contenir un total de 8 fichiers texte, ces fichiers ne doivent pas être renommés
    
    -    le dossier cleaned contient à l'installation 8 fichiers texte, ces fichiers peuvent être supprimés pour vérifier le bon fonctionnement de fonctions telles             que : Ponctuations ou ConvertirMin
    
    -    le fichier main.py va permettre de tester les différentes fonctions contenues dans le dossier FonctionsProjet.py
    
Liste des bugs connus :

    -     Il se peut qu'il y ait des fois des erreurs ressemblant à PermissionError: [Errno 13] Permission denied: 'cleaned/Nomination_Chirac1.txt'
        si c'est le cas, après plusieurs re-éxecution la fonction devrait marcher.

    -     Aucun mot ne peut avoir dans chaque document un score TF-IDF égal à 0 c'est pour cela que dans la fonction motnonimportant, nous avons calculé la moyenne
        des TF-IDF et pas simplement le fait que la somme des TF-IDF soit égale à 0.
        
    - L'utilisation de la fonciton reponse generer avec le modele moodle : "Peux-tu me dire comment une nation peut-elle prendre soin du climat ?" en utilisant
    le menu ne donne pas la réponse attendu, cependant si on l'utilise dans fonction_Projet en ajoutant et executant
    print(reponse_generer("cleaned","Peux-tu me dire comment une nation peut-elle prendre soin du climat ?")) , On va alors obtenir le resultat du moodle  
    
     - Probleme avec l'utilisation de github, une seule personne a pu ajouter les informations du code sur le github, nous avons alors mis dans le README qui a créé chaque fonction
     Plusieurs repositories ont été créés dû à cela 

Notice d'utilisation des différentes fonctions :

    Pour exécuter les différentes fonctions, il suffit d'appuyer sur l'îcone "exécuter" dans le fichier main.py et de suivre les instructions, vous n'aurez qu'à taper le numéro de la fonction dont vous souhaitez exécuter et les différentes entrées à saisir
    
    A savoir, merci de ne pas exécuter la fonction ponctuation avant la fonction ConvertirMin
    et merci de ne pas exécuter les fonctions 5 à 13 avant ConvertirMin et Ponctuation

    Liste des différentes fonctions:
    Pour toutes les fonctions exécutées avec le menu dans main, merci de ne pas mettre l'input entre guillemets lorsqu'on vous demande d'en saisir.

    1 - Noms_president : Cette fonction va vous permettre d'obtenir le nom du président avec le nom de son fichier, Merci de bien vouloir respecter la syntaxe Nomination_NomdupresidentNumero.txt (PAR ERWAN)
    
    2 - prenoms : Vous allez pouvoir obtenir le prénom du président en entrant son nom (PAR ERWAN)
    
    3 - ConvertirMin : cette fonction va convertir toutes les majuscules d'un document texte en minuscule, elle va ensuite les stocker dans le dossier cleaned (PAR LUCAS)

    4 - Ponctuation : Cette fonction va supprimer toutes les ponctuations dans une liste de fichiers, merci d'exécuter la fonction ConvertirMin avant celle-là (PAR LUCAS)

    5 - Calcul TF : Cette fonction va calculer le score TF de chaque mot dans un document (PAR LUCAS)

    6 - Calcul IDF : Cette fonction va calculer le score IDF de chaque mot dans le corpus de documents (PAR ERWAN)

    7 - Matrice TF-IDF : Cette fonction va calculer le score TF-IDF de chaque mot dans chaque document (PAR ERWAN)
        La matrice se lit de la manière suivant : [[Mot1, scoreTFIDF_doc1, scoreTFIDF_doc2,...,scoreTFIDF_doc8],[Mot2, scoreTFIDF_doc1,                          
        scoreTFIDF_doc2,...,scoreTFIDF_doc8],...]
        
        Nous avons donc le mot en premier indice de chaque liste puis les scores de chaque document de 1 à 8
            les numéros de chaque document sont donnés dans l'ordre croissant des noms des fichiers, le numéro 1 sera alors celui de Chirac1 et le 8 celui de 
            Sarkozy
            
    8 - mot non important : Cette fonction va retourner une liste de tous les mots non importants (PAR ERWAN)
        Nous avons fait la moyenne de tous les scores TF-IDF pour et on a pris ceux qui étaient très proches de 0 car aucun mot à un score TF-IDF égal à 0 dans            tous les documents

    9 - mot score TF IDF MAX : cette fonction va retourner une liste du mot ou des mots ayant le plus grand score TF IDF (PAR LUCAS)

    10 - mot utilisé : Cette fonction va vous retourner les noms des présidents utilisant le mot demandé (PAR LUCAS)

    11 - mot repete : cette fonction va retourner la liste des ou du mot le plus répété par un president et le nombre de fois qu'il l'a répété (PAR ERWAN)

    12 - climat ecologie : cette fonction va indiquer le premier président à parler du climat et/ou de l’écologie (PAR LUCAS)

    13 -  mot hormis non important : Cette fonction va indiquer les mots que tous les présidents ont prononcés hormis les mots non importants (PAR ERWAN)

    14 - doc_pertinent : Cette fonction va renvoyer le document dans lequel se trouve la phrase ayant la plus grande similarité avec la question posée parmi toutes les autres phrases du corpus
    (PAR LUCAS)

    15 - produit_scalair : Cette fonction effectue le calcule du produit scalaire de deux listes de même longueur. (PAR LUCAS)

    16 - norme : Cette fonction effectue le calcule de la norme d’une liste de nombres (PAR LUCAS)

    17 - similarité : Cette fonction va renvoyer un nombre appartenantà l’intervalle [0 ; 1] informant combien deux objets sont similaires (PAR LUCAS)

    18 - TFIDF_question : Cette fonction va renvoyer le vecteur TFIDF de la question posée (PAR ERWAN)

    19 - présence : Cette fonction va renvoyer une liste des mots étant présents dans la question posée ainsi que dans les fichiers d'un dossier donné (PAR LUCAS)

    20 - matrice_transposee : Cette fonction modifie la matrice TFIDF de sorte à ce que les lignes deviennent les documents et les colonnes deviennent le TFIDF de chaque mot de chaque document (PAR ERWAN)

    21 - reponse_generer : Cette fonction permet de retourner des réponses qui soient plus agréables et plus compréhensibles (PAR ERWAN)
    
