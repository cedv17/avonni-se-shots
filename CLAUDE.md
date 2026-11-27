# avonni-se-shots : consignes pour Claude Code

Ce dépôt contient de vraies captures d'orgs de démo Salesforce (données fictives). Elles servent aux posts LinkedIn de la page Avonni et du profil de Cédric, et aux démos commerciales. Une tâche hebdomadaire le clone en lecture seule pour proposer un visuel : tout ce qui suit sert à ce qu'elle choisisse bien et ne se trompe pas sur les faits.

## D'où viennent les fichiers

- Le dépôt est publié depuis la banque de captures (son `index.json` est la seule source de vérité) : captures, `scenario.md` et liste du README sont générés depuis l'index. On ne les modifie pas à la main dans le dépôt ; on corrige la banque puis on régénère.
- Les images sont servies par GitHub Pages sur https://shots.avonni.app/<dossier>/<fichier>.

## Dossiers

- Un dossier par scénario, en minuscules avec des tirets : `<préfixe>-<scénario>`.
- Préfixes existants : secteur (`fins-`, `hls-`, `mfg-`, `tmt-`…) ou transverse (`xc-`).
- Préfixes pour les captures SANS Avonni (utiles au profil de Cédric, qui montre surtout du Salesforce natif) :
  - `native-` : un écran construit avec les seuls outils Salesforce (Flow, LWC de base, Dynamic Forms, etc.).
  - `release-` : une nouveauté d'une release Salesforce essayée dans une org (`release-winter27-<fonctionnalité>`).
  - `claudecode-` : un build fait avec Claude Code dans une org, sans composant Avonni.

## Fichiers

- Nom : `<scénario>__<vue>__v<n>.<ext>`. On incrémente `v<n>` au lieu d'écraser une version déjà utilisée.
- Vues : `workspace` (la page remplie), `builder` (la même page dans le builder), `dashboard`, `standard` (la page Salesforce standard), `before-after`, `clip-<action>` ; suffixe `-email` pour le recadrage email (haut de page), suffixe `-fr` pour une version française.
- Captures : PNG, 1280 px de large, sans barre de favoris, sans onglet ni notification personnelle, sans adresse e-mail ni nom réel visible.
- Clips :
  - `clip-<action>.gif` : 5 à 8 secondes, une seule action (amorce, aperçu). Outlook n'affiche que la première image : elle doit se comprendre seule.
  - `clip-<action>.mp4` : 30 à 45 secondes, H.264, 1280 px de large, sans son, le résultat d'abord puis comment on y arrive, plans dans l'ordre. C'est le format visé pour les posts Build.

## Fiche de scénario (obligatoire)

Chaque dossier contient un `scenario.md` :

```
Titre : <ce que fait l'écran, en une phrase>
Pour qui : <rôle de l'utilisateur, par exemple commercial, gestionnaire de sinistres, admin>
Question à laquelle l'écran répond : <la question de l'utilisateur, par exemple « par quel dossier je commence ce matin ? »>
Surface : <page Lightning | Screen Flow | Experience Cloud | LWC | mobile | Agentforce>
Produits : <Avonni Dynamic Components | Avonni Flow Screen Components | Avonni Experience Components | Avonni LWC Components | aucun (natif)>
Composants : <liste exacte, noms tels que dans l'Avonni MCP ou dans Salesforce>
Version : <version du package Avonni, ou release Salesforce>
Date de capture : <AAAA-MM-JJ>
Construit pour une démo prospect : <oui | non>
Usage : <page | profil | les deux>
Montre Avonni : <oui | non>
Notes : <ce qui est réel et ce qui est configuré pour la démo ; limites connues>
```

- `Construit pour une démo prospect : oui` interdit d'utiliser le scénario dans un post qui raconte l'histoire de ce prospect (règle d'anonymat : jamais deux traits ensemble parmi secteur, taille, pays et ce qui a été construit).
- `Usage : page` pour les `before-after` et `standard` : ils ne vont jamais sur le profil de Cédric. Quand un scénario mêle ces vues à d'autres, la fiche les liste dans `Notes` (« Vues réservées à la page »).
- Une fonctionnalité pas encore sortie ne s'affiche que si `Notes` le dit ; aucune capture d'une fonctionnalité non sortie n'est publiée.

## Données fictives

- Les montants et compteurs sont des données de démo : ils ne sont jamais cités comme des résultats.

## Quoi ajouter en priorité

1. Des scénarios qui répondent à une vraie question entendue en appel. La liste est dans la Banque d'angles profil (Notion) : les angles avec `Preuve = Capture` ou `Vidéo possible` et sans capture associée. Écris la question générale dans la fiche, jamais le compte.
2. Des captures `native-`, `release-` et `claudecode-` : elles nourrissent la plupart des posts du profil.
3. Des MP4 de 30 à 45 secondes pour les scénarios Avonni déjà forts (`xc-agentforce-action`, `rev-quote-approval`, `sales-territory-forecast`).

## Commits

- Un commit par scénario ajouté ou modifié, message en anglais : `Add <scénario> (<vues>)` ou `Update <scénario>: <ce qui change>`.
- Mets à jour la liste du README (une ligne par scénario : dossier, titre, montre Avonni oui ou non) : elle est régénérée depuis l'index avec les fiches.
