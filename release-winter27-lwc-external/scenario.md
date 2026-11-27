Titre : Une page Lightning qui affiche des durées relatives avec time-elements, un web component open source, rendu nativement grâce à lwc:external (GA en Winter '27).
Pour qui : développeur Salesforce
Question à laquelle l'écran répond : « Est-ce que je peux réutiliser une bibliothèque de web components existante dans un LWC, sans iframe ? »
Surface : LWC (page Lightning)
Produits : aucun (natif)
Composants : @salesforce/resourceUrl, lightning-card, lightning-progress-bar, lightning/platformResourceLoader loadScript, lwc:external, time-ago (@github/time-elements), time-until (@github/time-elements)
Version : Winter '27
Date de capture : 2026-11-27
Construit pour une démo prospect : non
Usage : les deux
Montre Avonni : non
Notes : Données fictives (personnes, entreprises, montants, compteurs) : jamais citées comme des résultats. Org de démo jetable (scratch org) construite pour la banque de captures, pas pour un prospect. Fonctionnalité sortie (GA en Winter '27, API 68.0), vérifiée dans la doc officielle et le guide développeur Winter '27. Bibliothèque : @github/time-elements 3.1.0 (licence MIT), build UMD officiel du paquet npm, chargé tel quel en ressource statique avec loadScript ; Lightning Web Security activé. Seules les vues relatives (time-ago, time-until) sont utilisées. Essai écarté : @lottiefiles/lottie-player 2.0.12 (UMD) se charge mais n'anime pas sous LWS (IntersectionObserver refuse l'élément).

Fichiers : release-winter27-lwc-external__code__v1.png, release-winter27-lwc-external__workspace__v1.png
