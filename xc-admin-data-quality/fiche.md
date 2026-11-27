# Fiche : xc-admin-data-quality

- Statut : À compléter (captures d'org manquantes, voir plus bas)
- Données : fictives
- Composants data-driven à l'écran : Data Table (colonnes en Display as Input, barre Cancel / Save), List ("Records to fix"), graphiques
- Lieu d'usage : page Lightning (Dynamic Components)

## Pattern enseigné

Corriger la donnée là où on la voit : l'édition dans le tableau évite de passer d'une vue de lecture à un formulaire, et toutes les corrections partent avec un seul Save. Le style d'édition dépend du travail : un crayon (Editable) pour un tableau surtout lu et parfois corrigé, des champs toujours ouverts (Display as Input) pour une saisie sur beaucoup de lignes. Cet écran utilise le second.

## Ce que le lecteur peut appliquer sans cliquer

- Choisir le style d'édition selon le travail : lire et corriger de temps en temps, ou remplir beaucoup de lignes.
- Prévoir l'enregistrement : une modification dans une cellule ne change que l'affichage tant que l'enregistrement n'a pas eu lieu.
- Prévoir le message d'erreur : une règle de validation peut refuser l'enregistrement.

## Sources (lues le 27/11/2026)

- Lightning Design System, Data Entry, section Inline Edit : https://www.lightningdesignsystem.com/2e1ef8501/p/33f0d7-data-entry
  L'édition en ligne permet de modifier une partie d'un record sans passer de la lecture à l'édition, sans perdre le contexte ; un crayon signale le champ modifiable (double clic ou clic sur le crayon).
- Tutoriel Avonni, Enable Inline Editing : https://docs.avonnicomponents.com/dynamic-components/tutorials/components/data-table/enable-inline-editing
  Editable (crayon, tableaux surtout lus) contre Display as Input (saisie sur beaucoup de lignes) ; rien n'atteint Salesforce avant l'interaction Save (Update Record(s)) ; cellules modifiées surlignées et barre Cancel / Save ; Update Record(s) seulement avec une source Query ; les formules sont en lecture seule.
- Lien du premier commentaire : le tutoriel Avonni ci-dessus, avec UTM.

## Piège possible (à valider par Cédric avant de le montrer)

- Sans l'interaction Save de type Update Record(s), les modifications disparaissent au rafraîchissement.
- Si l'enregistrement échoue (règle de validation, champ requis, droit manquant), le même message s'affiche sur chaque ligne modifiée et les valeurs saisies peuvent être perdues : ajouter un Show Toast sous On Error. C'est une limite documentée ; la montrer est honnête mais reste un choix.

## Captures

Faites (recadrées depuis les images existantes) :
- crops/xc-admin-data-quality__crop-display-as-input-table__v1.png : le tableau en Display as Input avec la barre Cancel / Save (830 x 610).
- crops/xc-admin-data-quality__crop-records-to-fix-list__v1.png : la liste "Records to fix" (optionnelle).

À produire dans l'org :
1. Le même tableau avec deux ou trois cellules saisies (surlignées) et la barre Save : l'action en cours.
2. Le même tableau en style Editable (crayons) : mis à côté du Display as Input, c'est l'image qui enseigne le choix.
3. Un état d'erreur après un refus de règle de validation (si Cédric valide le piège).
4. Builder : Data Mappings ouvert sur une colonne avec les réglages Editable et Display as Input visibles.
5. Builder : onglet Interactions, Save avec Update Record(s) et le Show Toast sous On Error.

## À ne pas utiliser

- Le panneau "Fix brief" et "Next best actions" (texte de démo, pas une fonctionnalité).
- Les chiffres de démo (score de 86 %, 130 champs vides, 42 corrigés).
- Les vues Builder actuelles (panneau de la List avec un champ HTML préparé).
