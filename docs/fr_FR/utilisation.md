# Utilisation  
## Le widget  
Le widget est décopmosé en six zones , en fonction des options installés dans le notif'heure.  
  * Bloc 1 :  
  ![screenshot1](../images/partie1.png)  
  La partie haute représente l'etat du notif'heure en fonction des commandes envoyés .  
    * OFF   
        ![screenshot1](../images/off.png)   
    * Affichage des secondes  
        ![screenshot1](../images/partie1.png)
    * Masquage des secondes  
        ![screenshot1](../images/secoff.png)
    * Mode automatique ou Manuel  
        ![screenshot1](../images/manu.png)
    * Temoin led on / off  
        ![screenshot1](../images/ledon.png)   

  * Bloc 2 : Réglage de l'intensité pour le mode Manuel ( des que l'on modifie ce paramétrage le Notif'Heure passe en Mode Manuel pour la luminositée ).
  l'info Mode manuel  et valeur , s'affiche dans le bloc 1.  

  ![screenshot1](../images/partieint.png)

  * Bloc 3 : Options et Notification à envoyer.  

  ![screenshot1](../images/partienotif.png)

  Les Options possibles sont ( séparation possibles : , ou ; ou - ou : ) . Par exemple : _lum=8 , type=INFO , fio = 24 , important_   
  indiquera une luminosité de 8 , affichage de type INFO avec un effet en entrée et sortie de 24 , et ajoutera le tag important afin de le marquer pour l'historique.


  * **lum** : de 0 à 15 pour indiquer une valeur de luminositée  
  * **type** : Type d’animation ou de comportement BLINDS ,PAC ou OPENING : pour des effets d’animation avant la notification affiche l’info “txt” , contenu dans la variable txt.  
    * INFO : associé au champ “pause” permet d’afficher un texte court  entre 0 et 60 secondes.  
    * FIX : Affiche un texte court , en permanence . Une nouvelle notification envoyée , enleverra le texte. Pour la version notifheure standard si , on désire effacer , il faut utiliser le mot clé ” **!Clear!**” dans le champ message. Pour la version XL , il suffit d'envoyer un message avec juste un espace .
  * **txt** : Un mot a afficher avant les effets d’animation ( la valeur par défaut renseigner dans la page de création sera utilisé si l'option txt n'existe pas ).  ( **version notifheure uniquement**)
  * **pause** : Associé à INFO , permet de définir un temps d’affichage entre 0 et 60 secondes.  
  * **flash** : pour activer le flash lumineux avant notification ( si LED présente )  
  * **important** : Permet de rajouter un tag sur le message pour l’historisation et notification LED si présente.
  * **fi**,**fo** ou **fio** : permet de choisir un effet pour la commande de type INFO . fi pour l’effet d’entrée , fo pour l’effet de sortie et fio pour définir le même effet en entrée et sortie. Par exemple fio=26,type=info permet un scrolling de la droite vers la gauche.     

##### Mots clef pour version XL

* **nzo** : Numéro de zone sur laquelle afficher la notification
* **anim** : Numéro animation à jouer pour la notification ( voir tableau ci-dessous)
* **fx** : Numéro d'effet pour notification .

L'option **type** est prioritaire sur les options anim et fx.

#### Listes Codes Animation ( anim= xx )  NOTIFHEUREXL

|Code| Désignation        |
|:--:|--------------------|
|0|	PAC MAN
|1|	FLECHE 1
|2|	ROLL 1
|3|	MARCHEUR
|4|	SPACE INVADER
|5|	CHEVRON
|6|	COEUR
|7|	BATEAU VAPEUR
|8|	VOILIER
|9|	BOULE DE FEU
|10|	ROCKET
|11|	LIGNE
|12|	VAGUE
|13|	FANTOME PAC MAN
|14|	FLECHE 2
|15|	ROLL 2




  #### Listes Codes effets (fi,fo, fio)  NOTIFHEURE

|Code| Désignation        |
|:--:|--------------------|
|0|	Apparition / disparition par point
|1|	Affichage sans effet
|2|	Effet scanner horizontal
|3|	Scrolling gauche
|4|	Ne fait rien ( sert pour le fix )
|5|	Apparition / disparition effet efface
|6|	balayage verticale
|7|	Scrolling diagonal haut-gauche
|8|	Scrolling Haut
|9|	Fondu
|10|	Effet curseur ouverture
|11|	Apparition / Disparition par le bas
|12|	Scrolling diagonal haut-droite
|13|	Blinds ( effet persienne )
|14|	PAC MAN    /   PAC MAN + fantôme
|15|	Ouverture / Fermeture
|16|	Apparition / Disparition par le haut
|17|	effet scanner vertical
|18|	Scrolling diagonal bas-gauche
|19|	curseur horizontal
|20|	balayage horizontal
|21|	Brouillage
|22|	Entrelaçement
|23|	Fermeture / Ouverture
|24|	Effet curseur fermeture
|25|	Scrolling diagonal haut-gauche
|26|	Scrolling droite
|27|	effet tranche
|28|	Scrolling bas

#### Listes Codes effets (fi,fo, fio , fx )  NOTIFHEUREXL

|Code| Désignation        |
|:--:|--------------------|
|0|	PRINT
|1|	SCROLL LEFT
|2|	SCROLL UP LEFT
|3|	SCROLL DOWN LEFT
|4|	SCROLL UP
|5|	GROW UP
|6|	SCAN HORIZ
|7|	BLINDS
|8|	WIPE
|9|	SCAN VERTX
|10|	SLICE
|11|	FADE
|12|	OPENNING CURSOR
|15|	CLOSING
|16|	SCAN VERT
|17|	WIPE CURSOR
|18|	SCAN HORIZX
|19|	DISSOLVE
|20|	MESH
|21|	OPENNING
|22|	CLOSING CURSOR
|23|	GROW DOWN
|24|	SCROLL DOWN
|25|	SCROLL DOWN RIGHT
|26|	SCROLL DOWN RIGHT
|27|	SCROLL RIGHT
|28|	Random


  Vous pouvez retrouvez la documentation compléte sur mon site : https://byfeel.info

* Bloc 4 : Retrouvez les infos du DHT , si celui ci sont présentes dans le NotifHeure ( les infos sont réactualisés toutes les 30 minutes ).  

  ![screenshot1](../images/infodht.png)  

* Bloc 5 : Les commandes

  ![screenshot1](../images/commandes.png)   

  Dans l'ordre :
  * Off : Supprime affichage de l'Horloge  
  * On(reveil) : Affiche l'horloge  
  * Plus : Affiche les secondes si masqué
  * Moins : Masque les secondes  
  * Auto : Active le mode Auto  
  * Led On : Allume la led  
  * Led Off : Eteind la led  

* Bloc 6 : Le minuteur   
![screenshot1](../images/minuteur.png)   
  * Le - et le + pour incrementer le temps du minuteur . L'option increment dans "Paramètres optionnels sur la tuile" permet de modifier l'unité d'increment par défaut : 1  
  * Bouton play : Pour lancer le minuteur  
  * Bouton Stop : Pour annuler le minuteur  
  * Bouton "magic" : Pour afficher / Masquer le minuteur
