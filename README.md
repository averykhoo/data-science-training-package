#   Data Science Training Package
To train up new data scientists to bare minimum competency level


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
When you want to take a break from lectures 😊
*    [The Tao of Programming](http://www.mit.edu/~xela/tao.html)
*    [The Codeless Code](http://www.thecodelesscode.com/contents)
*    [Some AI Koans](http://catb.org/jargon/html/koans.html)


### ML workflow
0.  [asking the right questions](https://developers.google.com/machine-learning/problem-framing)
    *   see also the [data literacy project scoping guide](https://go.gov.sg/project-scoping-guide)
    *   look into elicitation of requirements or ideas from your users
1.  data acquisition
    *   maybe 'just get some labelled training data' doesn't seem like it even warrants a mention
    *   trust me, it does (unless it's an [open source dataset](https://datasetsearch.research.google.com))
2.  ETL
    *   (part of 'wrangling' or 'munging')
    *   transforming data between formats (csv, json, html/xml, pipe-delimited, ...)
    *   fixing broken formats (such as unquoted csv ಠ_ಠ)
    *   minimal data edits for now, at least until you understand the data
3.  [exploration](https://developers.google.com/machine-learning/guides/good-data-analysis)
    *   also known as 'EDA'
    *   just look at a subset if your dataset can't fit in RAM, but make sure it's not a biased subset
    *   `df.describe()`
    *   it is [important](https://www.autodeskresearch.com/publications/samestats) to visualize your data
        *   parallel coordinate plot / Andrews plot  / Kent–Kiviat radar m chart
        *   correlation matrix
        *   [example](https://www.kaggle.com/mervinpraison/seaborn-to-visualize-iris-data/notebook)
4.  background research and data provenance
    *   understand where the data came from
    *   what the labels mean, and how accurate they are, whether there's class imbalance
    *   any pre-processing that was done that can't be undone
5.  [cleaning](https://www.kaggle.com/learn/data-cleaning)
    *   (part of 'wrangling' or 'munging')
    *   outliers / anomalies (eg huge spike in data)
    *   impute missing values
    *   remove noise
    *   handle Unicode
        *   [`ftfy.fix_text`](https://pypi.org/project/ftfy)
        *   [`bs4.UnicodeDammit.detwingle`](https://pypi.org/project/beautifulsoup4)
            (you can also use bs4 to decode html entities (possibly recursively))
        *   [`grapheme`](https://pypi.org/project/grapheme)
            or the `\X` pattern in [`regex`](https://pypi.org/project/beautifulsoup4)
    *   data version control, to track how the data was cleaned
6.  baseline / POC
    *   linear least squares / logistic regression
    *   xgboost
    *   if you're getting abysmal performance, maybe the data is still borked
        *   or maybe it's impossible, and you should just give up
    *   if you're getting suspiciously good performance (especially if you get 100%) something is probably wrong
        *   somehow leaking your label, maybe via an *extremely* correlated variable 
        *   you've effectively split a timeseries into top and bottom halves and are using one to predict the other
        *   or maybe your problem is too easy, and you just need some rules or heuristics 
7.  [featurization](https://www.kaggle.com/learn/feature-engineering) *(NLP usually happens here)*
    *   [categorical to numeric](https://developers.google.com/machine-learning/data-prep/transform/transform-categorical)
    *   [text processing](https://www.kaggle.com/learn/natural-language-processing)
    *   [binning](https://developers.google.com/machine-learning/data-prep/transform/bucketing)
    *   [t-score normalization](https://developers.google.com/machine-learning/data-prep/transform/normalization)
8.  training *(ML usually happens here)*
    *   what is the value in your data? -> ML must be either actionable or informative (or both)
        *   predictive models (regressions)
        *   descriptive models (classifications)
        *   prescriptive models (recommendations)
        *   associative models (clustering)
        *   (this list is not comprehensive - e.g. there are also generative models)
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
    *   also known as 'storytelling'
    *   seaborn![img.png](img.png)![img_1.png](img_1.png)
11. inference and [explanations](https://www.kaggle.com/learn/machine-learning-explainability)
    *   if you've gotten this far, congrats
    *   try LIME / [SHAP](https://github.com/slundberg/shap#tree-ensemble-example-with-treeexplainer-xgboostlightgbmcatboostscikit-learnpyspark-models
12. deploying / sharing your model
    *   [`fastapi`](https://fastapi.tiangolo.com/)
    *   [`streamlit`](https://streamlit.io)
    *   or just share the Jupyter notebook with all your above steps (but clean it up and add explanations first!)
13. developing a clean API
    *   [best practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
    *   [documentation](https://documentation.divio.com)
    *   linting and type-checking your code (e.g. `flake8` and maybe `mypy`)
14. building a UI
    *   UX is more of an art than a science,
        many books have been written,
        none of them cover everything you need to know
    *   but here's a TL;DR for UI: 
        let the user get their thing done as fast as possible, 
        with the fewest possible ways to get it wrong or misunderstand what happened,
        with minimal interaction per transaction,
        ideally not needing to read any instructions or even think about the process,
        and also don't make it ugly 
        or irritating if you have to use it a thousand times (because they probably will have to) 
15. monitoring: collecting usage stats / telemetry
    *   inevitably, management will ask how many people are using your thing
    *   you can't really answer "no clue" and still expect to get your bonus
16. making it faster with better algorithms (do this last, don't prematurely optimize unless it's really too slow)
    *   think about time / space complexity
    *   an inverted index for search
    *   binary search in a sorted list (`bisect`)
    *   dynamic programming, memoization (`lru_cache`), tail call elimination, loop unrolling
    *   approx nearest-neighbor lookup (`annoy`, `scann`)
    *   parallelism (`multiprocessing`), async, locks, atomicity
    *   A* search (as opposed to BFS / DFS)
    *   cython / numba / pypy
17. ml ops
    *   CI/CD (e.g. to push to prod)
    *   version control of models and data
    *   quality metrics, detecting drift, auto retraining
    *   TODO: fill up this bit
