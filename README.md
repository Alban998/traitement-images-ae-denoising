# Exposé — Autoencodeurs et débruitage (DAE)

Exposé (M1) sur les **autoencodeurs** et l’**autoencodeur débruiteur** (Denoising Autoencoder), avec une présentation Beamer, une démo notebook, et deux documents d’accompagnement (notes + cours).

## Membres du groupe
- Alban Komla Henovi
- Asta Walo Diop
- Arthur Bomemo Walé

## Contenu du dépôt
- `docs/`
  - `presentation.tex` : slides Beamer (PDF: `presentation.pdf` une fois compilé)
  - `notes_presentateur.tex` : notes orales (script / explications)
  - `cours_autoencodeurs_debruitage.tex` : cours détaillé
- `notebooks-demo/`
  - `demo_denoising_autoencoder.ipynb` : démo (MNIST + image locale)
- `assets/`
  - `figures/` : figures et exports du notebook (utilisés par les slides)
  - `inputs/` : image locale d’entrée (WEBP)
  - `logos/` : logos

## Compilation (Beamer)
Depuis `docs/` :

```bash
pdflatex -interaction=nonstopmode -halt-on-error presentation.tex
pdflatex -interaction=nonstopmode -halt-on-error presentation.tex
```

## Démo notebook → exports pour les slides
Le notebook exporte les images dans `assets/figures/` :
- image locale : `demo_noisy.png`, `demo_denoised.png`, `demo_clean.png`
- MNIST : `demo_mnist_noisy.png`, `demo_mnist_denoised.png`, `demo_mnist_clean.png`

## Documents annexes
Depuis `docs/` :

```bash
pdflatex -interaction=nonstopmode -halt-on-error notes_presentateur.tex
pdflatex -interaction=nonstopmode -halt-on-error cours_autoencodeurs_debruitage.tex
```

## Licence / droits
Avant publication publique : vérifiez que vous avez le droit de redistribuer `assets/logos/*` et `assets/inputs/image1.webp`.

Par défaut (configuration repo public), ces éléments peuvent être exclus du dépôt via `.gitignore` si vous n'êtes pas certain des droits :
- `assets/logos/*`
- `assets/inputs/*`
- les PDFs générés (`docs/*.pdf`) et tout PDF externe (`assets/figures/*.pdf`)

La présentation reste compilable sans logos (ils sont optionnels) et les figures locales peuvent apparaître en placeholders si les exports correspondants sont absents.

Plus de détails : voir `docs/README.md`.
