# Novozymes-Enzyme-Stability-Prediction
![image](https://user-images.githubusercontent.com/83581531/219054493-5e7ce082-9482-4d2d-8925-72ade4a0d652.png)
## Problem Definition
#### The challange of this competition is to predict the thermostability of enzyme variants. The experimentally measured thermostability (melting temperature) data includes natural sequences, as well as engineered sequences with single or multiple mutations upon the natural sequences.
## Data Set description
#### The Dataset consists of
• Train.csv : the coaching information, with columns as follows:
1. seq id: distinctive symbol of every macromolecule variants
2. macromolecule sequence: organic compound sequence of every macromolecule variant. The stability (as measured by tm) of macromolecule is
decided by its macromolecule sequence.
3. pH: the size accustomed specify the acidity of associate degree solution
underneath that the steadiness of macromolecule was measured. Stability of
an equivalent macromolecule will modification at totally different hydrogen
ion concentration levels.
4. information supply: source wherever the info was published
5. tm: target column. Since solely the spearman correlation are going to
be used for the analysis, the right prediction of the relative order is additional necessary than absolutely the Tm values. (Higher Tm suggests that
the macromolecule variant is additional stable.)
• train updates 20220929.csv - corrected rows in train, please see this
forum post for details
• test.csv - the take a look at data; Our task is to predict the target Tm
for every macromolecule sequence (indicated by a novel seqid)
• samplesubmission.csv - a sample submission come in the right format,
with seq id values adore take a look at.csv
• wildtype structure prediction af2.pdb - the three dimensional structure
of the protein listed on top of, as foretold by AlphaFold.

## Methodology
### Model 1: Random Forest Regressor
![Untitled Diagram drawio (2)](https://user-images.githubusercontent.com/83581531/219157875-4090526a-0c1f-4ff3-919f-ab4fd834822b.png)

#### A Random Forest Regressor model was enforced that is capable of acting each regression and classification tasks with the employment of multiple call trees. The basic plan behind this can be to mix multiple call trees in crucial the ultimate output instead of counting on individual call trees. Then it indiscriminately perform row sampling and have sampling from the dataset forming sample datasets for each model

### Model 2: X Gradient Boosting
![XGBOOST](https://user-images.githubusercontent.com/83581531/219157783-5bc61b6a-4e41-49d3-8045-66fd1b56151c.png)

#### XGBoost is associate optimized distributed gradient boosting library designed to be extremely economical, versatile and moveable. It implements machine learning algorithms below the Gradient Boosting framework. XGBoost provides a parallel tree boosting (also called GBDT, GBM) that solve several information science issues in an exceedingly quick and correct method. an equivalent code runs on major distributed surroundings (Hadoop, SGE, MPI) and might solve issues on the far side billions of examples

###  Model 3: The Levenshtein Algorithm
#### The Levenshtein distance is a string metric for measuring difference between two sequences. Informally, the Levenshtein distance between two words is the minimum number of single-character edits (i.e. insertions, deletions or substitutions) required to change one word into the other. It is named after Vladimir Levenshtein, who considered this distance in 1965. Levenshtein distance may also be referred to as edit distance, although it may also denote a larger family of distance metrics. It is closely related to pairwise string alignments.

### Results and Discussions
#### Sequential model results
#### ![comparision](https://user-images.githubusercontent.com/83581531/219156579-97a64503-17d0-4da6-b775-cb3271844936.png)
#### Inference: Since we have used 3 model out of which x gradient boosting model shows high accuracy than other 2 models .Then deep ddg is better compared to Random Forest.


