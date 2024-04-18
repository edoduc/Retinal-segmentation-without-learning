# Retinal-segmentation-without-learning
A retinal segmentation model without learning algorithm

This projects aims at developping a model to perform vessel segmentation on retinal images (SLO) without using any learning algorithm, but only basic image processing techniques such as filters and morphological operations.
<Br>The data for this projet come from [IOSTAR](https://www.idiap.ch/software/bob/docs/bob/bob.db.iostar/stable/) dataset.
<Br>The performance criteria are the accuracy, recall, and F1-score between the segmented images and the ground truth ones.

First, we implement a sequence of image processing operations that gives quite good results on one image.
<Br>Then, we use Optuna library in order to optimize the parameters selection over the whole dataset (maximization of mean F1-score).

And we obtain the following results:
<Br>Best mean F1-score: 0.821
