# Named Entity Recognition

Pretrained BERT model: `clinicalcovid-bert-base-cased`

Download link: [https://huggingface.co/manueltonneau/clinicalcovid-bert-base-cased](https://huggingface.co/manueltonneau/clinicalcovid-bert-base-cased)

### Our best model's results (epoch 6)

1. On development set

```
 Label                      Precis   Recall   Fscore     #TPs   #Preds   #Golds
                               ion
-------------------------- -------- -------- -------- -------- -------- --------
 ANATOMICAL_STRUCTURE        76.92    80.51    78.67      190      247      236
 ARCHAEON                    100.0    100.0    100.0        7        7        7
 BACTERIUM                   74.19    85.19    79.31       69       93       81
 BODY_PART_ORGAN_OR_ORGAN    87.76    87.65     87.7     1455     1658     1660
 _COMPONENT
 BODY_SUBSTANCE              97.31    95.59    96.44      434      446      454
 CARDINAL                    85.12    90.44     87.7     6452     7580     7134
 CELL                         81.8    88.78    85.15     5285     6461     5953
 CELL_COMPONENT              86.58    82.01    84.23     3451     3986     4208
 CELL_FUNCTION               98.47    98.38    98.42     1093     1110     1111
 CELL_OR_MOLECULAR_DYSFUN    99.16    97.35    98.25      588      593      604
 CTION
 CHEMICAL                    84.23     87.3    85.74    30251    35916    34651
 CORONAVIRUS                 99.36    99.26    99.31     5267     5301     5306
 DAILY_OR_RECREATIONAL_AC    100.0    97.85    98.91      318      318      325
 TIVITY
 DATE                        80.94    83.47    82.19     3555     4392     4259
 DIAGNOSTIC_PROCEDURE        95.02    96.33    95.67      210      221      218
 DISEASE_OR_SYNDROME          84.8     85.2     85.0    12667    14938    14867
 EDUCATIONAL_ACTIVITY        94.12    88.89    91.43       16       17       18
 EUKARYOTE                   94.06    96.04    95.04     2645     2812     2754
 EVENT                       29.41    17.86    22.22        5       17       28
 EVOLUTION                   97.85    98.95     98.4     1227     1254     1240
 EXPERIMENTAL_MODEL_OF_DI    90.55    96.64     93.5      115      127      119
 SEASE
 FAC                         51.28    18.35    27.03       20       39      109
 FOOD                        91.74    97.09    94.34      100      109      103
 GENE_OR_GENOME              79.38    85.28    82.22    27259    34340    31965
 GOVERNMENTAL_OR_REGULATO    93.44    100.0    96.61       57       61       57
 RY_ACTIVITY
 GPE                         73.51    70.69    72.07     1365     1857     1931
 GROUP                       98.94    99.27     99.1     3531     3569     3557
 GROUP_ATTRIBUTE             92.31    85.71    88.89       12       13       14
 HUMAN-CAUSED_PHENOMENON_    96.97    100.0    98.46       32       33       32
 OR_PROCESS
 IMMUNE_RESPONSE             97.14    98.71    97.92     1837     1891     1861
 INDIVIDUAL_BEHAVIOR         95.29    98.78    97.01       81       85       82
 INJURY_OR_POISONING         95.24    95.24    95.24       80       84       84
 LABORATORY_OR_TEST_RESUL    96.97    96.64    96.81      288      297      298
 T
 LABORATORY_PROCEDURE        95.78    94.47    95.12     1179     1231     1248
 LANGUAGE                    69.23     50.0    58.06        9       13       18
 LAW                         31.67     25.0    27.94       19       60       76
 LIVESTOCK                   98.08    96.45    97.26      869      886      901
 LOC                         75.72    51.17    61.07      131      173      256
 MACHINE_ACTIVITY            97.67    100.0    98.82       42       43       42
 MATERIAL                    94.16    87.88    90.91      145      154      165
 MOLECULAR_FUNCTION          96.69    97.03    96.86     2222     2298     2290
 MONEY                       59.15    49.41    53.85       42       71       85
 NORP                        69.74     71.7    70.71      461      661      643
 ORDINAL                     88.16    95.05    91.48      730      828      768
 ORG                         67.18    60.87    63.87     3187     4744     5236
 ORGANISM                    85.67    84.07    84.86     3695     4313     4395
 ORGAN_OR_TISSUE_FUNCTION    95.34    96.98    96.15      225      236      232
 PERCENT                     84.85    68.29    75.68       28       33       41
 PERSON                      56.81    44.62    49.98      692     1218     1551
 PHYSICAL_SCIENCE            100.0    100.0    100.0       22       22       22
 PRODUCT                     50.63    31.86    39.11      202      399      634
 QUANTITY                    68.52    63.93    66.15      296      432      463
 RESEARCH_ACTIVITY           99.39     98.8     99.1      657      661      665
 SIGN_OR_SYMPTOM             94.56    95.38    94.96      330      349      346
 SOCIAL_BEHAVIOR              98.8    96.85    97.81      246      249      254
 SUBSTRATE                   96.59    98.46    97.51      510      528      518
 THERAPEUTIC_OR_PREVENTIV    97.73    98.54    98.13     2966     3035     3010
 E_PROCEDURE
 TIME                        71.97     66.9    69.34       95      132      142
 TISSUE                      78.04     70.9     74.3     1162     1489     1639
 VIRAL_PROTEIN               91.09    93.56    92.31      654      718      699
 VIRUS                       90.18    95.01    92.53     3085     3421     3247
 WILDLIFE                    98.46    98.31    98.38      638      648      649
 WORK_OF_ART                 18.75     9.23    12.37        6       32       65
 Overall                     84.62    86.43    85.52   134507   158949   155626


2020-07-06 00:23:59,851 - INFO - allennlp.commands.evaluate - Finished evaluating.
2020-07-06 00:23:59,851 - INFO - allennlp.commands.evaluate - Metrics:
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - num_matches: 134507
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - num_predictions: 158949
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - num_golds: 155626
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - precision: 84.62274062749687
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - recall: 86.42964543199723
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - fscore: 85.5166494476675
2020-07-06 00:23:59,852 - INFO - allennlp.commands.evaluate - loss: 0.00023669198562777864
```

2. On test set

```
 Label                      Precis   Recall   Fscore     #TPs   #Preds   #Golds
                               ion
-------------------------- -------- -------- -------- -------- -------- --------
 ANATOMICAL_STRUCTURE        76.62    76.62    76.62      390      509      509
 ARCHAEON                     96.3     96.3     96.3       52       54       54
 BACTERIUM                    79.8    90.51    84.82      391      490      432
 BODY_PART_ORGAN_OR_ORGAN    87.03    84.79     85.9     3517     4041     4148
 _COMPONENT
 BODY_SUBSTANCE              95.56    96.72    96.14     1357     1420     1403
 CARDINAL                    82.36    90.94    86.44    54376    66021    59793
 CELL                        82.24    87.52     84.8    15278    18578    17456
 CELL_COMPONENT              83.03    81.41    82.21     9789    11790    12024
 CELL_FUNCTION               95.33    97.66    96.48     1797     1885     1840
 CELL_OR_MOLECULAR_DYSFUN    98.91    98.91    98.91     2267     2292     2292
 CTION
 CHEMICAL                    83.55     84.6    84.07    94459   113056   111650
 CORONAVIRUS                 98.46    98.94     98.7    21928    22271    22162
 DAILY_OR_RECREATIONAL_AC     97.2    98.85    98.02     1460     1502     1477
 TIVITY
 DATE                        80.24    83.79    81.98    30231    37675    36080
 DIAGNOSTIC_PROCEDURE        94.72    96.57    95.64      592      625      613
 DISEASE_OR_SYNDROME         84.85    84.99    84.92    30717    36202    36140
 EDUCATIONAL_ACTIVITY        90.91    93.75    92.31       30       33       32
 EUKARYOTE                   89.68    95.04    92.28     5268     5874     5543
 EVENT                       40.79    17.71     24.7       31       76      175
 EVOLUTION                   97.16    98.46     97.8     5301     5456     5384
 EXPERIMENTAL_MODEL_OF_DI    96.05    97.33    96.69      146      152      150
 SEASE
 FAC                         42.75    10.87    17.34       56      131      515
 FOOD                        89.12     93.4    91.21      467      524      500
 GENE_OR_GENOME              76.07    74.83    75.45    71833    94426    95993
 GOVERNMENTAL_OR_REGULATO    65.76    99.18    79.08      121      184      122
 RY_ACTIVITY
 GPE                          78.4    74.71    76.51     7020     8954     9396
 GROUP                       98.48    99.25    98.86    11104    11275    11188
 GROUP_ATTRIBUTE              88.1    100.0    93.67       74       84       74
 HUMAN-CAUSED_PHENOMENON_    95.88    98.94    97.38       93       97       94
 OR_PROCESS
 IMMUNE_RESPONSE             97.29    99.42    98.35     1725     1773     1735
 INDIVIDUAL_BEHAVIOR          84.5    93.09    88.59      229      271      246
 INJURY_OR_POISONING          93.6    95.12    94.35      117      125      123
 LABORATORY_OR_TEST_RESUL    95.63    97.47    96.54      810      847      831
 T
 LABORATORY_PROCEDURE        93.24    95.43    94.32     4030     4322     4223
 LANGUAGE                    78.57    61.11    68.75       22       28       36
 LAW                         43.98    22.51    29.78       95      216      422
 LIVESTOCK                   96.67    97.26    96.96     2091     2163     2150
 LOC                         70.63    43.34    53.72      267      378      616
 MACHINE_ACTIVITY            97.35    96.08    96.71      147      151      153
 MATERIAL                     94.8    90.46    92.58      237      250      262
 MOLECULAR_FUNCTION          96.31    97.91     97.1     4930     5119     5035
 MONEY                       50.97    32.99    40.05      158      310      479
 NORP                        70.48    70.79    70.63     1294     1836     1828
 ORDINAL                     85.55    95.82    90.39     4220     4933     4404
 ORG                         66.33    50.37    57.26     9289    14004    18440
 ORGANISM                     85.8    83.32    84.54     9015    10507    10820
 ORGAN_OR_TISSUE_FUNCTION    89.84    94.01    91.88      345      384      367
 PERCENT                     66.33    42.76     52.0       65       98      152
 PERSON                      56.02    51.16    53.48     4027     7188     7872
 PHYSICAL_SCIENCE             96.8    93.08     94.9      121      125      130
 PRODUCT                      52.6    35.28    42.23      930     1768     2636
 QUANTITY                    71.15    73.38    72.25     3095     4350     4218
 RESEARCH_ACTIVITY           98.63    98.75    98.69     2600     2636     2633
 SIGN_OR_SYMPTOM             95.07    96.39    95.73     1310     1378     1359
 SOCIAL_BEHAVIOR             95.73    98.18    96.94      538      562      548
 SUBSTRATE                   95.99    98.46    97.21     1341     1397     1362
 THERAPEUTIC_OR_PREVENTIV    97.28    98.86    98.06     7551     7762     7638
 E_PROCEDURE
 TIME                        86.67    85.33     86.0     1437     1658     1684
 TISSUE                       78.1    74.66    76.34     4223     5407     5656
 VIRAL_PROTEIN               89.39    91.09    90.23     1053     1178     1156
 VIRUS                       89.18    95.09    92.04     5383     6036     5661
 WILDLIFE                    98.43    97.56    97.99     1438     1461     1474
 WORK_OF_ART                 34.75    14.44     20.4       41      118      284
 Overall                     82.83    83.23    83.03   444319   536416   533872


2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - Finished evaluating.
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - Metrics:
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - num_matches: 444319
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - num_predictions: 536416
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - num_golds: 533872
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - precision: 82.83104903656864
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - recall: 83.22575448796715
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - fscore: 83.02793266859015
2020-07-05 23:17:02,695 - INFO - allennlp.commands.evaluate - loss: 0.0002649060442224623
```

3. On our manually annotated test set

```
 Label                        Precis   Recall   Fscore   #TPs   #Preds   #Golds
                                 ion
---------------------------- -------- -------- -------- ------ -------- --------
 CHEMICAL                       3.01    55.26     5.71     21      697       38
 DISEASE_OR_SYNDROME           49.16    47.27     48.2    147      299      311
 GENE_OR_GENOME                 24.6    28.48     26.4    170      691      597
```

* Confusion Matrix

![Confusion matrix](https://imgur.com/download/kEc1NXk)

### Scispacy

On manually annotated test set

1. Using pretrained Scispacy on BC5CDR

```
 Label                 Precision   Recall   Fscore   #TPs   #Preds   #Golds
--------------------- ----------- -------- -------- ------ -------- --------
 CHEMICAL                   7.95    31.58     12.7     12      151       38
 DISEASE_OR_SYNDROME       36.01    56.27    43.91    175      486      311
```

2. Using pretrained Scispacy on BIONLPCG13

* Please note that `CANCER` type in CG13 is treated as `DISEASE_OR_SYNDROME`

```
 Label                 Precision   Recall   Fscore   #TPs   #Preds   #Golds
--------------------- ----------- -------- -------- ------ -------- --------
 CHEMICAL                  12.16    23.68    16.07      9       74       38
 DISEASE_OR_SYNDROME        6.45     1.29     2.14      4       62      311
 GENE_OR_GENOME            45.92    38.69     42.0    231      503      597
```

# Candidate Generation

Pretrained Bio word2vec: `BioWordVec_PubMed_MIMICIII_d200`

Download link: [https://github.com/ncbi-nlp/BioSentVec](https://github.com/ncbi-nlp/BioSentVec)

### Our best model's results (epoch 202)

1. Using gold mentions

a. On MedMentions development set

```
Recall@1: 41.369 (32103 / 77602)
Recall@10: 63.177 (49027 / 77602)
Recall@20: 67.286 (52215 / 77602)
Recall@30: 69.335 (53805 / 77602)
Recall@40: 70.609 (54794 / 77602)
Recall@50: 71.487 (55475 / 77602)
```

b. On our manually annotated test set

```
Recall@1: 24.267 (265 / 1092)
Recall@10: 42.949 (469 / 1092)
Recall@20: 47.070 (514 / 1092)
Recall@30: 48.810 (533 / 1092)
Recall@40: 50.000 (546 / 1092)
Recall@50: 50.916 (556 / 1092)
```

c. On our exact-match test set

```
Recall@1: 29.78% (89,996/302,166)
Recall@10: 48.33% (146,027/302,166)
Recall@20: 53.89% (162,847/302,166)
Recall@30: 56.22% (169,863/302,166)
Recall@40: 57.53% (173,843/302,166)
Recall@50: 58.74% (177,486/302,166)
```

2. Using predicted mentions from our NER model on our exact-match test set

a. Overall score

```
Recall@1: 27.61% (83,429/302,166)
Recall@10: 44.56% (134,632/302,166)
Recall@20: 49.74% (150,285/302,166)
Recall@30: 51.88% (156,777/302,166)
Recall@40: 53.08% (160,401/302,166)
Recall@50: 54.19% (163,747/302,166)
```

b. Normalized score (using true positive mentions only)

```
Recall@1: 30.31% (83,429/275,272)
Recall@10: 48.91% (134,632/275,272)
Recall@20: 54.60% (150,285/275,272)
Recall@30: 56.95% (156,777/275,272)
Recall@40: 58.27% (160,401/275,272)
Recall@50: 59.49% (163,747/275,272)
```

# Ranking

### Our best model's results (epoch 20)

1. Using gold mentions

a. On MedMentions development set

- Using top-1 candidate from candidate generation

```
```

- Using ranking model on top-30 candidates

```
 Description                                                                  #
------------------------------------------------------- ------------------------
 # gold mentions:                                                        77,606
 # predicted mentions:                                                   73,202
 # mention-level precision:                              44.85% (32,828/73,202)
 # mention-level recall:                                 42.30% (32,828/77,606)
 # mention-level fscore:                                                 43.54%
```

2. Using predicted mentions from our NER model (pipeline)

a. On our exact-match test set

- Using top-1 candidate from candidate generation

```
 Description                                                                  #
------------------------------------------------------ -------------------------
 # gold mentions:                                                       302,166
 # predicted mentions:                                                  536,415
 # mention-level precision:                             15.55% (83,429/536,415)
 # mention-level recall:                                27.61% (83,429/302,166)
 # mention-level fscore:                                                 19.90%
```

- Using ranking model on top-30 candidates

```
 Description                                                                  #
------------------------------------------------------ -------------------------
 # gold mentions:                                                       302,166
 # predicted mentions:                                                  412,456
 # mention-level precision:                             18.75% (77,316/412,456)
 # mention-level recall:                                25.59% (77,316/302,166)
 # mention-level fscore:                                                 21.64%
```
