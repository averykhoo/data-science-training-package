#   Data Scientist Syllabus: zero to ~~hero~~ 0.5
50% of the bare minimum, in 5% of the time

*   *"Appreciate the existence of"* means:
    *   Know that this thing exists and roughly what it does
    *   But it's _not_ necessary to know how or why it works
*   ~~Strikethrough~~ means:
    *   This topic is not being covered *on purpose*, to minimize the scope of the syllabus

##  [Foundation Module](./Foundation/README.md) (1 week)

*   Mathematics
    *   Basic linear algebra
    *   Basic probability and statistics (including Bayes’ Theorem)
*   Programming
    *   Markdown
    *   Git
    *   Python 3 and basic regex
        *   Google’s Python Class
        *   Official Python Tutorial 1 to 8, 9.8 to 9.10 (if you have no Python knowledge)
        *   Do we want to give an exemplar regex cheat sheet?
    *   Unix tools and scripting
        *   CS2043 lectures 1 to 8
    *   minimal SQL
        *   `SELECT <named columns> AS <renamed columns>`
        *   `COUNT(*)` and `COUNT(DISTINCT column_name)`
        *   `UPDATE`
        *   only 3 joins: `(INNER) JOIN`, `LEFT JOIN`, `LEFT OUTER JOIN`
        *   `UNION`
        *   `GROUP BY`
        *   `WHERE`
        *   `DATE('YYYY-mm-dd')` (or whatever is native to your SQL dialect)
        *   `START TRANSACTION`, `ROLLBACK`, `COMMIT`
    *   Avery’s comments on code style:
        *   Pls provide type hints for core algorithmic functions (and a description, if the algo is not obvious)
        *   Pls give important functions and variables appropriately descriptive names
        *   Pls break your code into logical chunks (and at a higher level, into reusable functions / classes)
        *   Pls add comments to describe what each logical chunk accomplishes, if it's not immediately obvious
        *   Pls use a code formatter (any formatter) and static analyzer
            *   if you don't know what static analyzers are or what they do,
                just use an IDE like PyCharm and keep your code squiggle-free
*   Distance Measures
    *   Equal-length vectors / sequences
        *   Manhattan / Euclidean distances
        *   Hamming distance
        *   Cosine similarity (normalized dot product)
        *   Pearson's coefficient (aka the linreg r²), covariance
    *   Variable-length strings
        *   Edit / Levenshtein distance (longest common subsequence)
        *   BLEU score (n-grams)
    *   Variable-size sets
        *   Jaccard similarity (intersection over union)
    *   *Appreciate the existence of:*
        *   *Edit distance backtracking*
        *   *Smoothed BLEU score*
        *   *METEOR*
        *   *ROUGE*
        *   *Damerau-Levenshtein distance*
        *   *haversine distance*
        *   *Overlap coefficient*
        *   *Spearman's coefficient (monotonicity)* 
        *   *gini coefficient (for categorical sequences)*
*   ~~Splunk~~
*   ~~Advanced regex~~
    *   ~~Backreferences~~
    *   ~~Positive / negative look-ahead~~
    *   ~~Positive / negative look-behind~~
    *   ~~Non-capturing groups~~
    *   ~~Efficiency~~
    *   ~~Character classes~~
*   ~~How to install and set up Linux~~
    *   ~~How to install GPU drivers~~
    *   ~~How to setup your network config~~
*   ~~Less-common algorithms~~
    *   ~~Strings~~
        *   ~~Longest common substring~~
        *   ~~Sequence alignment / warping~~
        *   ~~Multiple string search (e.g. Aho Corasick)~~
        *   ~~Fuzzy string matching~~
    *   ~~Non-strings~~
        *   ~~Recursion~~
        *   ~~Graph algorithms (DFS/BFS, A-star, Bellman-Ford, MST, flows, cliques, etc)~~
        *   ~~Unusual data structures (linked lists, circular buffers, tries, etc)~~
        *   ~~Satisfiability (CSP, linear programming, etc)~~
        *   ~~Sorting algorithms~~
        *   ~~Searching (BST, heaps, hash tables, bloom filters)~~
        *   ~~FFT~~
