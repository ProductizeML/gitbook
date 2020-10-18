---
description: 'You will learn: ways of collecting data.'
---

# Data Collection

Yet working with a public dataset can be difficult to ensure business advantage as a unique asset from potential competitors, so in order to differentiate from others' approaches, someone may consider building our own dataset via user's data collection and labeling, what is known as **data flywheel**, or even generating synthetic data from existing datasets.

![Data collection is defined as the first need in the Data Science hierarchy of needs by Monica Rogati.](../.gitbook/assets/1_7imev5xslc9flxr9hhhpfw%20%281%29.png)

## Labeling tools

Datasets can sometimes contain errors on the labels or even lack of them. An example can be when gathering data from your users, this data is pretty valuable since it belongs to the domain you want to solve but you will only have access to the ML models predictions. Obviously this is not enough, and you might want to properly label the samples by human labelers experts on that task.

To address this problem, a marketplace has appeared for data labeling services like image classification, object detection in images, object segmentation, video frame tagging, object tracking in videos, or text classification. In some tasks, the costs associated with the knowledge required to complete the labeling process successfully is quite expensive, and in those cases, a hybrid method between human and ML-based labeling solution can reduce the task's cost.

Some existing **collecting and** **labeling tools** include:

{% embed url="https://www.mturk.com/" %}

{% embed url="https://scale.com/" %}

{% embed url="https://www.snorkel.ai/" %}

{% embed url="https://appen.com/" %}

{% embed url="https://cloud.google.com/ai-platform" %}

## Synthetic creation

Labeling your own data might require time, logistics, and economical costs. A useful way to keep extending your datasets to train other ML algorithms is by generating realistic data samples by other ML approaches such as Generative Adversarial Networks \(GAN\).

Some of the benefits of synthetic data are:

1. **Anonymized data**: usage constraints due to privacy rules or other regulations.
2. **Class unbalancing**: it can mitigate problems by generating more samples of the underrepresented classes.  
3. **Not yet encountered cases**

{% embed url="https://towardsdatascience.com/synthetic-data-generation-a-must-have-skill-for-new-data-scientists-915896c0c1ae" %}

## Readings

* [The Data Flywheel: Building momentum by putting your data to work](https://techcloudlink.com/wp-content/uploads/2019/10/The-Data-Flywheel-Building-momentum-by-putting-your-data-to-work.pdf)

{% embed url="https://hackernoon.com/the-ai-hierarchy-of-needs-18f111fcc007" %}

