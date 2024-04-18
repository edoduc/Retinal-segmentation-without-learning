# Retinal-segmentation-without-learning
A retinal segmentation model without learning algorithm

This projects aims at developping a model to perform vessel segmentation on retinal images (SLO) without using any learning algorithm, but only basic image processing techniques such as filters and morphological operations.
The data for this projet come from [IOSTAR](https://www.idiap.ch/software/bob/docs/bob/bob.db.iostar/stable/) dataset.
The performance criteria are the accuracy, recall, and F1-score between the segmented images and the ground truth ones.

First, we implement a sequence of image processing operations that gives quite good results on one image.
Then, we use Optuna library in order to optimize the parameters selection over the whole dataset (maximization of mean F1-score).

And we obtain the following results:

Meilleure moyenne de score F1: 0.821
Paramètres associés:
  clip_limit: 0.011
  sigma: 1.233
  frequency: 0.831
  seuil: 194.000
Image star01_OSC.jpg: Meilleur F1 Score: 0.849
Image star02_OSC.jpg: Meilleur F1 Score: 0.845
Image star03_OSN.jpg: Meilleur F1 Score: 0.809
Image star08_OSN.jpg: Meilleur F1 Score: 0.841
Image star21_OSC.jpg: Meilleur F1 Score: 0.778
Image star26_ODC.jpg: Meilleur F1 Score: 0.808
Image star28_ODN.jpg: Meilleur F1 Score: 0.798
Image star32_ODC.jpg: Meilleur F1 Score: 0.849
Image star37_ODN.jpg: Meilleur F1 Score: 0.830
Image star48_OSN.jpg: Meilleur F1 Score: 0.852

Temps total de calcul: 1128.23 secondes
