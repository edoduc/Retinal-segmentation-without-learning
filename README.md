# Retinal-segmentation-without-learning
A retinal segmentation model without learning algorithm

This projects aims at developping a model to perform vessel segmentation on retinal images (SLO) without using any learning algorithm, but only basic image processing techniques such as filters and morphological operations.
<Br>The data for this projet come from [IOSTAR](https://www.idiap.ch/software/bob/docs/bob/bob.db.iostar/stable/) dataset.
<Br>The performance criteria are the accuracy, recall, and F1-score between the segmented images and the ground truth ones.

First, we implement a sequence of image processing operations that gives quite good results on one image.
<Br>Then, we use Optuna library in order to optimize the parameters selection over the whole dataset (maximization of mean F1-score).

And we obtain the following results:

Meilleure moyenne de score F1: 0.821
<Br>Paramètres associés:
<Br>  clip_limit: 0.011
<Br>  sigma: 1.233
<Br>  frequency: 0.831
<Br>  seuil: 194.000
<Br>Image star01_OSC.jpg: Meilleur F1 Score: 0.849
<Br>Image star02_OSC.jpg: Meilleur F1 Score: 0.845
<Br>Image star03_OSN.jpg: Meilleur F1 Score: 0.809
<Br>Image star08_OSN.jpg: Meilleur F1 Score: 0.841
<Br>Image star21_OSC.jpg: Meilleur F1 Score: 0.778
<Br>Image star26_ODC.jpg: Meilleur F1 Score: 0.808
<Br>Image star28_ODN.jpg: Meilleur F1 Score: 0.798
<Br>Image star32_ODC.jpg: Meilleur F1 Score: 0.849
<Br>Image star37_ODN.jpg: Meilleur F1 Score: 0.830
<Br>Image star48_OSN.jpg: Meilleur F1 Score: 0.852

Temps total de calcul: 1128.23 secondes
