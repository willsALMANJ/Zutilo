Zutilo
======

Zutilo est une petite extension pour Firefox qui sert de module complémentaire à [l'extension Zotero pour Firefox](http://www.zotero.org/).
Zutilo a été conçu comme un moyen pratique d'ajouter des fonctions supplémentaires qui ne sont pas fournies par Zotero.
Son nom a été choisi pour rappeler l'idée d'utilité combinée avec Zotero.
Tous les éléments graphiques de Zutilo peuvent être désactivés séparément, de sorte que les éléments jugés inutiles n'encombrent pas l'interface utilisateur.

Liste des fonctions courantes
-----------------------------

### Raccourcis clavier ###
La plupart des fonctions de Zotero sont accessibles avec des menus contextuels qui apparaissent sous le clic droit sur les éléments pertinents de Zotero ou Firefox.
Il peut être très utile d'appeler les un grand nombre de fonctions de Zutilo directement au clavier plutôt qu'en utilisant les menus contextuels.
Raccourcis pour de nombreuses fonctions peuvent être définies dans les préférences de Zutilo.

Les fonctions de Zutilo peuvent être « mappées » en utilisant un autre module pour Firefox comme [Keyconfig](http://forums.mozillazine.org/viewtopic.php?t=72994), qui fournit une une interface simple pour le mappage des touches du clavier destinées aux commandes JavaScript, il fonctionne aussi bien avec Firefox qu'avec la version standalone de Zotero.
Vous pouvez aussi utiliser [Pentadactyl](http://5digits.org/pentadactyl/index) ou [Vimperator](http://www.vimperator.org/vimperator), qui offrent tous deux une interface plus avancée en ligne de commande pour Firefox.
Dans les descriptions de fonctions ci-dessous, les noms des fonctions correspondantes vous sont donnés.

Ce sont les noms de fonctions qui devraient être associées aux touches du clavier pour appeler des fonctions sans utiliser les menus contextuels.
.
.

### Fonction d'entrées de menu ###
.
.

* __Copier les marqueurs:__
    Cliquez droit dans la bibliothèque de Zotero et copiez les marqueurs dans le presse-papiers en tant que liste délimitée par des « \r\n ».
    .
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.copyTags()`).

* __Coller les marqueurs:__
    Cliquer droit sur des parties de la bibliothèque de Zotero et collez le contenu du presse-papiers dans celles-ci.
    Le contenu du presse-papiers doit être une liste dont les éléments sont séparés par des '\r\n' ou des '\n' (comme pour la liste créée par la fonction 'copier les marqueurs' ci-dessus).
    (nom de la fonction : `ZutiloChrome.zoteroOverlay.pasteTags()`).

* __Copier les créateurs:__
    Cliquez droit sur les éléments de la bibliothèque de Zotero et copiez les créateurs dans le presse-papiers sous forme de liste délimitée par des '\r\n'.
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.copyCreators()`).

* __Afficher le chemin des pièces jointes:__
    Afficher les chemins vers les fichiers joints sélectionnés et vers les pièces jointes aux éléments habituels sélectionnés (un par un dans une fenêtre de dialogue distincte -- vous ne voudrez sûrement pas sélectinner plus de quelques éléments à la fois de cette façon !).
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.showAttachments()`).

* __Modifier les chemins des pièces jointes:__
    Changer le début du chemin vers toutes les pièces jointes sélectionnées disponibles et vers toutes les pièces jointes aux élements habituels.
    .
    .
    .
    .

    .
    .
    .
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.modifyAttachments()`).

* __Associer les éléments:__
    Paramétrer tous les éléments sélectionnés comme pouvant s'associer les uns aux autres.
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.relateItems()`).

* __Copy select item links:__
	Copy links of the form "zotero://select/items/ITEM_ID" to the clipboard for each selected item.
	Pasting such a link into the Firefox address bar will select the corresponding item in the Zotero Firefox plugin.
	Following links from other applications and having the links select items in the Zotero Standalone client may also be achievable but might require additional set up.

* __Copy Zotero URIs:__
	Copy (www.zotero.org) links to the clipboard for each selected item.
	If you have a (www.zotero.org) profile, following such a link will open the page for the corresponding item in profile on (www.zotero.org).
	If you do not have a (www.zotero.org) profile, a placeholder link is still generated but might not be useful.

### Fonctions de modifications d'éléments ###

Zutilo implémente pour l'instant quelques fonctions qui sont utiles pour éditer les élémenst de Zotero avec le stouches du clavier.
Ces fonctions ne peuvent être appelées par une quelconque interface graphique mais on peut les assigner à un raccourci-clavier tel que décrit ci-dessous.
Les fonctions suivantes ne fonctionneront que si un seul élément de Zotero est sélectionné :

* __Modifier l'information de l'élément:__
    Sélectionnez l'onglet « Info » dans le panneau des éléments.
    Placez le curseur dans le premier champ modifiable des informations de l'élément.
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.editItemInfoGUI()`).
* __Ajouter une note:__
    Sélectionnez l'onglet « Notes » dans le panneau des éléments.
    Créez une nouvelle note.
    .
    .
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.addNoteGUI()`).
* __Ajouter un marqueur:__
    Sélectionnez l'onglet « Marqueurss » dans le panneau des éléments.
    Ouvrez une boîte de saisie de texte pour créer un nouveau marqueur.
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.addTagGUI()`).
* __Ajouter un élément associé:__
    Sélectionnez l'onglet « Associés » dans le panneau des éléments.
    Ouvrez la boîte de dialogue pour ajouter des éléments associés.
    (Nom de la fonction : `ZutiloChrome.zoteroOverlay.addRelatedGUI()`).

