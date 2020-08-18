# Import de statblock

La version 2.4 de la fiche de personnage Chroniques Oubliées Contemporain comporte une fonction d'import de statblock (bloc d'attributs abrégé résumant les données techniques de jeu) pour les fiches de PNJ. Cette fonction tente d'extraire les données du statblock et les insère dans la fiche de PNJ.

Cette fonction est capable de récupérer :

- Le nom de la créature
- Le Niveau de Créature (NC), inséré dans le champ Niveau
- Le type de créature, inséré dans le champ Profil
- La taille de la créature (de "très petite" à "colossale")
- Les six caractéristiques principales (FOR, DEX, CON, INT, SAG/PER, CHA)
- Les attributs de combat (PV, DEF et Init)
- Les diverses lignes d'attaque
- Les diverses capacités

## Mode d'emploi

Pour importer un statblock et récupérer ses données dans une fiche de PNJ :

1. Copier le texte du statblock depuis un document PDF
2. Sur l'onglet _PNJ_ et le sous-onglet _Caractéristiques_, cliquer sur la flèche _Importer statblock_ pour afficher le champ d'import
3. Coller le texte précédemment copié dans le champ approprié
4. Cliquer en dehors de ce champ : la fonction d'import se déclenche
5. Depuis la version 3.4 de la fiche, c´est un bouton qui permet de lancer la fonction d´import

Si l'import se déroule sans encombres, le champ contenant le statblock est effacé.

Si un problème se pose au cours de l'import et que la fonction n'est capable d'extraire qu'une partie des données du PNJ, un ou plusieurs messages explicitant l'origine du problème sont affichés dans le champ texte résultat.

Si le champ contenant le statblock n'est pas effacé, il s'agit d'une erreur d'analyse ayant entraîné l'arrêt de l'import.

## Format du statblock

_Nom_    
_NC xxx, créature xxx, taille xxx_  
_FOR xxx DEX xxx CON xxx_  
_INT xxx PER xxx CHA xxx_  
_DEF xxx PV xxx (RD xxx) Init xxx_  
_Attaque/Arme (autres info) +Bonus DM Dommages (autres infos)_  
_Autre attaque DM Dommages (autres infos)_

_Nom de la capacité : Description de la capacité_

Toutes les données n'ont pas obligatoirement à être présentes. La fonction d'import extrait celles qu'elle trouve et les insère dans les champs appropriés de la fiche de PNJ, les autres seront à remplir manuellement.

## Trucs & astuces

- Après avoir collé le statblock dans le champ d'import, prenez soin de supprimer les sauts de lignes surnuméraires, en particulier sur la première ligne du bloc (nom du PNJ/créature ou NC et type) et sur les lignes d'attaques
- Si la première ligne du statblock ne commence pas par le mot 'NC', elle est considérée comme contenant le nom du PNJ ou de la créature
- Une ligne d'attaque est reconnue comme telle si elle comporte le mot 'DM' ou qu´elle commence par le mot 'attaque'.
- Le bonus d'attaque est le premier chiffre précédé d'un signe + présent sur la ligne d'attaque
- Les dommages sont le premier mot de la ligne d'attaque après le mot DM
- La fonction d'import regroupe les autres informations de la ligne d'attaque dans un champ _Spécial_ et si elle y détecte la mention d'un jet de dés, elle remet celui-ci en forme de manière à effectuer un _"inline roll"_ lorsque l'attaque est utilisée.
- Les traits et capacités peuvent être séparées des attributs de base et des lignes d'attaque soit par une ligne vide, soit par au moins 3 tirets '---', soit par le mot 'Capacité'.
- Les descriptions de capacités sont également traitées pour transformer toute mention d´un jet de dés en _"inline roll"_
- Les données extraites du statblock qui ne correspondent pas à un champ sur la fiche de PNJ sont regroupées dans le champ texte _Capacités_
