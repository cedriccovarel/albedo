# Calculateur d'albédo moyen — Méthode Berlin

Application web autonome pour calculer l'albédo moyen pondéré d'un projet architectural selon la méthode de Berlin (*Leitfaden Stadtklima*, SenStadtWohn).

## Fonctionnalités

- Informations projet éditables : nom du projet, référence, maître d'ouvrage, rédacteur et date.
- Ajout dynamique de surfaces : toiture, façade ou sol extérieur.
- Sélection de matériaux avec coefficients α intégrés.
- Calcul de l'albédo moyen pondéré :

```text
Albédo moyen = Σ(αᵢ × Sᵢ) / Σ(Sᵢ)
```

- Fenêtre de vérification avant calcul avec rappel des surfaces à inclure ou exclure.
- Résultat avec jauge visuelle, interprétation automatique et statistiques.
- Détail par surface avec contribution relative.
- Export PDF via la fonction d'impression du navigateur.
- Table de référence repliable des coefficients α.
- Interface responsive, en fichier HTML unique.

## Utilisation locale

Ouvrir simplement le fichier `index.html` dans un navigateur récent.

Aucune installation n'est nécessaire.

## Déploiement sur GitHub Pages

1. Créer un nouveau dépôt GitHub.
2. Envoyer les fichiers de ce dossier dans le dépôt.
3. Aller dans **Settings** → **Pages**.
4. Dans **Build and deployment**, sélectionner :
   - Source : **Deploy from a branch**
   - Branch : **main**
   - Folder : **/root**
5. Cliquer sur **Save**.

L'application sera disponible à l'adresse indiquée par GitHub Pages après quelques instants.

## Structure

```text
.
├── index.html
├── README.md
├── LICENSE
└── .gitignore
```

## Référence

Méthode Berlin — *Leitfaden Stadtklima*, SenStadtWohn.

## Licence

MIT — voir le fichier `LICENSE`.

## Note méthodologique sur les vitrages

Les surfaces vitrées extérieures sont intégrées au calcul lorsqu’elles participent à l’enveloppe exposée du bâtiment : vitrages en façade, murs rideaux, verrières, sheds ou garde-corps vitrés significatifs. Les vitrages intérieurs, durablement masqués ou protégés peuvent être exclus ou traités à part selon le périmètre retenu. Les vitrages très réfléchissants doivent être signalés en raison du risque d’éblouissement.