### Navigating and hiding panes ###

Zutilo implements several functions that are useful for navigating between and within the three main panes.
If the relevant pane is hidden, the following functions will show it.
These functions can not be called from any graphical element (but can be assigned to a keyboard shortcut as described above).

* __Focus collections pane:__
    Set the focus to the collections pane (left pane, Libraries pane).
    Added for completeness, but Zotero already has a keyboard shortcut that does this.
* __Focus items pane:__
    Set the focus to the items pane (middle pane).

The following four functions are similar to the four item editing functions above, except that they just set focus on the respective tab in the item pane.

* __Focus item pane: Info tab:__
    Select the "Info" tab in the item pane.
* __Focus item pane: Notes tab:__
    Select the "Notes" tab of the item pane.
* __Focus item pane: Tags tab:__
    Select the "Tags" tab of the item pane.
* __Focus item pane: Related tab:__
    Select the "Related" tab of the item pane.

The following two functions allow you to cycle through the same four tags in the item pane.

* __Focus item pane: next tab:__
    Select next tab in item pane.
* __Focus item pane: previous tab:__
    Select previous tab in item pane.

The following two functions allow you to easily show or hide the collections pane (left pane) and the item pane (right pane).

* __Item pane: Show / hide:__
    Show or hide the item pane.
* __Collections pane: Show / hide:__
    Show or hide the collections pane.

The following two functions achieve the same, i.e. they allow you to easily show or hide the collections pane (left pane) and the item pane (right pane).
However, when the pane is shown, the thicker vertical divider ("splitter", "grippy", appears when the pane is hidden) remains visible until the width of the pane is adjusted. 

* __Item pane: Show / hide (sticky):__
    Show or hide the item pane.
    When the pane is show, the thicker vertical divider remains visible until the width of the pane is adjusted.
* __Collections pane: Show / hide (sticky):__
    Show or hide the collections pane.
    When the pane is show, the thicker vertical divider remains visible until the width of the pane is adjusted.

### Fonctions pour le navigateur Firefox ###

Zutilo ajoute quelques fonctions pour vous aider à joindre des documents aux éléments de Zotero depuis les pages de Firefox.
Ces fonctions sont acessibles depuis le navigateur Firefox et ne sont pas disponibles avec Zotero Standalone.

