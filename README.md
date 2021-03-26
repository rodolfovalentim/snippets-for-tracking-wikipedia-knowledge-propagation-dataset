# Tracking Knowledge Propagation Across Wikipedia Languages Dataset

We present a dataset of inter-language knowledge propagation in Wikipedia. The dataset includes the data from 2001 to the first trimester of 2020. Covering the entire 309 language editions and 33M articles, the dataset aims to track the full propagation history of Wikipedia concepts, and allow follow up research on building predictive models of them. For this purpose, we align all the Wikipedia articles in a language-agnostic manner according to the concept they cover, which results in 13M propagation instances. To the best of our knowledge, this dataset is the first to explore the full inter-language propagation at a large scale.

## Dataset format

The dataset is stored in csv format, with the followings columns:

* Wikidata ID: The Wikidata item id (ex [Q298](https://www.wikidata.org/wiki/Q298)). 
* Language Edition: The list of languages editions containig an article related to the Wikidata ID. The  full  list  of  the  mapping  between  the  code  and  the  lan-guage can be found [here](https://meta.wikimedia.org/wiki/TableofWikimediaprojects) (ex: [enwiki](https://en.wikipedia.org/wiki/Chile),[eswiki](https://es.wikipedia.org/wiki/Chile),[ptwiki](https://pr.wikipedia.org/wiki/Chile)) ,
* Creation Timestamp: The creation timestamp for each language edition.
* Topics: The list of topics that the item belongs to (ex: Geography.Geographical, Geography.Regions.Americas.South_America), based on this [taxonomy](https://wiki-topic.toolforge.org/). 

The dataset can be downloaded from [here](https://doi.org/10.5281/zenodo.4433137).

## Examples

You read the data directly from zenodo: 

```
import pandas as pd 
wikipedia_df = pd.read_csv('https://zenodo.org/record/4433137/files/dataset.csv.zip', sep=',')
```
For more details please check [this notebook](https://github.com/rodolfovalentim/wikipedia-content-propagation/blob/main/snippets.ipynb).

## Citation
```
@inproceedings{valetim2020Wikipedia,
  title={Tracking Knowledge Propagation Across Wikipedia Languages},
  author={Valentim, Rodolfo and Comarela, Giovanni and Park, Souneil and Saez-Trumper, Diego},
  booktitle={Proceedings of the International AAAI Conference on Web and Social Media},
  year={2021}
}
```






