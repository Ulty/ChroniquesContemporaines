# Import de statblock #

La version 3.3 de la fiche de personnage Chroniques Galactiques comporte une fonction d'import de statblock (bloc d'attributs abrégé résumant les données techniques de jeu) pour les fiches de PNJ. Cette fonction tente d'extraire les données du statblock et les insère dans la fiche de PNJ.

Cette fonction est capable de récupérer :
* Le Niveau de Créature (NC)
* Le type de créature, inséré dans le champ Profil
* La taille de la créature (de "très petite" à "colossale")
* Les six caractéristiques principales (FOR, DEX, CON, INT, SAG/PER, CHA)
* Les attributs de combat (PV, DEF et Init)
* Les diverses lignes d'attaque

## Mode d'emploi ##
Pour importer un statblock et récupérer ses données dans une fiche de PNJ :
1. Copier le texte du statblock depuis un document PDF
2. Sur l'onglet _PNJ_ et le sous-onglet _Configuration_, cliquer sur la flèche _Importer statblock_ pour afficher le champ d'import
3. Coller le texte précédemment copié dans le champ approprié
4. Cliquer en dehors de ce champ : la fonction d'import se déclenche

Si l'import se déroule sans encombres, le champ contenant le statblock est effacé.

Si un problème se pose au cours de l'import et que la fonction n'est capable d'extraire qu'une partie des données du PNJ, un ou plusieurs messages explicitant l'origine du problème sont affichés dans le champ texte résultat.

Si le champ contenant le statblock n'est pas effacé, il s'agit d'une erreur d'analyse ayant entraîné l'arrêt de l'import.

## Format du statblock ##

_NC xxx, créature xxx, taille xxx_                                                                         
_FOR xxx DEX xxx CON xxx_                                                                                
_INT xxx PER xxx CHA xxx_                                                                                        
_DEF xxx PV xxx (RD xxx) Init xxx_                                                                               
_Attaque/Arme (autres info) +Bonus DM Dommages (autres infos)_                                             
_Autre attaque DM Dommages (autres infos)_                                             

Toutes les données n'ont pas obligatoirement à être présentes. La fonction d'import extrait celles qu'elle trouve et les insère dans les champs appropriés de la fiche de PNJ, les autres seront à remplir manuellement.

## Trucs & astuces ##
* Lorsque le statblock est collé dans le champ d'import, prenez soin de supprimer les sauts de lignes surnuméraires, qui surviennent souvent sur la première ligne du bloc ou sur les lignes d'attaques
* Une ligne d'attaque est reconnue comme telle si elle comporte le mot DM.
* Le bonus d'attaque est le premier chiffre précédé d'un signe + présent sur la ligne d'attaque
* Les dommages sont le premier mot de la ligne d'attaque après le mot DM
* La fonction d'import regroupe les autres infos de la ligne d'attaque dans un champ _Spécial_ et si elle y détecte la mention d'un jet de dés, elle remet celui-ci en forme de manière à effectuer un _"inline roll"_ lorsque l'attaque est utilisée.
* Toutes les données extraites du statblock qui ne correspondent pas à un champ sur la fiche de PNJ sont regroupées dans le champ texte _Capacités_
