---
description: 'You will learn: ways of accessing and sources of data.'
---

# Data Access

In all ML scenarios, data plays a crucial role respect the overall solution since it can be seen as the training process' "fuel". In other words, we can have access to a really effective and promising training algorithm, but if we feed inconsistent or impractical data, the outcome will not be as.

In this section, we will describe ways of getting access to data, either via a public access, collection of custom data, and best practices to curate it before passing it to the training algorithm.

![The world&#x2019;s most valuable resource is no longer oil, but data.](../.gitbook/assets/20170506_ldd001_0%20%281%29.jpg)

## Availability and challenges

When searching for a dataset to work with for a product that will be publicly deployed, there are some considerations to take in mind before its deployment.

Firstly, in many ML problems, data can be a **limitation** in terms of **size** and **domain** **representation**. Despite this, we should guarantee to have access to large sets so the model can understand the whole problem as well as representative of the domain we want to become experts at. Note that in some problems these requirements are hard to achieve, especially those for which labeled data can be expensive like in medical fields. As a solution, we will propose data collection workarounds like [labeling tools](data-collection.md#labeling-tools) or generating our [synthetic data](data-collection.md#synthetic-creation) to fight the unbalance of classes.

Secondly, this data needs to be **clean**, **organized, and structured** since most of the ML algorithms that succeed rely on supervised learning methods, and therefore we this data to be properly labeled. We will dive more into about this second challenge and propose solutions to overcome it in [Data Curation](data-curation.md).

Finally, and really importantly, the data that we use in our product should always guarantee **privacy** **consent** from its original sources in order to be regulatory compliant with data protection regulations such as [GDPR](https://gdpr-info.eu/).

## Sources

The best option to guarantee that our dataset fulfills all these previous considerations is to use data marketplaces and dataset searching tools that provide public, structured, and licensed data.

Some well-known options include Google's [Dataset Search](https://datasetsearch.research.google.com/), [Harvard Dataverse](https://dataverse.harvard.edu/), and [Kaggle's Datasets](https://www.kaggle.com/datasets). These repositories provide access in a wide variety of subjects that go from common ML applicable domains such as business, finance, healthcare, earth, and climate sciences, natural language and image processing, to other less common like art, education, law, or social sciences.

![](../.gitbook/assets/screen_shot_2020-07-08_at_5.36.14_pm%20%281%29.png)

Kaggle's Dataset offers access to +40,000 structured and public datasets, and it offers collaborative dataset publication so it can get extended by other users

{% embed url="https://ml-cheatsheet.readthedocs.io/en/latest/datasets.html" %}

## Readings

{% embed url="https://www.economist.com/leaders/2017/05/06/the-worlds-most-valuable-resource-is-no-longer-oil-but-data" %}



