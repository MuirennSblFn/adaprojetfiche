# Forge de Personnage — Ashford & Dirman Adventures

Assistant interactif de création de personnage pour la Bible de JDR **Ashford & Dirman Adventures (ADA)**. L'outil fait tenir tout l'assistant de création dans une seule page web autonome : identité et race, caractéristiques (avec lancer automatique ou saisie manuelle des jets physiques), compétences civiles, traits naturels, arbres de combat et de magie, points de vie, or de départ, langues, équipement, et enfin la fiche finale prête à imprimer ou à télécharger.

**Ceci est un outil de fan, non officiel, sans lien avec les auteurs de la Bible.** Il sert uniquement d'aide de jeu personnelle.

## Utiliser l'outil

Aucune installation n'est nécessaire.

- **En ligne** : une fois ce dépôt publié via GitHub Pages (voir plus bas), l'outil est accessible à l'adresse `https://<ton-pseudo-github>.github.io/<nom-du-depot>/`.
- **En local** : télécharge `index.html` et ouvre-le simplement dans un navigateur. Tout le code (HTML, CSS, JavaScript) tient dans ce seul fichier, sans dépendance externe à part les polices Google Fonts (Cinzel et Spectral), chargées via Internet.

Aucune donnée n'est envoyée à un serveur : le personnage en cours de création est conservé uniquement dans le stockage local du navigateur (`localStorage`), pour permettre de reprendre la création plus tard sur le même appareil.

## Fonctionnalités

L'assistant couvre l'intégralité du processus de création décrit dans la Bible : calcul automatique des budgets de compétences civiles à partir des caractéristiques, application des bonus raciaux et de classe (inconditionnels seulement — les bonus contextuels comme « en forêt » restent affichés à titre indicatif), choix des arcanes pour Mage/Ensorceleur et des ordalies pour Prêtre, arbres de compétences de combat et de magie avec points d'arbre et de maîtrise, traits naturels par paires, sélection des langues parlées, et génération d'une fiche finale imprimable — soit directement via le navigateur, soit via un fichier HTML autonome téléchargeable (à ouvrir puis imprimer/enregistrer en PDF depuis son propre navigateur).

## Publier ce dépôt sur GitHub Pages

1. Crée un nouveau dépôt sur GitHub et pousse le contenu de ce dossier dessus (voir les commandes ci-dessous).
2. Dans les paramètres du dépôt (**Settings → Pages**), choisis comme source la branche `main` et le dossier `/ (root)`.
3. GitHub publie alors le site à l'adresse `https://<ton-pseudo-github>.github.io/<nom-du-depot>/` en général en une à deux minutes.

```bash
cd ada-fiche
git init
git add .
git commit -m "Version initiale de la Forge de Personnage"
git branch -M main
git remote add origin https://github.com/<ton-pseudo-github>/<nom-du-depot>.git
git push -u origin main
```

## Structure du dépôt

- `index.html` — l'application complète (HTML, CSS, JavaScript).
- `.nojekyll` — indique à GitHub Pages de servir le site tel quel, sans passer par le moteur de rendu Jekyll (inutile ici mais évite un piège classique des sites statiques).
- `LICENSE` — licence MIT du code.

## Licence

Le code de cet outil est publié sous licence MIT — voir le fichier `LICENSE`. Le contenu du jeu (règles, races, classes, sorts, etc.) appartient à ses auteurs originaux ; ce dépôt ne redistribue que le code de l'assistant, pas le texte intégral de la Bible.
