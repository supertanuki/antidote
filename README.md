# ANTIDOTE — Bataille contre le lobby des pesticides

Jeu de simulation pédagogique sur le lobbying environnemental. En incarnant une chargée de plaidoyer de l'association fictive **ANTIDOTE**, le joueur découvre les mécanismes d'influence politique, la communication publique et la gestion des ressources d'une association face à un lobby industriel puissant.

## Présentation

Une proposition de loi vient d'être déposée au Sénat pour **réautoriser plusieurs pesticides dangereux** aujourd'hui interdits. L'AIPP (Association Industrielle de Protection des Plantes) est déjà à l'œuvre. Le joueur dispose de **8 actions** pour empêcher l'adoption de la loi avant le vote final, en gérant trois indicateurs :

| Indicateur | Valeur de départ |
|---|---|
| 👥 Soutien du public | 40 |
| 🏛️ Influence politique | 60 |
| 💶 Ressources | 100 |

Si l'un des trois indicateurs tombe à zéro, la partie s'arrête immédiatement.

## Démarrage rapide

Le jeu fonctionne entièrement dans le navigateur, sans serveur ni dépendance externe.

```bash
# Cloner le dépôt
git clone <url-du-depot>
cd antidote

# Ouvrir directement dans le navigateur
open index.html
# ou via un serveur local (recommandé pour éviter les restrictions CORS)
npx serve .
```

## Structure du projet

```
antidote/
├── index.html        # Structure de l'interface (écrans, modales)
├── style.css         # Styles (design system, composants, responsive)
├── game.js           # Logique du jeu, navigation, interface messagerie
├── game-data.js      # Données du jeu (phases, stratégies, événements, fins)
├── images/           # Illustrations des actions et logos
└── sfx/              # Effets sonores optionnels
```

### Modifier le contenu du jeu

Tout le contenu narratif et les règles du jeu se trouvent dans `game-data.js` :
- `initialScores` — valeurs de départ des trois indicateurs
- `phases` — les 8 champs d'action disponibles (avec leurs stratégies et effets)
- `events` — événements aléatoires déclenchés par le lobby adverse
- `finalResults` — les 4 issues possibles selon le score final
- `endConditions` — textes des fins prématurées (indicateur à zéro)

## Équipe

| Nom | Rôle |
|---|---|
| Jordan | Lobbying écologiste |
| Céline | Graphiste engagée |
| Richard | Développeur militant |

## Licence

Ce jeu est mis à disposition selon les termes de la [licence Creative Commons Attribution – Pas d'Utilisation Commerciale – Partage dans les Mêmes Conditions 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr).

Vous êtes libre de partager et d'adapter le jeu à condition de citer les auteurs, de ne pas en faire un usage commercial, et de redistribuer sous la même licence.
