#   PTR Training Package
To train up new PTR officers to bare minimum competency level


##  Prerequisites
*   Minimal mathematical foundation knowledge
*   Some programming background
*   Ability and willingness to learn independently with limited guidance
*   [Install Anaconda Python 3](https://www.anaconda.com/distribution/#download-section)
*   [Jupyter Notebook Extensions *(optional)*](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/)


##  Contents
| S/N | Domain                                                                    | Estimated Duration |
| --- | ------------------------------------------------------------------------- | ------------------ |
| 1   | [Foundation](Foundation/README.md)                                        | 2 weeks            |
| 2   | [Machine Learning](Machine%20Learning/README.md)                          | 2 months           |
| 3   | [Natural Language Processing](Natural%20Language%20Processing/README.md)  | 1 month            |
| 4   | [Automatic Speech Recognition](Automatic%20Speech%20Recognition/README.md)| 1 month            |


##  (Bonus) Interesting Reads
For officers to take a break from lectures 😊
*    [The Tao of Programming](http://www.mit.edu/~xela/tao.html)
*    [The Codeless Code](http://www.thecodelesscode.com/contents)
*    [Some AI Koans](http://catb.org/jargon/html/koans.html)


##  Original Training Packages
*   [PTR Training Package](https://www.dropbox.com/s/cqa6g2rrk5at6as/Trainingpackage.docx?dl=0)
*   [ASR Training Package](https://www.dropbox.com/sh/id3pp9wjhasz5rx/AACzS2mVfKeuQbpWTi-TiUNIa?dl=0)
*   [DA Training Package](https://gist.github.com/shanesoh/6ec2a65187638b32448be82222a754ce)


##  Future Plans
*   [x] split up the syllabus and the curriculum for this package:
    *   [x] the syllabus notes down things that need to be learned and outcomes that should be achieved
    *   [ ] the curriculum collates and orders the material needed to cover the syllabus
    *   makes it easy to look for better materials and make updates to the curriculum, 
        while making sure the scope of the training package doesn’t drift too much
    *   but it’s more effort than I feel is justified right now; after all we’re CSIT not MOE
*   deep learning in the ML module

### added by Avery, maybe we'll look at them someday
*   [deep learning specialization course](https://www.deeplearning.ai/deep-learning-specialization/) (free to audit)
*   [google AI education](https://ai.google/education/)
    *   [google ML crash course](https://developers.google.com/machine-learning/crash-course)
    *   [glossary](https://developers.google.com/machine-learning/glossary/)
    *   [rules for ML](https://developers.google.com/machine-learning/guides/rules-of-ml/)
    *   [Data Preparation and Feature Engineering in ML](https://developers.google.com/machine-learning/data-prep/)
    *   [problem framing](https://developers.google.com/machine-learning/problem-framing/)
    *   [debugging ML](https://developers.google.com/machine-learning/testing-debugging/)
    *   [recommendation systems](https://developers.google.com/machine-learning/recommendation/)
    *   [clustering](https://developers.google.com/machine-learning/clustering/)
    *   [how to deal with users](https://pair.withgoogle.com/)
    *   [technical debt in ML](https://ai.google/research/pubs/pub43146)
    *   [wizard of oz models](https://medium.com/google-design/human-centered-machine-learning-a770d10562cd)
*   [kaggle courses](https://www.kaggle.com/learn/overview)
*   [see sidebar for titanic walkthroughs](https://techdevguide.withgoogle.com/paths/machine-learning/sequence-2/kaggle-competition-titanic/#!)
*   [see page 130](https://www.acm.org/binaries/content/assets/education/cs2013_web_final.pdf)
*   [10 rules for better Jupyter notebooks](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007007)
*   SQL
    *   [intro to SQL](https://mystery.knightlab.com/walkthrough.html)
    *   [how SQL queries really work](https://jvns.ca/blog/2019/10/03/sql-queries-don-t-start-with-select/)
*   [random nlp walkthrough](https://github.com/TiesdeKok/Python_NLP_Tutorial/blob/master/NLP_Notebook.ipynb)
*   [visualization walkthrough](https://github.com/TiesdeKok/LearnPythonforResearch/blob/master/3_visualizing_data.ipynb)
*   [ML in the industry](https://github.com/firmai/industry-machine-learning)
*   algorithms?
    *   BFS / DFS / A*
    *   recursion, tail call elimination
    *   binary search in a sorted list
    *   sorting
    *   complexity
    *   parallelism, sync/async, locks, atomicity
    *   dynamic programming, memoization
*   what is the value in data?
    *   predictive models (regressions)
    *   descriptive models (classifications)
    *   prescriptive models (recommendations)
*   Joel Spolsky’s article on Unicode
*   https://madewithml.com/
*   https://github.com/mrdbourke/machine-learning-roadmap
*   https://sotabench.com/
*   https://github.com/slundberg/shap#tree-ensemble-example-with-treeexplainer-xgboostlightgbmcatboostscikit-learnpyspark-models
*   use Kaggle’s SQL tutorial?


### data science workflow
1.  data acquisition
    *   if you're new, then maybe 'just getting data' doesn't seem ike it warrants a mention
    *   trust me, it does
2.  ETL
    *   transforming data between formats (csv, json, html/xml, pipe-delimited, ...)
    *   fixing broken formats (such as unquoted csv ಠ_ಠ)
3.  exploration
    *   just look at a subset if your dataset can't fit in RAM, but make sure it's not a biased subset
    *   correlation matrix
    *   parallel coordinate plot / Andrews plot  / Kent–Kiviat radar m chart
    *   `df.describe()`
    *   [example](https://www.kaggle.com/mervinpraison/seaborn-to-visualize-iris-data/notebook)
4.  background research and data provenance
    *   understand where the data came from
    *   what the labels mean
    *   any pre-processing that was done that can't be undone
5.  cleaning
    *   outliers / anomalies
    *   missing
    *   `ftfy.fix_text()`, detwingle unicode, decode html entities (possibly recursively), etc
6.  baseline / POC
    *   linear least squares / logistic regression
    *   xgboost
    *   if you're getting abysmal performance, maybe the data is still borked
7.  featurization *(NLP usually happens here)*
    *   categorical to numeric
    *   text processing
    *   binning
    *   t-score normalization
8.  training *(ML usually happens here)*
    *   feature selection
        *   correlation and covariance
    *   model selection
    *   hyperparameter optimization
    *   dimension reduction
    *   stacking/bagging/boosting
9.  testing
    *   as close to real data as possible
10. visualization (of results)
    *   seaborn
11. inference and explanations
    *   if you've gotten this far, congrats
    *   SHAP/LIME
