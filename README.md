# curing-SICK

This repo contains the data presented in the paper *Curing the SICK and other NLI maladies*.

## re-annotated SICK

`SICK-cured.csv` is our fully re-annotated SICK dataset, where:

- Origin: either the data point is from SICK or in semeval
- Logic_label: the logic label for the NLI pair, either aggregated from the symbolic systems, or aggregated from the 3 human expert annotators
- Commonsense_label: the commensense label for the NLI pair, either aggregated from the symbolic systems, or aggregated from the 3 human expert annotators
- SICK_original_label: original label from SICK
- monalog: label assigned by the MonaLog system (Hu et al 2020)
- gkr4nli: label assigned by the GKR4NLI system (Kalouli et al 2020; Kalouli 2021)	
- langpro: label assigned by the LangPro system (Abzianidze 2017)
- ccg2lambda_easyccg: label assigned by the ccg2lamdbda system with teh EasyCCG parser (Yanaka et al 2018)
- ccg2lambda_candc: label assigned by the ccg2lamdbda system with teh CandC parser (Yanaka et al 2018)

To be more specific, 3,138 pairs (31.6% of the entire corpus) have been reannotated by us, each pair by 3 expert annotators. See section 3 of the paper for details. 

## crowd-annotation of 100 MNLI examples from chaosNLI using our annotation scheme

`results100.xlsx` contains annotations from crowd workers on MTurk. 
They were asked to give two labels for each pair, one as a judge in court (being strict), another as a person on the street.

- from chaosNLI: three columns showing the number of annotators giving the Entail, Neutral or Contradiction label
- ours-as judge: the number of crowd workers annotating a certain label as a judge, 10 workers have worked on a pair, but some were removed because they answered the catch trial wrong
- ours-as person on the street: the number of crowd workers annotating a certain label as a person on the street
- ours majority-as judge: majority label
- ours majority-as person on the street: majority label
- diff: whether the above two labels were the same
- HITid: these 100 pairs were distributed in five HITs, each with 20 pairs


## Citation

The paper is accepted to Computational Linguistics. 

```
@article{kalouliEtAl2023, 
  author    = {Aikaterini-Lida Kalouli and
               Hai Hu and
               Alexander F. Webb and
               Lawrence S. Moss and
               Valeria de Paiva},
  title     = {Curing the SICK and other NLI maladies},
  journal   = {Computational Linguistics},
  year      = {2023},
}
```


