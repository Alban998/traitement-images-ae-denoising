# Beamer — Autoencodeurs & Débruitage

Projet d'exposé (M1) sur les **autoencodeurs** et le **débruitage d'images** (Denoising Autoencoders), avec :
- une présentation Beamer (`presentation.tex`),
- une démo notebook (TensorFlow/Keras),
- deux documents annexes : notes de présentation et cours détaillé.

## Membres du groupe
- Alban Komla Henovi
- Asta Walo Diop
- Arthur Bomemo Walé

## Structure du projet
- `docs/`
  - `presentation.tex` : slides Beamer
  - `notes_presentateur.tex` : notes orales (script / explications slide-par-slide)
  - `cours_autoencodeurs_debruitage.tex` : cours détaillé (texte structuré)
- `assets/`
  - `figures/` : figures et exports du notebook (utilisés par les slides)
  - `inputs/` : image locale d'entrée (ex. `image1.webp`)
  - `logos/` : logos affichés sur la page de titre
- `notebooks-demo/`
  - `demo_denoising_autoencoder.ipynb` : notebook de démo (MNIST + image locale)

## Compiler la présentation
Depuis le dossier `docs/` :

- PDFLaTeX :
  - `pdflatex -interaction=nonstopmode -halt-on-error presentation.tex`
  - relancer une 2ᵉ fois si besoin (sommaire / liens)

- LaTeXmk (si installé) :
  - `latexmk -pdf -interaction=nonstopmode presentation.tex`

## Générer / mettre à jour les figures (démo)

La diapo **Résultats** utilise (par défaut) :
- `assets/figures/demo_noisy.png`
- `assets/figures/demo_denoised.png`
- `assets/figures/demo_clean.png`

Ces images sont générées par le notebook `notebooks-demo/demo_denoising_autoencoder.ipynb` à partir de `assets/inputs/image1.webp`.

Exports MNIST (séparés, ne remplacent pas les images locales) :
- `assets/figures/demo_mnist_noisy.png`
- `assets/figures/demo_mnist_denoised.png`
- `assets/figures/demo_mnist_clean.png`

Si les fichiers `demo_*.png` n'existent pas, la présentation compile quand même (placeholders).

## Schémas (optionnels)
Le diaporama affiche ces fichiers s'ils existent :
- `assets/figures/autoencoder.png` (schéma AE)
- `assets/figures/autoencoder-denoising.png` (schéma DAE)

## Documents annexes
Depuis `docs/` :
- Notes de présentation : `pdflatex -interaction=nonstopmode -halt-on-error notes_presentateur.tex`
- Cours détaillé : `pdflatex -interaction=nonstopmode -halt-on-error cours_autoencodeurs_debruitage.tex`

## Publication sur GitHub (public) : points d'attention
Avant de rendre le dépôt public, vérifiez :
- que vous avez le **droit de publier** les fichiers dans `assets/logos/` et `assets/inputs/image1.webp` (logos + image source),
- que les figures (schémas / images) proviennent de sources que vous pouvez redistribuer,
- qu'aucune donnée sensible (identifiants, chemins personnels, données confidentielles) n'est incluse.

Pour faciliter une publication publique, le dépôt peut être configuré pour **exclure** (via `.gitignore`) :
- les PDFs générés (`docs/*.pdf`) et les PDFs externes éventuels (`assets/figures/*.pdf`),
- les logos (`assets/logos/*`) et l'image source (`assets/inputs/*`) si vous n'êtes pas sûr des droits.

La présentation est configurée pour rester compilable même si les logos sont absents.
