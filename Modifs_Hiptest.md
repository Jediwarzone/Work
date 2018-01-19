--------------------------------------------------------------------------------------------------------------------------------------------------------
*18/01/2018*

# Modifs sur Hiptest

	mettre un tag et aller le récupérer dans la page **Fait mais incomplet**
		- 900957 - Operation IG + TAS #IGTAS
		- tag primaire : GTM-NLWSWW - **OK**
		- tag secondaire1 : GTM-WPMSPT - **KO**
		- tag secondaire2 : UA-82653197-2 - **KO**

	Gérer les paramètres d'affichage du jeu **Fait**
		-	Data - Completion (Timer) && Data - Popin delay

		- **1er test : Timer** 			--> **OK**
			Timer 	(en ms)					: 3000    
			popin delay (en ms)			: default
			-->

		- **2ème test : Popin delay** --> **OK**
			Timer 	(en ms)					: default
			popin delay (en ms)			: 5000
				-->

		- 900958 - Operation CG + TAS #CGTAS
	**OK pour IG + TAS**
	mais
	**KO pour CG + TAS**

## JEU : Texte consolante gagnée (lot de consolation) **Fait**
### Duplication de l'opération :
- 900958 - Operation CG + TAS #CGTAS
--> 900959 - Operation IG100%-loose-#IG%loose
	- Ajout d'IG
	- Paramétrage du lot de consolation 100% gagné

--------------------------------------------------------------------------------------------------------------------------------------------------------
*17/01/2018*

#Liste des Scénarii FO en erreur :
**[PTFJ-1415160]** Bloc Codes : Contrôle des codes générés
**[PTFJ-1341511]** Validation de la preuve d'achat
**[PTFJ-1366272]** Format de la page de saisie des preuves d'achat
**[PTFJ-1402735]** Jeux - Carte à gratter
**[PTFJ-1413967]** Format de la page d'inscription (full option)

# Modifs sur Hiptest
## Duplication de l'opération :
- 900954 - Operation Confirmation TAS #TAS
--> 900957 - Operation IG + TAS #IGTAS
	- Ajout d'IG

## Duplication de l'opération :
- 900957 - Operation IG + TAS #IGTAS --> 900958 - Operation CG + TAS #CGTAS
	- Ajout de CG
	- Ajout de nécessité d'un code de participation en tant que Preuve d'achat

# Etats du paramétrage pour Hiptest :

## OPERATION : Url du lien de reprise
->  **Peut le faire**
- créer une participation IG
- abandonnée en cours (avt jeu)
- récupèrer token de reprise (bo)
- génèrer scénario sur ce token

## OPERATION : Mécanique
->  **Peut le faire**
- autres mécaniques testées au travers des paramètres associés aux IG, TAS, ...
- testés au travers de cinématique sur les opérations réelles
(CG + tas : récupérer code gagnant + message inscription au TAS sur page de remerciement)

## STATISTIQUES : Tag
->  **Peut le faire****
- mettre un tag et aller le récupérer dans la page (TBOS pour avoir Tag analytics primaire et secondaire de recette)
	**Réponse TBOS : Seulement primaire car jamais utilisé secondaire** (fonctionnement non assuré)
		- tag primaire : GTM-NLWSWW
		- tag secondaire : GTM-WPMSPT

## JEU : Data - Completion (Timer)
-> **Peut le faire**
- peut essayer de les faire
- check sur le délai d'affichage pour vérifier les delais d'affichage
- tester en 5 et 10 sec pour valider présence + disparition de la popin

## JEU : Data - Popin delay
-> **Peut le faire**
- peut essayer de les faire
- check sur le délai d'affichage pour vérifier les delais d'affichage
- tester en 5 et 10 sec pour valider présence + disparition de la popin

## REMERCIEMENT : Partage email
-> **Peut le faire**
- peut etre le partage email donc testé avec l'email

## PARTAGE : tous
-> **Peut le faire**

