# Data Scientist Syllabus: zero to ~~hero~~ 0.5

50% of the bare minimum, in 5% of the time

* *"Appreciate the existence of"* means:
    * Know that this thing exists and roughly what it does
    * But it's _not_ necessary to know how or why it works
* ~~Strikethrough~~ means:
    * This topic is not being covered *on purpose*, to minimize the scope of the syllabus

## [Foundation Module](./Foundation/README.md) (1 week)

* Mathematics
    * Basic linear algebra (vectors and matrices)
    * Basic probability and statistics (including distributions and Bayes' Theorem)
* Programming
    * Markdown
    * Python 3, (basic) regex, pandas, pydantic, fastapi, jupyter
        * Google's Python Class
        * Official Python Tutorial 1 to 8, 9.8 to 9.10 (if you have no Python knowledge)
        * Do we want to give an exemplar regex cheat sheet?
    * Git
    * Unix tools and scripting
        * [CS2043 lectures 1 to 8](https://www.cs.cornell.edu/courses/cs2043/2014sp/)
    * minimal SQL
        * `SELECT <named column> AS <renamed column>`
        * `COUNT(*)` and `COUNT(DISTINCT <column_name>)`
        * `UPDATE`
        * only 3 joins: `(INNER) JOIN`, `LEFT JOIN`, `LEFT OUTER JOIN`
        * `UNION`
        * `GROUP BY`
        * `WHERE`
        * `DATE('YYYY-mm-dd')` (or whatever is native to your SQL dialect)
        * `START TRANSACTION`, `ROLLBACK`, `COMMIT`
    * **Avery's comments on code style:**
        * Pls provide type hints for core algorithmic functions (and a description, if the algo is not obvious)
        * Pls give important functions and variables appropriately descriptive names
        * Pls break your code into logical chunks (and at a higher level, into reusable functions / classes)
        * Pls add comments to describe what each logical chunk accomplishes, if it's not immediately obvious
        * Pls use a code formatter (any formatter) and static analyzer
            * if you don't know what static analyzers are or what they do,
              just use an IDE like PyCharm and keep your code squiggle-free
* Distance Measures
    * Equal-length vectors / sequences
        * Manhattan / Euclidean distances
        * Hamming distance
        * Cosine similarity (normalized dot product)
        * Pearson's coefficient (aka the linreg r²), covariance
    * Variable-length strings
        * Edit / Levenshtein distance (longest common subsequence)
        * BLEU score (n-grams)
    * Variable-size sets
        * Jaccard similarity (intersection over union)
    * *Appreciate the existence of:*
        * *Edit distance backtracking*
        * *Smoothed BLEU score*
        * *METEOR*
        * *ROUGE*
        * *Damerau-Levenshtein distance*
        * *haversine distance*
        * *Overlap coefficient*
        * *Spearman's coefficient (monotonicity)*
        * *gini coefficient (for categorical sequences)*
* ~~how HTML/CSS works (usually to help with crawling)~~
* ~~Splunk~~
* ~~Advanced regex~~
    * ~~Backreferences~~
    * ~~Positive / negative look-ahead~~
    * ~~Positive / negative look-behind~~
    * ~~Non-capturing groups~~
    * ~~Efficiency~~
    * ~~Character classes~~
* ~~How to install and set up Linux~~
    * ~~How to install GPU drivers~~
    * ~~How to set up your network config~~
* ~~Less-common algorithms~~
    * ~~Strings~~
        * ~~Longest common substring~~
        * ~~Sequence alignment / warping~~
        * ~~Multiple string search (e.g., Aho Corasick)~~
        * ~~Fuzzy string matching~~
    * ~~Non-strings~~
        * ~~Recursion~~
        * ~~Graph algorithms (DFS/BFS, A-star, Bellman-Ford, MST, flows, cliques, etc.)~~
        * ~~Unusual data structures (linked lists, circular buffers, tries, etc.)~~
        * ~~Satisfiability (CSP, linear programming, etc.)~~
        * ~~Sorting algorithms~~
        * ~~Searching (BST, heaps, hash tables, bloom filters)~~
        * ~~FFT~~
* ~~How to use oracle's XML tables~~
* ~~Excel, pivot tables, charts, solver~~
* ~~Tableau / plotly / streamlit~~

[//]: # (TODO: experimental design?)

## Data Wrangling, EDA, Visualization, Cleaning

* Splitting data into a training/validation set and a "sacred" test set, avoiding leakage
* *(WIP) Featurization*
    * Handling data types
        * Categorical features - usually encoded
            * Unique labels / categories with insanely high cardinality are usually dropped
            * One-hot encoding (for categories of reasonably low cardinality - or use -1 and 1, and 0 for missing
              values)
            * Ordinal encoding for things like likert scales (but be warned that how these are interpreted sometimes
              vary from person to person, so their survey responses may not be comparable - only the differences between
              responses to questions may be valid)
        * Numerical features - sometimes quantized or normalized
            * Discretization/quantization/binning (equal-frequency, equal-width, clustering, handmade lookup table,
              etc.)
            * *Appreciate the existence of: z-score standardization, l2 normalization, min-max scaling*
            * ~~Log-linearizing~~
        * Constructed features - when the base features can be made sense of in more ways
            * e.g., "is this guest a noble?" or "is this guest a domestic helper?" for titanic
            * *Appreciate the existence of: using proxy variables when "true" values are unavailable*
    * Imputation of null values
    * Feature importance and selection (SHAP, permutation)
    * gotchas to avoid
        * negative effects of having strongly-correlated features (in some models)
        * accidentally introducing time (e.g., via sequential ids, or shadows in labeled images of tanks)
* ~~Dimension reduction~~
    * ~~VC dimension~~
    * ~~Auto-encoders~~
    * ~~PCA~~
    * ~~UMAP/PaCMAP~~

* *WIP: data viz*
* *WIP: data cleaning, dvc*
* *WIP: ETL, pipelines*
* *WIP: data format wrangling? move unicode here?*

## [Machine Learning](./Machine%20Learning/README.md) (1 month)

* Supervised Learning
    * Regression
        * Linear, ridge, lasso
        * Logistic
    * Classification
        * KNN
        * Support vector machine (just a linear SVM for binary classification)
        * Decision trees
    * Ensemble
        * Bagging (e.g., random forests)
        * Boosting (e.g., using `XGBoost` or `LightGBM`)
        * Stacking
    * Metrics
        * Confusion matrix
        * Recall, precision, F1 score
        * ROC curve, AUC, [AUPRC](https://arxiv.org/html/2401.06091v1)
        * Micro vs macro averaging
        * How to choose a threshold
        * *Appreciate the existence of: MRR, MAP, NDCG*
    * (Convex, single-objective) Optimization
        * Loss function
        * Bias / variance trade-off
        * What is over-fitting and under-fitting
        * Curse of dimensionality
        * Cross-validation, hyperparameter tuning
        * *Appreciate the existence of:*
            * *Regularization*
            * *Bayesian optimization, e.g., the `hyperopt` library for Python*
* Unsupervised Learning
    * Clustering
        * K-means
        * EM GMM
        * Density
        * Hierarchical
    * Types of anomaly detection
        * Parametric (e.g., standard deviations away from mean)
        * Non-parametric (e.g., quartiles, box-and-whisker plot)
    * Types of topic modeling
        * LSA (or NMF; these are kind of based on factorization)
        * LDA (based on generative models)
        * Hierarchical / agglomerative (based on similarity measures)
    * Frequent itemset mining
* *Appreciate the existence of*
    * *Reinforcement Learning*
    * *Genetic/evolutionary Algorithms*
    * *Why they are different from supervised / unsupervised*
* Neural Networks (this segment is still a work in progress)
    * Backpropagation
    * Deep neural networks
        * Feedforward
        * CNN, pooling, cross-entropy, softmax
        * RNN, LSTM
        * Dropout
* Tutorials / Capstone Project
    * use jupyter and python
    * learn and use `pandas` (and maybe how it relates to SQL?)
    * `scipy`, `numpy`, `sklearn`
    * Visualization (charts & graphs with `seaborn`)
    * Titanic (with mandatory walkthroughs)
        * if you've done this before:
          you can choose another kaggle, or just speedrun this project
        * Data exploration and data cleaning
            * Dealing with missing values
            * Finding and fixing outliers
        * Featurization, feature importance, feature selection
            * Categorical to one-hot encoding
            * Binning (e.g., quartiles)
            * Removing highly-correlated features to reduce dimensionality
                * PCA is not a measure of feature importance
    * Presentation to group covering process, outcome, and learning points
* ~~"Advanced" regressions~~
    * ~~Isotonic~~
    * ~~Heteroskedastic~~
    * ~~Kernel~~
    * ~~Quadratic / polynomial~~
    * ~~Robust regressions (e.g., repeated median regression)~~
* ~~Non-linear and non-binary SVMs~~
    * ~~Kernels~~
    * ~~Ranking~~
    * ~~Ordinal~~
    * ~~Multiclass~~
* ~~Other ML topics~~
    * ~~Semi-supervised learning (e.g., LLDA)~~
    * ~~Self-organising maps (clustering)~~
    * ~~Association rules~~
    * ~~MLE, maxent~~
    * ~~GANs~~
    * ~~Expectation maximisation~~
    * ~~Working with unbalanced data~~
    * ~~Embeddings~~
    * ~~Recommendation systems aside from itemset mining~~
* ~~KL / JS divergence~~
* ~~Time-series data~~
    * ~~ARIMA~~
    * [~~Facebook Prophet~~](https://facebook.github.io/prophet/)
      *([update](https://medium.com/@cuongduong_35162/facebook-prophet-in-2023-and-beyond-c5086151c138):
      use [statsforecast](https://nixtla.github.io/statsforecast/) or [neuralprophet](https://neuralprophet.com/)
      instead)*
* ~~Non-convex optimization~~

## [Natural Language Processing](./Natural%20Language%20Processing/README.md) (1 month)

* Unicode
    * [Joel Spolsky's article on Unicode](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)
    * see also https://tonsky.me/blog/unicode/
    * [`regex`](https://pypi.org/project/regex/)'s grapheme-match
      pattern [`\X`](https://github.com/mrabarnett/mrab-regex#matching-a-single-grapheme-x)
    * Fixing [mojibake](https://en.wikipedia.org/wiki/Mojibake)
* Text Preprocessing (`NLTK`)
    * Language identification
    * Tokenization and segmentation (and what is an n-gram)
    * Stemming and lemmatization
    * POS tagging
    * Bag of words / bag of n-grams
    * Byte pair encoding and subword tokenization (e.g., sentencepiece, tiktoken)
    * Multilingual text embeddings
* (Small) Language Models (Stanford NLP)
    * HMMs
    * N-grams
    * OOV and simple smoothing methods
    * Interpolation and back-off
* Text Classification and Sentiment Analysis (Stanford NLP)
    * Naïve Bayes classifier
* Named Entity Recognition (Stanford NLP)
    * As a sequence labeling problem
        * Greedy
        * Viterbi
        * Beam
    * *Appreciate the existence of:*
        * *CRFs, which are like super-powered HMMs for sequence-to-sequence*
* Information Retrieval and Ranked IR (Stanford NLP)
    * Inverted index
    * TF-IDF
    * Approximate nearest neighbors, e.g., `FAISS` (for indexing vectors)
    * *Appreciate the existence of:*
        * *Locality sensitive hashing (e.g., minhash vectors)*
        * *Variants of TF-IDF (SMART IR system, Okapi BM25)*
        * *geohashing (only for 2d space)*
* Neural Networks for NLP (optional)
    * Transformers & Muppet models
* Capstone Project
    * Kaggle Avito (or new project?)
        * MUST use word vectors
        * MUST also use TF-IDF or edit / lev distance
        * ~~Images not necessary~~
    * Presentation to group as usual
* ~~Linguistics~~
    * ~~Grammar and syntax parsing (CFGs, CYK)~~
    * ~~Semantics~~
    * ~~Polysemy / metonymy (word sense disambiguation)~~
    * ~~Semiotics (e.g., emoji)~~
    * ~~Morphology~~
    * ~~Ontology~~
* ~~Machine translation~~
    * ~~IBM models~~
    * ~~Back-translation~~
    * ~~Syntax-based SMT~~
    * ~~Corpus alignment / crawling / creation~~
    * ~~Word vector alignment (e.g., Procrustes)~~
* ~~Information extraction / relation extraction~~
* ~~Question answering~~
* ~~Summarization / simplification~~
* ~~How do CRFs work (used for NER tagging)~~
* ~~Spelling / grammar correction~~

## [Automatic Speech Recognition](./Automatic%20Speech%20Recognition/README.md) (1 month)

> ⚠
> 
> This is very outdated!
> Instead, you probably need to learn conformers, transformers, transducers, and maybe CTCs.

* Fundamentals of Speech Recognition (Stanford CS224S Lecture 1)
* Language Modelling (Edinburgh)
    * Lexicon and language model
* Acoustic Modeling and Decoding
    * HMM, forward-backward, and Viterbi (Stanford CS224S Lecture 3)
    * Word error rate, training, and advanced decoding (Stanford CS224S Lecture 4)
        * How to weight the AM and LM
        * Viterbi beam decoding
        * Multi-pass decoding e.g., N-best lists, lattices, word graphs, meshes / confusion networks
        * Finite state methods
    * GMM acoustic modeling and feature extraction (Stanford CS224S Lecture 5)
    * Neural network acoustic models in speech recognition (Stanford CS224S Lecture 7)
* End-to-End Neural Network Speech Recognition (Stanford CS224S Lecture 8) (optional)
* Kaldi Tutorial
* SAGE Tutorial (this will be imported into Confluence because it can't be put on GitHub)

## Storytelling

*WIP*
