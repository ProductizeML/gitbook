---
description: 'You will learn: recommended methods to curate your data.'
---

# Data Curation

In order to build a robust data pipeline that can evolve over time in terms of volume and data quality, it is crucial to standardize the way this data is managed and label, as well as curate and creating the proper splits before running your entire system.

## Standardization

For the case of supervised learning approaches, it is really important to keep your data well organized so it can be accessed via query systems and extended easily over time. A solution for this standardization process is using a relational database that acts as hierarchical trees of concepts.

An example can be found with the lexical database [WordNet](https://wordnet.princeton.edu/) used in the [ImageNet](http://www.image-net.org/) image database.

![WordNet&apos;s cloud map of concepts.](../.gitbook/assets/screen_shot_2020-07-13_at_10.18.58_pm%20%282%29.png)

![Most popular synsets in current ImageNet using WordNet&apos;s hierarchy.](../.gitbook/assets/screen_shot_2020-07-13_at_10.19.34_pm%20%281%29.png)

Examples in the medical domains include making use of medical ontologies, such as [SNOMED](http://www.snomed.org/) or [ICD](https://icd.who.int/en) in order to organize your medical data into standardized disease codes.

## Versioning control

A really important idea to keep in mind is that datasets evolve over time, data is never fixed when an AI/ML solution is shipped to production. Changes to this dataset can include the addition of new data or modifications of the existing one. Independently to this, you must always checkpoint your data in order to facilitate reproducibility and introduce back up options in your production pipeline.

That being said, a potential solution for this problem is to _version_ your dataset using in order to be able to access to the right data at any point in time through requesting specific states of this.

![DVC tracks ML models and data sets.](../.gitbook/assets/screen_shot_2020-07-17_at_2.33.37_pm%20%281%29.png)

There are some open-source frameworks like [DVC](https://dvc.org/) that provide check-pointing features of not only your dataset but also models trained on the different versions of your data.

{% embed url="https://dvc.org/" %}

## Data Split

In most all Machine Learning scenarios, datasets are split into three buckets with different objectives:

* **Train** set: a group of samples dedicated to training your model.
* **Validation** set: a group of samples dedicated to iterating during your model.
* **Evaluation** set \(or **test** set\): a group of samples dedicated to evaluating your model.

Some considerations when performing the validation and test splits are:

1. They must be **large enough** in order to extract statistically meaningful insights. Usually, the ratios are 75-80% train set and 15-20% validation set. 
2. Share the **same data distribution** and **domain** as the train set. 

## Data Quality

It is crucial to never show any test sample at training time to your model. \(Test\) data leaking is common, especially when your solution includes **data flywheel \(discussed in** [Data Collection](data-collection.md)\). If you are obtaining better than expected results when evaluating your model, it is recommended to set up a retrieval system, e.g. [image retrieval systems](https://paperswithcode.com/task/image-retrieval) using deep learning architectures have shown excellent performance at spotting test samples in training subsets.

