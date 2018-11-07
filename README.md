
# 1.  Quora Question Pair Similarity 

## 1.1Problem Statement :
Identifying Given pair of questions are Duplicates or not (Similar or not) to provide instant answers 

##### Business objectives and Constraints:
    * cost of miss-classification is very high as customer might get disaapointed with the provided answers
    * No-strict latency requirements (can take some time to provide the answers)
    * Probability of questions being similar to put a threshold
    * Interpretability is partially important

### 1.2 Mapping Real world problem to machine-leanring Problem:
* It's  binary Classification problem (whether the given pair of questions are duplicates are not)


#### Performance Metric to Evaluate the Model:
    * log-loss (As we need probabilities of each prediction) as Primary KPI
    * Confusion-matrix as secondary KPI

#### Overvoew of Dataset:
<p> 
- Data will be in a file train.csv <br>
- Train.csv contains 5 columns : qid1, qid2, question1, question2, is_duplicate <br>
- Size of Train.csv - 60MB <br>
- Number of rows in Train.csv = 404,290
</p>

##### Description of columns:
    * qid1 : unique ID of question number 1
    * qid2 : unique ID of question number 2
    * question1 : Textual content of question1
    * question2 : Textual content of question2
    * is_diplicate : target variable ( whether the given pair of question are duplicates or not) 
        **Note** : 0 : Given pair of questions are not duplicate
                   1 : Given pair of questions are duplicate

##### Train-Test Construction of Dataset:
We build train and test by randomly splitting in the ratio of 70:30  

