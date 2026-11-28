Titre : Déclare un sinistre habitation depuis la fiche de la police, en trois étapes guidées, et crée le dossier de sinistre rattaché à la police.
Pour qui : gestionnaire de déclarations de sinistres (assurance habitation)
Question à laquelle l'écran répond : « Comment enregistrer une déclaration complète, avec une estimation des dégâts, sans quitter la fiche de la police ? »
Surface : Screen Flow (lancé depuis une page d'enregistrement Lightning)
Produits : Avonni Flow Screen Components
Composants : alert, dcCard, dcDatatable, dcMap, dcMetric, formattedValue, header, inputChoiceSet, metric, progressIndicator, slider, textArea, visualPicker, Create Records, Get Records, Highlights Panel, Lightning record page, Quick Action (Flow), Record Detail, Related List - Single, Screen Flow, Tabs
Version : Avonni Flow Screen Components 6.35.0.2 (avcmpbuilder)
Date de capture : 2026-11-27
Construit pour une démo prospect : non
Usage : les deux
Montre Avonni : oui
Notes : Données fictives (personnes, entreprises, montants, compteurs) : jamais citées comme des résultats. Org de démo jetable (scratch org) construite pour la banque de captures, pas pour un prospect. Clips : clip-report-claim (7.4 s); clip-report-claim-story (37.4 s). Outlook n'affiche que la première image d'un GIF. Vues de page d'enregistrement (record, record-after) : la fiche Salesforce avec son en-tête standard, ses onglets et listes associées, et le composant Avonni lié à la fiche. Page d'enregistrement Salesforce standard (panneau de synthèse, onglets, listes associées) avec une action rapide Report a Claim qui lance le Screen Flow. Étape 1 : tuiles de type de sinistre et date relative ; étape 2 : éléments endommagés, curseur d'estimation avec valeur en direct, logement habitable ; étape 3 : récapitulatif et gravité calculée. Le flow crée le sinistre et un événement. Après la fermeture du flow, la liste associée standard se met à jour, mais le composant dynamique Avonni de la page n'est rafraîchi qu'au rechargement (le clip montre un rechargement). Données fictives.

Fichiers : fins-insurance-fnol-intake__clip-report-claim__v1.gif, fins-insurance-fnol-intake__clip-report-claim-story__v1.mp4, fins-insurance-fnol-intake__flow-step-1__v1.png, fins-insurance-fnol-intake__flow-step-2__v1.png, fins-insurance-fnol-intake__record__v1.png, fins-insurance-fnol-intake__record-after__v1.png
