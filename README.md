# Dermatology

* [The Original Data](#the-original-data)
* [Augmentations](#augmentations)
* [Copyright and Attribution](#copyright-and-attribution)

<br>
<br>

This is a image data repository.  It complements the

* [augmentation](https://github.com/greyhypotheses/augmentation)
* [derma](https://github.com/greyhypotheses/derma)

repositories.  The [augmentation repository](https://github.com/greyhypotheses/augmentation) augments the images of this repository, whilst the [derma repository](https://github.com/greyhypotheses/derma) is a repository of models that use the augmentations.

<br>

## The Original Data

The data is courtesy of the International Skin Imaging Collaboration (ISIC).  It is a set of dermoscopic images of skin lesions: specifically, the images of the [ISIC 2019 Challenge](https://challenge2019.isic-archive.com/), i.e.,

<br>

|file| description|size|
|:---|:---|:---|
|[ISIC_2019_Training_Input.zip](https://s3.amazonaws.com/isic-challenge-2019/ISIC_2019_Training_Input.zip)|25,331 JPEG images of skin lesions|~9GB|
|[ISIC_2019_Training_Metadata.csv](https://s3.amazonaws.com/isic-challenge-2019/ISIC_2019_Training_Metadata.csv)|25,331 metadata entries of age, sex, general anatomic site, and common lesion identifier|1.15MB|
|[ISIC_2019_Training_GroundTruth.csv](https://s3.amazonaws.com/isic-challenge-2019/ISIC_2019_Training_GroundTruth.csv)|25,331 entries of gold standard lesion diagnoses|1.23MB|

<br>

The images are either the same as those hosted by the [ISIC Archive API](https://www.isic-archive.com/#!/topWithHeader/onlyHeaderTop/apiDocumentation) or  down-sampled versions.  The data set outlined below might be used if the ground truths are released.

* [ISIC_2019_Test_Input.zip](https://s3.amazonaws.com/isic-challenge-2019/ISIC_2019_Test_Input.zip): 8,238 JPEG images of skin lesions
* [ISIC_2019_Test_Metadata.csv](https://s3.amazonaws.com/isic-challenge-2019/ISIC_2019_Test_Metadata.csv): 8,238 metadata entries of age, sex, and general anatomic site

<br>

To ensure availability, the contents of ISIC_2019_Training_Input.zip are in the directory [data/images/](./data/images/), whilst copies of the ISIC_2019_Training_Metadata.csv & ISIC_2019_Training_GroundTruth.csv files are stored in [data](./data/).  


<br>
<br>


## Augmentations

Augmented versions of the images in ISIC_2019_Training_Input.zip are created via the [augmentation package](https://github.com/greyhypotheses/augmentation).  The package

* ensures that all images are of the same size; the size is determined by the models
* creates rotated forms of most images

The augmentations are stored in [augmentations/images/](./augmentation/images).  The images are zipped, and heir metadata is summarised in [augmentations/inventory.csv](./augmentations/inventory.csv)

<br>
<br>


## Copyright and Attribution

`Details: https://challenge2019.isic-archive.com/data.html`

The images and metadata of the "ISIC 2019: Training" data used herein are licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/) (CC-BY-NC).  The copyright holders are:

* BCN_20000 Dataset: &copy; Department of Dermatology, Hospital Clínic de Barcelona, https://arxiv.org/abs/1908.02288 <sup>4</sup>
* HAM10000 Dataset: &copy; ViDIR Group, Department of Dermatology, Medical University of Vienna, https://www.nature.com/articles/sdata2018161 <sup>1</sup>
* MSK Dataset: &copy; Anonymous; https://arxiv.org/abs/1710.05006, https://arxiv.org/abs/1902.03368 <sup>2, 3</sup>

<br>

References

1. P. Tschandl, C. Rosendahl, H. Kittler: [The HAM10000 dataset, a large collection of multi-source dermatoscopic images of common pigmented skin lesions](https://www.nature.com/articles/sdata2018161),  Scietific Data, Volume 5, Article Number: 180161, 2018, doi:10.1038/sdata.2018.161
2. Noel C. F. Codella, David Gutman, M. Emre Celebi, Brian Helba, Michael A. Marchetti, Stephen W. Dusza, Aadi Kalloo, Konstantinos Liopyris, Nabin Mishra, Harald Kittler, Allan Halpern: [Skin Lesion Analysis Toward Melanoma Detection: A Challenge at the 2017 International Symposium on Biomedical Imaging (ISBI), Hosted by the International Skin Imaging Collaboration (ISIC)](https://arxiv.org/pdf/1710.05006.pdf), 2018, arXiv:1710.05006
3. Noel Codella, Veronica Rotemberg, Philipp Tschandl, M. Emre Celebi, Stephen Dusza, David Gutman, Brian Helba, Aadi Kalloo, Konstantinos Liopyris, Michael A. Marchetti, Harald Kittler, Allan Halpern: [Skin Lesion Analysis Toward Melanoma Detection 2018: A Challenge Hosted by the International Skin Imaging Collaboration (ISIC)](https://arxiv.org/abs/1902.03368), 2019, arXiv:1902.03368
4. Marc Combalia, Noel C. F. Codella, Veronica Rotemberg, Brian Helba, Veronica Vilaplana, Ofer Reiter, Cristina Carrera, Alicia Barreiro, Allan C. Halpern, Susana Puig, Josep Malvehy: [BCN20000: Dermoscopic Lesions in the Wild](https://arxiv.org/pdf/1908.02288.pdf), 2019, arXiv:1908.02288