*   ~~How to use oracle’s XML tables~~


##  [Machine Learning](./Machine Learning/README.md) (1 month)

*   Supervised Learning
    *   Regression
        *   Linear, ridge, lasso
        *   Logistic
    *   Classification
        *   KNN
        *   Support vector machine (just a linear SVM for binary classification)
        *   Decision trees
    *   Ensemble
        *   Boosting (e.g. using `XGBoost` or `LightGBM`)
        *   Stacking
    *   Metrics
        *   Confusion matrix
        *   Recall, precision, F1 score
        *   AUC & ROC curve
        *   Micro vs macro averaging
        *   How to choose a threshold
    *   (Convex) Optimization
        *   Loss function
        *   Bias / variance trade-off
        *   What is over-fitting and under-fitting
        *   Cross-validation, hyperparameter tuning
        *   *Appreciate the existence of:*
            *   *Regularization*
            *   *Bayesian optimization, e.g. the `hyperopt` library for Python*
*   Unsupervised Learning
    *   Clustering
        *   K-means
        *   EM GMM
        *   Density
        *   Hierarchical
    *   Types of anomaly detection
        *   Parametric (e.g. standard deviations away from mean)
        *   Non-parametric (e.g. quartiles, box-and-whisker plot)
    *   Types of topic modelling
        *   LSA (or NMF; these are kind of based on factorization)
        *   LDA (based on generative models)
        *   Hierarchical / agglomerative (based on similarity measures)
    *   Frequent itemset mining
*   *Appreciate the existence of*
    *   *Reinforcement Learning*
    *   *Genetic/evolutionary Algorithms*
    *   *Why they are different from supervised / unsupervised*
*   Neural Networks (this segment is still a work in progress)
    *   Backpropagation
    *   Deep neural networks
        *   Feedforward
        *   CNN, pooling, cross-entropy, softmax
        *   RNN, LSTM
        *   Dropout
*   Tutorials / Capstone Project
    *   use jupyter and python
    *   learn `pandas` and how it relates to SQL
    *   `scipy`, `numpy`, `sklearn`
    *   Visualization (charts & graphs with `seaborn` or the more obscure `altair`)
    *   Titanic (with mandatory walkthroughs)
        *   if you've done this before:
            you can choose another kaggle, or just speedrun this project
        *   Data exploration and data cleaning
            *   Dealing with missing values
            *   Finding and fixing outliers
        *   Featurization
            *   Categorical to one-hot encoding
            *   Binning (e.g. quartiles)
            *   Removing highly-correlated features to reduce dimensionality
    *   Presentation to group covering process, outcome, and learning points
*   ~~"Advanced" regressions~~
    *   ~~Isotonic~~
    *   ~~Heteroskedastic~~
    *   ~~Kernel~~
    *   ~~Quadratic / polynomial~~
    *   ~~Robust regressions (e.g. repeated median regression)~~
*   ~~Non-linear and non-binary SVMs~~
    *   ~~Kernels~~
    *   ~~Ranking~~
    *   ~~Ordinal~~
    *   ~~Multiclass~~
*   ~~Curse of dimensionality~~
    *   ~~VC dimension~~
    *   ~~Auto-encoders~~
    *   ~~Dimensionality reduction~~
    *   ~~PCA~~
*   ~~Other ML topics~~
    *   ~~Semi-supervised learning (e.g. LLDA)~~
    *   ~~Self-organising maps (clustering)~~
    *   ~~Association rules~~
    *   ~~MLE, maxent~~
    *   ~~GANs~~
    *   ~~Expectation maximisation~~
    *   ~~Working with unbalanced data~~
    *   ~~Embeddings~~
    *   ~~Recommendation systems aside from itemset mining~~
*   ~~KL / JS divergence~~
*   ~~Time-series data~~
    *   ~~ARIMA~~
