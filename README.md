# NumWorks – Simulateur (pack local modifié)

Ce dépôt contient une copie locale d’une page HTML du simulateur NumWorks que j’ai téléchargée pour mes cours, à laquelle j’ai apporté de petites améliorations d’affichage (notamment un mode sombre, un bouton de bascule, et un comportement plein écran). Le simulateur et le logiciel de la calculatrice (Epsilon) restent l’œuvre et la propriété de NumWorks.

- Simulateur officiel et téléchargements : https://www.numworks.com/simulator/download
- Projet Epsilon (open-source) : https://github.com/numworks/epsilon

Avertissement important: je ne suis pas l’auteur du simulateur ni du système Epsilon. Je n’ai fait que télécharger le simulateur et le modifier légèrement pour améliorer le confort d’utilisation (mode sombre, etc.). Respectez la licence et les marques de NumWorks; référez‑vous aux pages officielles pour les conditions d’utilisation.

## Contenu

- `numworks-simulator-24.3.0.html` – Page HTML autonome du simulateur NumWorks.
- `README.md` – Ce fichier d’explication.

## Comment l’utiliser

Prérequis:
- Un navigateur moderne (Chrome, Edge, Firefox, Safari récents).

Lancement:
- Ouvrez directement le fichier `numworks-simulator-24.3.0.html` dans votre navigateur (double‑clic ou glisser‑déposer dans une fenêtre de navigateur). Aucune installation ni serveur n’est requis.

Commandes visibles:
- Bouton « Mode sombre » (ajouté) – Bascule entre mode clair et sombre. La préférence est mémorisée localement dans le navigateur.
- Bouton « Plein écran » – Affiche le simulateur en mode plein écran de la page.
- Bouton « Capture » – Réalise une capture d’écran du simulateur.

Interactions:
- Souris: cliquez sur l’écran ou les touches affichées sur l’image de la calculatrice.
- Clavier: vous pouvez utiliser votre clavier d’ordinateur pour saisir des chiffres, valider (Entrée), effacer (Retour arrière), naviguer (flèches), etc. Les correspondances exactes dépendent du simulateur NumWorks.

Fonctionnement interne (vue d’ensemble):
- La page charge Epsilon (le système de la calculatrice) compilé en WebAssembly. L’affichage et les touches sont rendus sur un canvas HTML. Les boutons « Plein écran » et « Capture » pilotent des fonctions déjà fournies par le simulateur. Mes modifications n’altèrent pas le cœur du simulateur; elles ajustent l’interface et l’apparence côté page web.

## Modifications apportées (qualité de vie)

- Mode sombre global avec contraste élevé: ajout d’un bouton « Mode sombre »; mémorisation de la préférence; respect de la préférence système (si aucune préférence n’a été enregistrée). Le fond de la page et les éléments d’interface s’adaptent.
- Écran de la calculatrice en sombre: un filtre d’affichage est appliqué au canvas pour inverser les couleurs et augmenter le contraste afin d’obtenir un texte clair sur fond sombre (confort visuel). Ce filtre n’altère pas le simulateur lui‑même, uniquement son rendu sur la page.
- Plein écran: simplification du basculement pour conserver les classes CSS (compatibilité avec le mode sombre).
- Icônes/contrôles: teinte des icônes adaptée au thème, survols cohérents en clair/sombre.

Notes:
- Les captures « Télécharger l’image » ne tiennent généralement pas compte des filtres CSS du canvas: la capture peut apparaître en couleurs « d’origine ». C’est un comportement normal des navigateurs (export des pixels réels du canvas). Si vous souhaitez exporter une capture « sombre », il faudrait ajouter une étape de post‑traitement spécifique.
- La copie vers le presse‑papiers (si disponible) peut nécessiter un contexte sécurisé (HTTPS) selon le navigateur. En local, l’option de téléchargement reste la plus fiable.

## Conseils d’utilisation

- Zoom navigateur: utilisez `Ctrl` + `+` / `Ctrl` + `-` (ou `Cmd` sur Mac) pour ajuster la taille si nécessaire.
- Accessibilité: activez le mode sombre pour réduire la fatigue visuelle dans des environnements peu lumineux.
- Hors‑ligne: le fichier fonctionne sans connexion. Un script de vérification de mise à jour peut tenter un accès réseau, mais le simulateur reste fonctionnel hors‑ligne.

## Crédits et mentions

- « NumWorks » et « Epsilon » sont des marques/logiciels de NumWorks. 
- Simulateur et firmware de calculatrice: © NumWorks. Voir les conditions et licences sur leurs sites officiels.
- Ce dépôt n’est ni affilié, ni soutenu par NumWorks. Il s’agit d’une utilisation personnelle à des fins éducatives, avec de légers ajustements d’interface.

## Problèmes connus / Support

- Si l’interface ne réagit pas, rechargez la page.
- Si la capture ne s’enregistre pas: vérifiez les permissions du navigateur ou utilisez l’option de téléchargement.
- Pour des questions techniques sur le simulateur lui‑même, consultez la documentation NumWorks et le dépôt Epsilon.

