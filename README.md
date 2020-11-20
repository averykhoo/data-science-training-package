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
*   [google ML crash course](https://developers.google.com/machine-learning/crash-course)
*   [glossary](https://developers.google.com/machine-learning/glossary/)
*   [rules for ML](https://developers.google.com/machine-learning/guides/rules-of-ml/)
*   [how to work with users](https://pair.withgoogle.com/guidebook/)
*   [technical debt in ML](https://ai.google/research/pubs/pub43146)
*   [wizard of oz models](https://medium.com/google-design/human-centered-machine-learning-a770d10562cd)
*   [see sidebar for titanic walkthroughs](https://techdevguide.withgoogle.com/paths/machine-learning/sequence-2/kaggle-competition-titanic/#!)
*   [10 rules for better Jupyter notebooks](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007007)
*   what is the value in data? -> ML must be either actionable or informative (or both) 
    *   predictive models (regressions)
    *   descriptive models (classifications)
    *   prescriptive models (recommendations)
    *   associative models (clustering)
*   Unicode
    *   [Joel Spolsky’s article on Unicode](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)
    *   http://reedbeta.com/blog/programmers-intro-to-unicode/
    *   see also [grapheme](https://github.com/alvinlindstam/grapheme), 
        which is a library for working with what you probably think are unicode characters
    *   see also [wcswidth](https://github.com/jquast/wcwidth),
        which gives you the length of a string, double-counting CJK characters since those are double-wide

### ML workflow
0.  [asking the right questions](https://developers.google.com/machine-learning/problem-framing)
1.  data acquisition
    *   if you're new, then maybe 'just getting data' doesn't seem ike it warrants a mention
    *   trust me, it does (unless it's an [open source dataset](https://datasetsearch.research.google.com))
2.  ETL
    *   transforming data between formats (csv, json, html/xml, pipe-delimited, ...)
    *   fixing broken formats (such as unquoted csv ಠ_ಠ)
3.  [exploration](https://developers.google.com/machine-learning/guides/good-data-analysis)
    *   just look at a subset if your dataset can't fit in RAM, but make sure it's not a biased subset
    *   `df.describe()`
    *   it is [important](https://www.autodeskresearch.com/publications/samestats) to visualize your data
        *   parallel coordinate plot / Andrews plot  / Kent–Kiviat radar m chart
        *   correlation matrix
        *   [example](https://www.kaggle.com/mervinpraison/seaborn-to-visualize-iris-data/notebook)
4.  background research and data provenance
    *   understand where the data came from
    *   what the labels mean
    *   any pre-processing that was done that can't be undone
5.  [cleaning](https://www.kaggle.com/learn/data-cleaning)
    *   outliers / anomalies (eg huge spike in data)
    *   impute missing values
    *   remove noise
    *   `ftfy.fix_text()`, `bs4.UnicodeDammit.detwingle`, decode html entities (possibly recursively), etc
6.  baseline / POC
    *   linear least squares / logistic regression
    *   xgboost
    *   if you're getting abysmal performance, maybe the data is still borked
7.  [featurization](https://www.kaggle.com/learn/feature-engineering) *(NLP usually happens here)*
    *   [categorical to numeric](https://developers.google.com/machine-learning/data-prep/transform/transform-categorical)
    *   [text processing](https://www.kaggle.com/learn/natural-language-processing)
    *   [binning](https://developers.google.com/machine-learning/data-prep/transform/bucketing)
    *   [t-score normalization](https://developers.google.com/machine-learning/data-prep/transform/normalization)
8.  training *(ML usually happens here)*
    *   classification/regression/clustering/recommendation/etc...
    *   feature selection
        *   duplicate features: high correlation / covariance
        *   useless features: low / no variance
        *   null features: mostly missing values, with only a small percent of real data
        *   xgboost feature importance
    *   model selection
    *   hyperparameter optimization
    *   [dimension reduction](https://en.wikipedia.org/wiki/Curse_of_dimensionality)
    *   stacking/bagging/boosting
9.  testing (measuring performance)
    *   as close to real data as possible
    *   [debugging](https://developers.google.com/machine-learning/testing-debugging)
10. [visualization](https://www.kaggle.com/learn/data-visualization) (of results)
    *   seaborn
11. inference and [explanations](https://www.kaggle.com/learn/machine-learning-explainability)
    *   if you've gotten this far, congrats
    *   try LIME / [SHAP](https://github.com/slundberg/shap#tree-ensemble-example-with-treeexplainer-xgboostlightgbmcatboostscikit-learnpyspark-models
12. building an API
    *   just use [`fastapi`](https://fastapi.tiangolo.com/)
    *   [best practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
    *   [documentation](https://documentation.divio.com)
13. building a UI
    *   UX is more of an art than a science,
        many books have been written,
        none of them can claim to be comprehensive
    *   TL;DR version: 
        the user wants to get their thing done as fast as possible, 
        with minimal interaction and thinking,
        and ideally no instruction-reading
        (also, don't make it ugly or irritating)
14. making it faster with better algorithms (do this last, don't prematurely optimize unless it's really too slow)
    *   time / space complexity
    *   binary search in a sorted list (`bisect`)
    *   dynamic programming, memoization (`lru_cache`), tail call elimination
    *   approx nearest neighbor lookup (`annoy`)
    *   parallelism (`multiprocessing`), sync/async, locks, atomicity
    *   A* search (as opposed to BFS / DFS)