*   ~~Non-convex optimization~~


##  [Natural Language Processing](./Natural Language Processing/README.md) (1 month)

*   Text Preprocessing (`NLTK`)
    *   Tokenization and segmentation (and what is an n-gram)
    *   Stemming and lemmatization
    *   POS tagging
    *   Bag of words / bag of n-grams
*   Word Embeddings
    *   Word Mover’s Distance
    *   *Please appreciate the existence of:*
        *   *Sentence / document embeddings (e.g. doc2vec, Google’s USE)*
        *   *Cross-lingual embeddings (e.g. RCSLS, LASER)*
*   Language Modelling (Stanford NLP)
    *   HMMs
    *   N-grams
    *   OOV and simple smoothing methods
    *   Interpolation and back-off
*   Text Classification and Sentiment Analysis (Stanford NLP)
    *   Naïve Bayes classifier
*   Named Entity Recognition (Stanford NLP)
    *   As a sequence labelling problem
        *   Greedy
        *   Viterbi
        *   Beam
    *   *Appreciate the existence of:*
        *   *CRFs, which are like superpowered HMMs for sequence-to-sequence*
*   Information Retrieval and Ranked IR (Stanford NLP)
    *   Inverted index
    *   TF-IDF
    *   *Appreciate the existence of:*
        *   *Locality sensitive hashing (e.g. minhash vectors)*
        *   *Variants of TF-IDF (SMART IR system, Okapi BM25)*
        *   *approximate nearest neighbors, e.g. `ANNOY` or `FAISS` (for indexing vectors)*
        *   *geohashing (only for for 2d space)*
*   Neural Networks for NLP (optional)
    *   Transformers & Muppet models
*   Capstone Project
    *   Kaggle Avito (or new project?)
        *   MUST use word vectors
        *   MUST also use TF-IDF or edit / lev distance
        *   Images not necessary
    *   Presentation to group as usual
*   ~~Linguistics~~
    *   ~~Grammar and syntax parsing (CFGs, CYK)~~
    *   ~~Semantics~~
    *   ~~Polysemy / metonymy (word sense disambiguation)~~
    *   ~~Semiotics (e.g. emoji)~~
    *   ~~Morphology~~
    *   ~~Ontology~~
*   ~~Machine translation~~
    *   ~~IBM models~~
    *   ~~Back-translation~~
    *   ~~Syntax-based SMT~~
    *   ~~Corpus alignment / crawling / creation~~
    *   ~~Word vector alignment (e.g. Procrustes)~~
*   ~~Hyperbolic / elliptic embeddings~~
*   ~~Information extraction / relation extraction~~
*   ~~Question answering~~
*   ~~Summarization / simplification~~
*   ~~How do CRFs work (used for NER tagging)~~
*   ~~Byte pair encoding and subword tokenization (e.g. sentencepiece)~~
*   ~~Spelling / grammar correction~~

##  [Automatic Speech Recognition](./Automatic Speech Recognition/README.md) (1 month)

*   Fundamentals of Speech Recognition (Stanford CS224S Lecture 1)
*   Language Modelling (Edinburgh)
    *   Lexicon and language model
*   Acoustic Modelling and Decoding
    *   HMM, forward-backward, and Viterbi (Stanford CS224S Lecture 3)
    *   Word error rate, training, and advanced decoding (Stanford CS224S Lecture 4)
        *   How to weight the AM and LM
        *   Viterbi beam decoding
        *   Multi-pass decoding e.g. N-best lists, lattices, word graphs, meshes / confusion networks
        *   Finite state methods
    *   GMM acoustic modelling and feature extraction (Stanford CS224S Lecture 5)
    *   Neural network acoustic models in speech recognition (Stanford CS224S Lecture 7)
*   End-to-End Neural Network Speech Recognition (Stanford CS224S Lecture 8) (optional)
*   Kaldi Tutorial
*   SAGE Tutorial (this will be imported into Confluence because it can’t be put on GitHub)
