## Implementation of BERT-based Exhaustive Neural Named Entity Recognition and Disambiguision (BENNERD) on COVID-19 Dataset

### Backgroud
In response to the coronavirus disease 2019 (COVID-19) pandemic, White House and a coalition of 
research groups have released COVID-19 Open Research Dataset (CORD-19). This dataset further taken 
into account by data mining group of University of Illinois to create a comprehensive named entity 
annotation (CORD-NER), a distantly supervised dataset that includes 29,500 documents. 

#### Corpora Link
    * https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge (CORD-19)
    * https://uofi.app.box.com/s/k8pw7d5kozzpoum2jwfaqdaey1oij93x (CORD-NER)
 
### BENNERD Description
We implement BERT-based exhaustive approach, an open-source scalable and extensible system that implement 
neural models like named entity recognition (NER) and entity disambiguision (ED) or a.k.a entity linking (EL) by addressing  distantly supervise-based CORD-NER data-set.

### BENNERD DEMO
Besides BENNERD, we also release an online text analyze system to meet real-time text annotation with visualization. 
* http://prm-ezcatdb.cbrc.jp/denner/

### Sample Data Format
    T1	GENE_OR_GENOME 0 31	Angiotensin-converting enzyme 2
    T2	GENE_OR_GENOME 33 37	ACE2
    T3	CORONAVIRUS 44 54	SARS-CoV-2
    T4	CHEMICAL 55 63	receptor
    T5	CORONAVIRUS 120 130	SARS-CoV-2
    T6	EVOLUTION 158 170	phylogenetic
    T7	WILDLIFE 195 198	bat
    T8	CORONAVIRUS 214 224	SARS-CoV-2
    T9	NORP 259 277	intermediate hosts
    T10	CORONAVIRUS 282 292	SARS-CoV-2

### NER Annotation Performance

    --------------------------------------------------------------------------------------------------
          Model                   Development-set                              Test-set
                        -------------------------------------    -------------------------------------       
                        Precision(%)   Recall(%)  F1-score(%)    Precision(%)   Recall(%)  F1-score(%)
    ------------------  ------------   ---------  -----------    ------------   ---------  -----------
    Our Model (BENNER)      80.39        82.47       81.41           80.54        82.54       81.53
    --------------------------------------------------------------------------------------------------

### NER Performance using different pre-trained BERT models

    --------------------------------------------------------------------------------------------------
          Model                   Development-set                              Test-set
                        -------------------------------------    -------------------------------------       
                        Precision(%)   Recall(%)  F1-score(%)    Precision(%)   Recall(%)  F1-score(%)
    ------------------  ------------   ---------  -----------    ------------   ---------  -----------
    SciBERT                 89.22        87.05       88.12           88.11        83.81       85.91
    ClinicalCovid BERT      87.62        83.34       85.42           86.98        80.43       83.58
    Covid BERT Base         85.56        62.56       72.27           85.29        63.29       72.66
    --------------------------------------------------------------------------------------------------
    
    [*] https://github.com/manueltonneau/covid-berts

### Categorical Performance Based on Selected Categories

    ----------------------------------------------------------------------------------------------
    Label                     Precision(%)   Recall(%)   F1-score(%)     #TPs      #Preds   #Golds
    ------------------------  ------------   ---------   -----------   ---------  --------  ------
    CELL                        83.75          84.05        83.90        79927     95435      9597
    CELL_COMPONENT              83.15          80.58        81.85        47708     57373     59208
    CELL_FUNCTION               96.91          97.36        97.13        11674     12046     11991
    CELL_OR_MOLECULAR_DYSF      95.04          98.94        96.95         8042      8462      8128 
    CHEMICAL                    79.99          81.79        80.88       446923    558705    546402
    DISEASE_OR_SYNDROME         83.96          83.49        83.73       189802    226056    227326
    CORONAVIRUS                 96.97          98.97        97.96        34644     35725     35004
    GENE_OR_GENOME              75.99          78.08        77.02       404927    532844    518630
    MOLECULAR_FUNCTION          93.2           98.11        95.59        26047     27947     26549
    VIRUS                       87.91          93.41        90.58        32415     36871     34700
    WILDLIFE                    94.54          98.35        96.41        12495     13216     12704
    ----------------------------------------------------------------------------------------------

#### Details Categorical Performance
    * https://under_construction
  
### Performance Comparison with State-of-the-art Models on CORD-NER Dataset

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
    Our Model (BENNER)  75.99      78.08    77.02   79.99      81.79    80.88   83.96      83.49    83.73
    ------------------------------------------------------------------------------------------------------

- *Note: The results of SciSpacy are based on ramdomly picked 1000 sentences from CORD-NER dataset, where scores with BENNER is on 4,500
test documents.  

### Acknowledgement:

This work is based on results obtained from a project commissioned by the PRISM

### Citing this work
When using this implementation, please use the following citation:
* under_construction


