# AEL
AIde en ligne Ilias 7 en Français

Aide en ligne dans ILIAS 7

Actuellement, aucune version d'ILIAS ne permet de changer de langue pour les fichiers d'aide en fonction des préférences linguistiques de l'utilisateur.

Même si vous faites traduire le fichier d'aide dans une autre langue et que vous téléchargez ce fichier dans ILIAS, vous ne pourrez toujours pas utiliser plus d'une langue.

L’aide en ligne d’Ilias est à ce jour disponible uniquement en langue allemande.
La feuille de route d’Ilias indique une évolution multilingue à compter de la version 9.
https://docu.ilias.de/goto_docu_cat_3255.html

Toutefois j’ai entrepris la traduction de l’aide en ligne en français. Celle-ci est désormais fonctionnelle sous deux conditions :

1.	Quelques modifications du code Ilias7
2.	De ne pas basculer Ilias sur une autre langue

Ainsi :

Si votre langue principale est le français, que vous souhaitez avoir l'aide en ligne en français et que vous n'envisagez pas de basculer entre le français et une autre langue, voici la solution de contournement :

ÉTAPE 1

•	Télécharger le package 1685555255__6127__lm_190.zip
•	NE renommez AUCUN des fichiers du package
•	NE renommez PAS le fichier .zip
•	Dans votre installation ILIAS, ouvrez « Administration » > « Aide en ligne »
•	Téléchargez votre package .zip traduit. Le téléchargement peut prendre plusieurs minutes
•	Cliquez sur Activer à droite du titre de l'aide

ÉTAPE 2
Modifiez la langue du système d'aide de « de » à « fr » dans les quatre fichiers suivants :

•	Dans Services/Help/classes/class.ilHelp.php
remplacez
if ($ilUser->getLanguage() != " de ") {
par
if ($ilUser->getLanguage() != " en ") {

•	Dans Services/Help/classes/class.ilHelpGUI.php
remplacez
if ((OH_REF_ID > 0 || $module_id > 0) && $ilUser->getLanguage() == " de ") {
par
if ((OH_REF_ID > 0 || $module_id > 0) && $ilUser->getLanguage() == " fr ") {

•	Dans Services/Help/classes/class.ilHelpMapping.php
remplacez
if ($ilUser->getLanguage() != " de ") {
par
if ($ilUser->getLanguage() != " en ") {

•	Dans Services/Help/GlobalScreen/classes/trait.ilHelpDisplayed.php
remplacez
if ($user->getLanguage() != " de ") {
par
if ($user->getLanguage() != " en ") {

ÉTAPE 3

•	Si vous ne l'avez pas déjà fait, réglez votre langue sur « francais » et cliquez sur le ? dans le bandeau du haut.
ILIAS ouvrira le menu d’aide.

Contact : vince.syh@free.fr

