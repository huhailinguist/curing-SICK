# curing-SICK

This repo contains the data presented in the paper *Curing the SICK and other NLI maladies*.

## re-annotated SICK

`SICK-cured.csv` is our fully re-annotated [SICK](https://marcobaroni.org/composes/sick.html) dataset, where:

- Origin: either the data point is from SICK or in semeval
- Logic_label: the logic label for the NLI pair, either aggregated from the symbolic systems, or aggregated from the 3 human expert annotators
- Commonsense_label: the commensense label for the NLI pair, either aggregated from the symbolic systems, or aggregated from the 3 human expert annotators
- SICK_original_label: original label from SICK
- [monalog](https://github.com/huhailinguist/monalog): label assigned by the MonaLog system (Hu et al 2020)
- [gkr4nli](https://github.com/kkalouli/GKR4NLI): label assigned by the GKR4NLI system (Kalouli et al 2020; Kalouli 2021)	
- [langpro](https://github.com/kovvalsky/LangPro): label assigned by the LangPro system (Abzianidze 2017)
- [ccg2lambda_easyccg](https://github.com/mynlp/ccg2lambda): label assigned by the ccg2lambda system with the EasyCCG parser (Yanaka et al 2018)
- [ccg2lambda_candc](https://github.com/mynlp/ccg2lambda): label assigned by the ccg2lambda system with the CandC parser (Yanaka et al 2018)

To be more specific, 3,138 pairs (31.6% of the entire corpus) have been reannotated by us, each pair by 3 expert annotators. See section 3 of the paper for details. 

## crowd-annotation of 100 MNLI examples from chaosNLI using our annotation scheme

`results100.xlsx` contains annotations from crowd workers on MTurk. 
They were asked to give two labels for each pair, one as a judge in court (being strict), another as a person on the street.

- from chaosNLI: three columns showing the number of annotators giving the Entail, Neutral or Contradiction label, taken from the chaosNLI dataset (Nie et al 2020)
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
  author    = {Aikaterini-Lida Kalouli* and
               Hai Hu* and
               Alexander F. Webb and
               Lawrence S. Moss and
               Valeria de Paiva},
  title     = {Curing the SICK and other NLI maladies},
  journal   = {Computational Linguistics},
  year      = {2023},
}
```

## Citations for the resources used in the paper

The original SICK corpus:
```
@inproceedings{marelli2014,
title = "A {SICK} cure for the evaluation of compositional distributional semantic models",
author = "Marelli, Marco  and
Menini, Stefano  and
Baroni, Marco  and
Bentivogli, Luisa  and
Bernardi, Raffaella  and
Zamparelli, Roberto",
booktitle = "Proceedings of the Ninth International Conference on Language Resources and Evaluation ({LREC}'14)",
month = may,
year = "2014",
address = "Reykjavik, Iceland",
publisher = "European Language Resources Association (ELRA)",
url = "http://www.lrec-conf.org/proceedings/lrec2014/pdf/363_Paper.pdf",
pages = "216--223",
abstract = "Shared and internationally recognized benchmarks are fundamental for the development of any computational system. We aim to help the research community working on compositional distributional semantic models (CDSMs) by providing SICK (Sentences Involving Compositional Knowldedge), a large size English benchmark tailored for them. SICK consists of about 10,000 English sentence pairs that include many examples of the lexical, syntactic and semantic phenomena that CDSMs are expected to account for, but do not require dealing with other aspects of existing sentential data sets (idiomatic multiword expressions, named entities, telegraphic language) that are not within the scope of CDSMs. By means of crowdsourcing techniques, each pair was annotated for two crucial semantic tasks: relatedness in meaning (with a 5-point rating scale as gold score) and entailment relation between the two elements (with three possible gold labels: entailment, contradiction, and neutral). The SICK data set was used in SemEval-2014 Task 1, and it freely available for research purposes.",
}
```

The chaosNLI corpus:

```
@inproceedings{nie2020chaosnli,
  title={What Can We Learn from Collective Human Opinions on Natural Language Inference Data?},
  author={Nie, Yixin and Zhou, Xiang and Bansal, Mohit},
  booktitle={Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)},
  pages={9131--9143},
  year={2020}
}
```

The MNLI corpus
```
@inproceedings{williams2018mnli,
  title={A Broad-Coverage Challenge Corpus for Sentence Understanding through Inference},
  author={Williams, Adina and Nangia, Nikita and Bowman, Samuel},
  booktitle={Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers)},
  pages={1112--1122},
  year={2018}
}
```
ccg2lambda system:
```
@inproceedings{YanakaMMB18, 
  author    = {Hitomi Yanaka and
               Koji Mineshima and
               Pascual Mart{\'{\i}}nez{-}G{\'{o}}mez and
               Daisuke Bekki},
  title     = {{A}cquisition of {P}hrase {C}orrespondences Using {N}atural {D}eduction {P}roofs},
  booktitle = {Proceedings of NAACL}, 
  year      = {2018},
  pages={756--766},
  url={https://www.aclweb.org/anthology/N18-1069/}
}
```

LangPro system:
```
@inproceedings{AbzianidzeLangPro,
    title = "{L}ang{P}ro: Natural Language Theorem Prover",
    author = "Abzianidze, Lasha",
    booktitle = "Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing: System Demonstrations",
    month = sep,
    year = "2017",
    address = "Copenhagen, Denmark",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/D17-2020",
    doi = "10.18653/v1/D17-2020",
    pages = "115--120",
}
```

GKR4NLI:
```
@inproceedings{kalouli2020b, 
	author = {Aikaterini-Lida Kalouli and Richard Crouch and Valeria de Paiva },
	title = {Hy-NLI: a Hybrid system for Natural Language Inference},
	booktitle = {Proceedings of the 28th International Conference on Computational Linguistics},
	series = {COLING '20},
	year = {2020},
    pages={5235–5249},
	location = {Barcelona, Spain},
	publisher = {Association for Computational Linguistics}
} 



@phdthesis{Kalouli2021diss, 
  title={Hy-NLI : a Hybrid system for state-of-the-art Natural Language Inference},
  year={2021},
  author={Kalouli, Aikaterini-Lida},
  address={Konstanz},
  school={Universität Konstanz}
}
```

MonaLog
```
@inproceedings{monalog,
	title={{MonaLog: a Lightweight System for Natural Language Inference Based on Monotonicity}},
	author={Hu, Hai and Chen, Qi and Richardson, Kyle and Mukherjee, Atreyee and Moss, Lawrence S and Kuebler, Sandra},
	booktitle={Proceedings of SCiL},
	year={2020},
    pages={334--344},
	url={https://arxiv.org/abs/1910.08772}
}
```