## ERREUR : titre
-> **Peut le faire**
- tenter de forcer l'erreur pour test titre

## CHANCE SUPPLEMENTAIRE : Règle de participation Facebook (TAS)
-> **Peut le faire**
- voir pour avoir des données de recette pour faire du partage

## PRE-INSCRIPTION : Participation Invalide -> Voir avec RLER
-> **Mis de côté**
- se connecter en /preregister avec les paramètres qui vont avec.

## INSCRIPTION : Afficher opt-in Industriel si deja pré-coché ?  
-> **Mis de côté pour l'instant** (tant qu'on ne teste pas ITM)
- Possiblement connexion par pré-inscription drive (voir ac RLER ou référentiel pour avoir un compte avec un optin activé)
- un test ac optin activée
- un test sans optin activée
- plus pour ITM (n'existe pas sur le drive)

## JEU : Texte consolante gagnée (lot de consolation)
-> **Peut le faire**
- perd à un IG pour un jeu 100% gagnant
- plusieurs dotations à gagner dont une consolante attribuée pour ceux qui n'ont pas gagné les dotations principales
- voir ac RLER pour créer l'opération si pas réussi
-	deux optins :
	- coche consolante 100% gagnée 	= texte consolante gagnée
	- coche consolante 				= texte perdu

## REGLES : E-mail
-> **Peut le faire**
- voir ac RLER pour la configuration d'email
- config dans op : 011549 - Produits Laitiers 2018 #reelle

## RESOURCE : Voir avec RLER
-> **Mis de côté pour l'instant**

## Mis de côté :
- Formulaire de reprise
- Ajout de réclamations
- Version des ressources
- Resources

--------------------------------------------------------------------------------------------------------------------------------------------------------
*16/01/2018*

# Modifs sur Hiptest :

## Duplication de l'opération : 900701 - Operation Inscription seule #Form
==> 900702 - Operation Inscription Fulloption #FullForm
- ajout des pages ACCUEIL et CONNEXION pour faire fonctionner le scénario HIPTEST
- ajout de règle de participation

## Duplication de l'opération : 900602 - Mécanique IG Gagnants #mechanic
==> 900604 - Mécanique IG Participation#rules
- ajout de règle de participation


--------------------------------------------------------------------------------------------------------------------------------------------------------
*15/01/2018*

# Modifs sur Hiptest :
## Duplication de l'opération : 900952 - Operation Test Preuve achat #TAS
==> 900956 - Operation Test Preuve achat #TAS_3

## Duplication de l'opération : 900952 - Operation Test Preuve achat #TAS
==> 900955 - Operation Test Preuve achat #TAS_2
- Règle pour passer la page : validCode('000', ['2017-11-20', '2017-12-23'], false, false) --> TRUE

## Duplication de l'opération : 900302 - Disclaimer SMS #disclaimer
==> 900303 - Disclaimer_false #disclaimer
- Règle pour passer la page : FALSE --> TRUE

## Modification de l'opération : 900951 	Operation Test TAS #TAS ==>

--------------------------------------------------------------------------------------------------------------------------------------------------------
*12/01/2018*

# Modifs sur Hiptest :
## Modification de l'opération : 900954 - Operation Confirmation TAS #TAS
- modification des règles d'affichages de la page INSCRIPTION (civilité et date de naissance =  false)
- modification des règles d'affichages de la page POINT DE VENTE (règle de la page = false)   null !== chooseShopAt

--------------------------------------------------------------------------------------------------------------------------------------------------------
 *11/01/2018*

# Modifs sur Hiptest :
## Duplication de l'opération : 900951 - Operation Test TAS #TAS  
==> 900954 - Operation Confirmation TAS #TAS
- Modification des textes
- Travail sur les règles d'affichage de la page de confimation
- Travail sur les règles d'affichage de la page d'inscription
- Ajout de champs dans la page inscription (Civilité + Date de naissance)
- Ajout de champs dans la page confimation (Civilité + Date de naissance + Adresse + PDV)
- Ajout de configuration pour la page remerciement

## Utilisation de l'opération : 900206 - PréJeu Quiz Juste Une Fois #pregame
Pour référencement du "texte pre-jeu perdant"

--------------------------------------------------------------------------------------------------------------------------------------------------------
*10/01/2018*

# Modifs sur Hiptest :
## Création de l'opération : 900904 - Operation Test Jeux
Par duplication de l'opération 900902 - Operation Test IG Gagnant #IG

## Ajout des différents types de jeux

--------------------------------------------------------------------------------------------------------------------------------------------------------
*08/01/2018*

# Modifs sur Hiptest :
## Modification : 900901 - Operation Test IG Perdant #IG
Ajout du pré-jeu (paramètres) +  configuration minimal (pages)
avec dates / bouton validez / réponse obligatoire

## Modification : 900902 - Operation Test IG Gagnant #IG
Ajout du pré-jeu (paramètres) +  configuration minimal (pages)
sans dates / bouton validez / réponse obligatoire

## Modification : 900903 - Operation Test Dotations IG #IG
Ajout du pré-jeu (paramètres) +  configuration minimal (pages)
Règle pour passer la page : true

--------------------------------------------------------------------------------------------------------------------------------------------------------
*29/12/2017*

# Modifs sur Hiptest :
## Remerciement :

lien externe 							: lien externe
Règle d'affichage du lien externe 		: true
Emplacement du bouton "Rejouer"			: Dans la page de remerciements
Partage (activé) 						: Facebook / Twitter / E-mail
Texte de partage 						: Texte de partage
Texte de partage secondaire				: Texte de partage secondaire
Règle d'affichage du texte secondaire 	: false

Lien de partage de l'opé Facebook	: Lien de partage de l'opé Facebook
Identifiant App Facebook 			: Identifiant App Facebook
Texte Facebook titre 				: Texte Facebook titre
Texte Facebook contenu 				: Texte Facebook contenu
Lien de partage de l'opé Twitter 	: Lien de partage de l'opé Twitter
Texte Twitter 						: Texte Twitter

--------------------------------------------------------------------------------------------------------------------------------------------------------
*28/12/2017*

# Modifs sur Hiptest :
## Disclaimer : PTFJ-900302
Validation des champs :
	- Slug
	- Titre
	- Texte principal
	- Contenu

## PDV : PTFJ-900302
Validation des champs :
	- Slug
	- Titre
	- Texte principal
	- Contenu

## Inscription : PTFJ-900302
Validation des champs :
	- optin partenaire + activation
	- optin industrielle + activation
--------------------------------------------------------------------------------------------------------------------------------------------------------
*07/12/2017*

# Modifs sur Hiptest :
## Opération 011480 - Parapharmacie
### Vérification du dédoublonnage de la preuve d'achat :
Modification dans les paramètres de la page "Preuve d'achat"
"  source !== null or validCode('000', ['2017-11-20', '2017-12-23'], false, true)  "
"  source !== null or validCode('000', ['2017-11-20', '2017-12-23'], false, false)  "

## Opération 900014 - Opération interrompue
### Accès à une opération interrompue :
Modification des dates d'interruptions  -->
03/12/2017 00:00:00 au 05/12/2017 00:00:00
CHANGE EN
03/12/2017 00:00:00 au 10/12/2017 00:00:00
Ajout d'un titre et d'un contenu pour la page d'interruption  --> Opération interrompue + texte

## Opération 109459 - Jeu Trade Marketing (Testing)
### Modification des dates d'interruptions  -->
07/12/2017 15:44:50 au 08/12/2017 15:44:50
CHANGE EN
06/12/2017 15:44:50 au 07/12/2017 15:44:50

### Ajout de quantité de dotations --> De 0 à 1 de chaque code article.
### Ajout de date d'IG en Sandbox  --> 07/12/2017 14:13:39 au 07/12/2017 14:13:39 (3 IG, une par produit)