* __Joindre des pages web et des liens aux éléments de Zotero:__
    Zutilo ajoute des entrées de menu contextuel à Firefox pour jondre la page courante ou la cible du lien (si un lien est sélectionné) à l'élément de Zotero sélectionné.
    Le traitement du fichier joint dépend de la méthode d'association que vous avez choisie dans les préférences de Zutilo.
    Si la méthode est « Importer », un fichier joint est importé depuis la page ou le lien.
    Si la méthode choisie est « Demander ou envoyer le fichier lié », une invite de fichier apparaît pour permettre à l'utilisateur de préciser un nouveau fichier.
    Le lien ou la page est enregistré(e) dans ce fichier puis un fichier joint lié est créé (avec un lien vers le fichier téléchargé).
    Si la méthode est « Demander après le premier », un fichier joint important est créé si l'élément sélectionné n'a pas encore de fichier joint (les captures d'écran jointes ne comptent pas).
    Sinon, l'invite de fichier pour créer un fichier joint lié est affichée.
    Si la touche majuscule est appuyée pendant que l afonction de fichier joint est activée, une invite pour fichier lié apparaît quelles que soient les préférences de Zutilo.
    .

    Si vous voulez créer un raccourci-clavier pour joindre la page courante à l'élément courant de Zotero en utilisant la méthode précisée dans les préférences, utilisez `ZutiloChrome.firefoxOverlay.attachURLToCurrentItem(window.content.location.href)` pour la commande.
    .
    .

* __Extraire un élément de Zotero de la page courante avec ou sans pièce jointe:__
    Zutilo ajoute des entrées de menu supplémentaires au menu contextuel de l'icône de Zotero dans la barre des modules qui extrait les citations de la page courante en ajoutant ou non les PDF ou autres fichiers extraits de la page.
    .
    .

    C'est-à-dire, la préférence « Joindre automatiquement les PDF et autres fichiers » est sélectionnée dans Zotero, Zutilo ajoute des entrées de menu (une entrée pour chaque méthode d'enregistrement avec Zotero qui s'applique à la page courante) pour créer un nouvel élément de Zotero sans pièce jointe.
    Si la préférence n'est pas sélectionnée, Zutilo ajoute des entrées de menu pour créer un nouvel élément Zotero sans pièce jointe.

    La fonction sur laquelle est basée cette fonctionnalité est `ZutiloChrome.firefoxOverlay.scrapeThisPage(translator, filesBool)`.
    Si un traducteur (un objet traducteur de Zotero) est sur `false` ou bien non précisé, le traducteur par défaut de la page sera utilisé.
    Si fileBool est sur `true`, l'élément est créé avec les documents joints associés.
    S'il est sur `false`, l'élément est créé sans fichiers joints.Si filesBool n'est pas précisé, alors c'est le l'inverse du comportement par défaut de Zotero qui est utilisé.
    .
    Donc, si dans les préférences de Zotero l'option « Joindre automatiquement les PDF et autres fichiers » est sélectionné, `ZutiloChrome.firefoxOverlay.scrapeThisPage(false)` créera un élément qui utilise le traducteur par défaut de la page sans joindre aucun fichier.

### Fonctions de base de Zotero ###

Pour référence, voici quelques autres fonctions de Zotero que j'ai trouvé utiles pour mapper les raccourcis-clavier:

* __Activer/désactiver Zotero:__
    Affiche/masque le panneau latéral de Zotero dans Firefox.
    (Nom de la fonction : `ZoteroOverlay.toggleDisplay()`).
* __Enregistrer la page web comme élément dans Zotero:__
    Enregistre la page courante comme un élément dans Zotero.
    (Nom de la fonction : `ZoteroPane.addItemFromPage()`).
* __Extraire un élément de Zotero d'une page web:__
    Ajoute un élément à la biblkiothèque de Zotero, basé sur le contenu de référence de la page web courante (équivalent à cliquaer sur la petite icône de page/livre dans la barre d'adresse de Firefox).
    (Nom de la fonction : `Zotero_Browser.scrapeThisPage()`).

### Comment l'installer ###

Le plus simple est d'installer l'extension Zutilo for Zotero via [la page officielle de l'extension sur AMO](https://addons.mozilla.org/en-US/firefox/addon/zutilo-utility-for-zotero/ "Zutilo's Mozilla Add-ons page").
Rendez-vous sur cette page et cliquez sur le bouton « Ajouter à Firefox ».

Pour Zotero Standalone (application autonome indépendante du navigateur), vous devrez télécharger un fichier .xpi (clic droit et "Enregistrer sous…" sur la page Zutilo de AMO) et l'installer manuellement (voir ci-dessous).
Une fois que vous avez le fichier zutilo.xpi, allez aux Outils\>Modules complémentaires soit dans Firefox, soit dans Zotero standalone.
Cliquez sur le bouton « engrenages » dans l'angle supérieur droit de la fenêtre de gestionnaire des modules qui apparaît et choisissez le fichier .xpi.

.
.
.

.
.
.

.
.
.
.
.

.
.
.
.

.
.
.
.
.

.
.
.
.
.

.
.
.
.

.

.
.
.
.
.

.
.
.

.
.

.

.
.
.

.
.
.
.

.
.
.

.

.

.

.
.
.
.
.
.
. 
.

.

.

.
.
.
.

.
.

Demande de nouvelles fonctions et signalements de bogues
--------------------------------------------------------

Le dernier code source de Zutilo est maintenu sur [GitHub](https://github.com/willsALMANJ/Zutilo "Zutilo's GitHub page").
vous pouvez faire remonter les bogues en cliquant sur le bouton "New Issue" (Nouveau problème) dans la section [Issues](https://github.com/willsALMANJ/Zutilo/issues "GitHub Issues page") du site de  GitHub.
Vous pouvez aussi vérifier si le bogue que vous rencontrez a déjà ou non été signalé par d'autres.
Veillez à vérifier l'onglet "fermé" de la section *Issues* pour voir sir le bogue a déjà été réglé.

les demandes de fonctionnalités peuvent être envoyées de cette façon.
.
.
.

.
.
.
.

.
.

.
.
.

* In version 1.2.11:

	1. New shortcuts/menu items:
		- Copy Zotero select link
		- Copy Zotero URI
	2. New shortcuts:
		- Focus collections, items pane, and various item pane tabs
		- Attachments: recognize PDF, create parent item, and rename from parent

. 

    .
    .
    .

.

.

.

.

.

.

.
.

.
.

.
.
.
Aide à la traduction fournie par Goofy de BabelZilla.