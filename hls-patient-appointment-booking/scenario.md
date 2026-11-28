Titre : Réserve un rendez-vous patient depuis sa fiche : type de soin, créneau de la semaine prochaine, résumé, en trois écrans.
Pour qui : coordinateur de soins
Question à laquelle l'écran répond : « Comment je cale le suivi de cardiologie de ce patient sans quitter sa fiche ? »
Surface : Screen Flow
Produits : Avonni Flow Screen Components, Avonni Dynamic Components
Composants : alert, dateTimePicker, dcActivityTimeline, dcCard, dcContainer, dcDatatable, dcLayout, dcList, dcMetric, dcRelationshipGraph, dcRepeatable, dcTabbedContainer, dcText, inputChoiceSet, textArea, visualPicker, Highlights Panel, Lightning record page, Quick Action (Flow), Related List - Single, Screen Flow
Version : Avonni Flow Screen Components 6.35.0.2 (avcmpbuilder), Avonni Dynamic Components 1.29.0.3 (avxp)
Date de capture : 2026-11-27
Construit pour une démo prospect : non
Usage : les deux
Montre Avonni : oui
Notes : Données fictives (personnes, entreprises, montants, compteurs) : jamais citées comme des résultats. Org de démo jetable (scratch org) construite pour la banque de captures, pas pour un prospect. Clips : clip-book-appointment (7.8 s); clip-book-appointment-story (40.4 s). Outlook n'affiche que la première image d'un GIF. Vues de page d'enregistrement (record, record-after) : la fiche Salesforce avec son en-tête standard, ses onglets et listes associées, et le composant Avonni lié à la fiche. Vrai Screen Flow lancé par une action rapide de la fiche patient, qui crée un vrai rendez-vous (Care_Appointment__c). Les créneaux pris sont fixés pour la démo (relatifs au lundi suivant) ; le week-end et le jour même sont fermés. Le bandeau des dates (plage de la semaine) du sélecteur de créneaux est masqué à la capture (règle : pas de date absolue) ; les en-têtes de jour gardent le numéro du jour. Limites connues : le sélecteur affiche les heures avec les secondes (8:00:00 AM) quel que soit le format choisi, et ouvre d'abord la semaine en cours ; le composant de la fiche ne se rafraîchit pas à la fin du flow, la fiche est rechargée dans le clip.

Fichiers : hls-patient-appointment-booking__clip-book-appointment__v1.gif, hls-patient-appointment-booking__clip-book-appointment-story__v1.mp4, hls-patient-appointment-booking__flow-step-1__v1.png, hls-patient-appointment-booking__flow-step-2__v1.png, hls-patient-appointment-booking__flow-step-3__v1.png, hls-patient-appointment-booking__record__v1.png, hls-patient-appointment-booking__record-after__v1.png
