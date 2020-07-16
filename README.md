# Implementation of BERT-based Exhaustive Neural Named Entity Recognition and Disambiguision (BENNERD) on CORD-19 Dataset

## Backgroud
**I**n response to the coronavirus disease 2019 (COVID-19) pandemic, White House and a coalition of 
research groups have released COVID-19 Open Research Dataset ([CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge)). This dataset further taken into account by data mining group of University of Illinois to create a comprehensive named entity 
annotation ([CORD-NER](https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x)), a distantly supervised dataset that includes 29,500 documents. 

### Corpora Link
- [CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge)
- [CORD-NER](https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x)
 
## BENNERD Description
Our [Knowledge and Information Research Team](https://www.airc.aist.go.jp/en/kirt/) in [AIRC](https://www.airc.aist.go.jp/en/) has implemented a BERT-based exhaustive approach, a scalable and extensible system that implement neural models like named entity recognition (NER) and entity disambiguision (ED) or a.k.a entity linking (EL) by addressing distantly supervise-based [CORD-NER](https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x) data set.

### [BENNERD DEMO](http://prm-ezcatdb.cbrc.jp/bennerd/)
Besides BENNERD, we also release an online text analyze system to meet real-time text annotation with visualization. 
* [http://prm-ezcatdb.cbrc.jp/bennerd/](http://prm-ezcatdb.cbrc.jp/bennerd/)

## Sample Data Format of Extended CORD-NER 
    T1	GENE_OR_GENOME 0 31	Angiotensin-converting enzyme 2
    N1	Reference T1	C0960880
    T2	GENE_OR_GENOME 33 37	ACE2
    N2	Reference T2	C1422064
    T3	CORONAVIRUS 44 54	SARS-CoV-2
    N3	Reference T3	C5203676
    T4	CHEMICAL 55 63	receptor
    N4	Reference T4	C0597357
    T5	CORONAVIRUS 120 130	SARS-CoV-2
    N5	Reference T3	C5203676
    T6	EVOLUTION 158 170	phylogenetic
    N6	Reference T6	cui_less
    T7	WILDLIFE 195 198	bat
    N7	Reference T7	C1412726
    T8	CORONAVIRUS 214 224	SARS-CoV-2
    N8	Reference T3	C5203676
    T9	NORP 259 277	intermediate hosts
    N9	Reference T9	cui_less
    T10	CORONAVIRUS 282 292	SARS-CoV-2
    N10	Reference T3	C5203676


## NER Performances using Different Pre-trained BERT Models

    --------------------------------------------------------------------------------------------------
          Model                   Development-set                              Test-set
                        -------------------------------------    -------------------------------------       
                        Precision(%)   Recall(%)  F1-score(%)    Precision(%)   Recall(%)  F1-score(%)
    ------------------  ------------   ---------  -----------    ------------   ---------  -----------
    ClinicalCovid BERT      84.62        86.43       85.52           82.83        83.23       83.03
    SciBERT                 84.03        87.05       85.51           82.16        83.81       82.98
    Covid BERT Base         78.31        66.80       72.10           77.44        66.80       71.73
    --------------------------------------------------------------------------------------------------
    
    [*] https://github.com/manueltonneau/covid-berts

## Categorical Performances Based on All Categories

We also show the score of NER model trained on ClinicalCovid BERT on all categories in the dataset.

    ----------------------------------------------------------------------------------------------
    Label                     Precision(%)   Recall(%)   F1-score(%)     #TPs      #Preds   #Golds
    ------------------------  ------------   ---------   -----------   ---------  --------  ------
    ANATOMICAL_STRUCTURE         76.62         76.62        76.62        390        509       509
    ARCHAEON                     96.30         96.30        96.30         52         54        54
    BACTERIUM                    79.80         90.51        84.82        391        490       432
    BODY_PART_ORGAN_OR_ORGAN     87.03         84.79        85.90       3517       4041      4148
    _COMPONENT
    BODY_SUBSTANCE               95.56         96.72        96.14       1357       1420      1403
    CARDINAL                     82.36         90.94        86.44      54376      66021     59793
    CELL                         82.24         87.52        84.80      15278      18578     17456
    CELL_COMPONENT               83.03         81.41        82.21       9789      11790     12024
    CELL_FUNCTION                95.33         97.66        96.48       1797       1885      1840
    CELL_OR_MOLECULAR_DYSFUN     98.91         98.91        98.91       2267       2292      2292
    CTION
    CHEMICAL                     83.55         84.60        84.07      94459     113056    111650
    --CORONAVIRUS--              98.46         98.94        98.70      21928      22271     22162
    DAILY_OR_RECREATIONAL_AC     97.20         98.85        98.02       1460       1502      1477
    TIVITY
    DATE                         80.24         83.79        81.98      30231      37675     36080
    DIAGNOSTIC_PROCEDURE         94.72         96.57        95.64        592        625       613
    DISEASE_OR_SYNDROME          84.85         84.99        84.92      30717      36202     36140
    EDUCATIONAL_ACTIVITY         90.91         93.75        92.31         30         33        32
    EUKARYOTE                    89.68         95.04        92.28       5268       5874      5543
    EVENT                        40.79         17.71        24.70         31         76       175
    EVOLUTION                    97.16         98.46        97.80       5301       5456      5384
    EXPERIMENTAL_MODEL_OF_DI     96.05         97.33        96.69        146        152       150
    SEASE
    FAC                          42.75         10.87        17.34         56        131       515
    FOOD                         89.12         93.40        91.21        467        524       500
    GENE_OR_GENOME               76.07         74.83        75.45      71833      94426     95993
    GOVERNMENTAL_OR_REGULATO     65.76         99.18        79.08        121        184       122
    RY_ACTIVITY
    GPE                          78.40         74.71        76.51       7020       8954      9396
    GROUP                        98.48         99.25        98.86      11104      11275     11188
    GROUP_ATTRIBUTE              88.10         100.0        93.67         74         84        74
    HUMAN-CAUSED_PHENOMENON_     95.88         98.94        97.38         93         97        94
    OR_PROCESS
    IMMUNE_RESPONSE              97.29         99.42        98.35       1725       1773      1735
    INDIVIDUAL_BEHAVIOR          84.50         93.09        88.59        229        271       246
    INJURY_OR_POISONING          93.60         95.12        94.35        117        125       123
    LABORATORY_OR_TEST_RESULT    95.63         97.47        96.54        810        847       831
    LABORATORY_PROCEDURE         93.24         95.43        94.32       4030       4322      4223
    LANGUAGE                     78.57         61.11        68.75         22         28        36
    LAW                          43.98         22.51        29.78         95        216       422
    LIVESTOCK                    96.67         97.26        96.96       2091       2163      2150
    LOC                          70.63         43.34        53.72        267        378       616
    MACHINE_ACTIVITY             97.35         96.08        96.71        147        151       153
    MATERIAL                     94.80         90.46        92.58        237        250       262
    MOLECULAR_FUNCTION           96.31         97.91        97.10       4930       5119      5035
    MONEY                        50.97         32.99        40.05        158        310       479
    NORP                         70.48         70.79        70.63       1294       1836      1828
    ORDINAL                      85.55         95.82        90.39       4220       4933      4404
    ORG                          66.33         50.37        57.26       9289      14004     18440
    ORGANISM                     85.80         83.32        84.54       9015      10507     10820
    ORGAN_OR_TISSUE_FUNCTION     89.84         94.01        91.88        345        384       367
    PERCENT                      66.33         42.76        52.00         65         98       152
    PERSON                       56.02         51.16        53.48       4027       7188      7872
    PHYSICAL_SCIENCE             96.80         93.08        94.90        121        125       130
    PRODUCT                      52.60         35.28        42.23        930       1768      2636
    QUANTITY                     71.15         73.38        72.25       3095       4350      4218
    RESEARCH_ACTIVITY            98.63         98.75        98.69       2600       2636      2633
    SIGN_OR_SYMPTOM              95.07         96.39        95.73       1310       1378      1359
    SOCIAL_BEHAVIOR              95.73         98.18        96.94        538        562       548
    SUBSTRATE                    95.99         98.46        97.21       1341       1397      1362
    THERAPEUTIC_OR_PREVENTIV     97.28         98.86        98.06       7551       7762      7638
    E_PROCEDURE
    TIME                         86.67         85.33        86.00       1437       1658      1684
    TISSUE                       78.10         74.66        76.34       4223       5407      5656
    VIRAL_PROTEIN                89.39         91.09        90.23       1053       1178      1156
    VIRUS                        89.18         95.09        92.04       5383       6036      5661
    WILDLIFE                     98.43         97.56        97.99       1438       1461      1474
    WORK_OF_ART                  34.75         14.44        20.40         41        118       284
    ----------------------------------------------------------------------------------------------
  
## Performance Comparison with State-of-the-art Models on [CORD-NER](https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x) Dataset

    ------------------------------------------------------------------------------------------------------
          Model                   Gene                      Chemical                     Disease
                        --------------------------  --------------------------  --------------------------       
                        Prec.(%)   Rec.(%)  F1.(%)  Prec.(%)   Rec.(%)  F1.(%)  Prec.(%)   Rec.(%)  F1.(%)
    ------------------  --------   -------  ------  --------   -------  ------  --------   -------  ------
    SciSpacy*            91.48      82.06    86.51   64.66      39.81    49.28   8.11       2.75     4.11
    (BIONLP13CG)
    ------------------  --------------------------  --------------------------  --------------------------
    SciSpacy*              -          -        -     86.97      51.86    64.69   80.31      59.65    68.46
    (BC5CDR)
    ------------------  --------------------------  --------------------------  --------------------------
    CORD-NER System      82.14      74.68    72.23   82.93      75.22    78.89   75.73      68.42    71.89
    ------------------------------------------------------------------------------------------------------

- *Note: The results of SciSpacy are based on ramdomly picked 1000 sentences from CORD-NER dataset.

## BENNERD Performances based on Indirect comparison with State-of-the-art Models on [CORD-NER](https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x) Dataset
Performance comparison of our model BENNERD on three major biomedical entity types in CORD-19 corpus. Since the manually annotated CORD-NER test set is not publicly available therefore we can not directly compare our system performances. Instead, here we  show  the  performance  of gene, chemical, and disease based on our 5,000 test set.

    ------------------------------------------------------------------------------------------------------
          Model                   Gene                      Chemical                     Disease
                        --------------------------  --------------------------  --------------------------       
                        Prec.(%)   Rec.(%)  F1.(%)  Prec.(%)   Rec.(%)  F1.(%)  Prec.(%)   Rec.(%)  F1.(%)
    ------------------  --------   -------  ------  --------   -------  ------  --------   -------  ------
    BENNERD              76.07      74.8     75.45   83.55      84.60    84.07    84.85     84.9     84.92
    ------------------------------------------------------------------------------------------------------

## Entity Linking With BENNERD System

### Entity Linking Performances on Test Sets.
We are the first to perform entity linking (EL) task on [CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) data set. To judge the EL system performances, we created two test sets: 1. UMLS-based test set 2. Manually annotated test set. 

#### Entity Linking Performances of BENNERD on UMLS-based Test Set.

```
    -------------------------------------------------------------------------------------------
    Model                                            UMLS-based Test Set
                                     ----------------------------------------------------------       
                                        A@1       A@2       A@3       A@4       A@5      A@6(%)
    -----------------------------    --------  --------  --------  --------  --------  --------
    BENNERD + NER's Prediction         27.61     44.56     49.74     51.88     53.08     54.19
    BENNERD + NER's Gold               29.78     48.33     53.89     56.22     57.53     58.74
    BENNERD + NER's True Positive      30.31     48.91     54.60     56.95     58.27     59.49
    -------------------------------------------------------------------------------------------
```

#### Entity Linking Performances of BENNERD on Manually Annotated Test Set.

We show the EL performances on manually annotated test set.

```
    --------------------------------------------------------------------------------
    Model                               Manually Annotated Test Set
                        ------------------------------------------------------------       
                           A@1       A@2       A@3       A@4       A@5      A@6(%)
    ------------------  --------  --------  --------  --------  --------  --------
    BENNERD               24.27     42.95     47.07     48.81     50.00     50.92
    --------------------------------------------------------------------------------
```

## Acknowledgement:

This work is based on results obtained from a project commissioned by the Public/Private R&D Investment Strategic Expansion PrograM (PRISM)



