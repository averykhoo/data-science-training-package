#   Syllabus

*   New syllabus (revised on 2019-11-05), converted from word doc
*   "Appreciate the existence of" means:
    *   Know that this thing exists and roughly what it does
    *   But it's not necessary to know how or why it works


##  Foundation Module (1 week)

*   Mathematics
    *   Basic linear algebra
    *   Basic probability and statistics (including Bayes’ Theorem)
*   Programming
    *   Markdown
    *   Git
    *   Python 3 and regex
        *   Google’s Python Class
        *   Official Python Tutorial 1 to 8, 9.8 to 9.10 (for officers without Python knowledge)
        *   Do we want to give an exemplar regex cheat sheet?
    *   Unix tools and scripting
        *   CS2043 lectures 1 to 8
    *   Basic SQL
        *   How to use oracle’s XML tables
        *   Kaggle’s SQL tutorial?
        *   Use SQLite since it’s easier to play with? Or use some oracle DB?
    *   Joel Spolsky’s article on Unicode
    *   Avery’s comments on code style:
        *   Pls give important variables names that describe what they are
        *   Pls break your code into logical chunks (ideally, reusable functions / classes)
        *   Pls use a code formatter (any formatter)
        *   Pls provide type hints for core algorithmic functions
*   Distance Measures
    *   Fixed-length vectors
        *   Manhattan / Euclidean distances
        *   Hamming distance
        *   Cosine similarity, dot product
    *   Variable-length strings
        *   Edit / Levenshtein distance (longest common subsequence)
        *   BLEU score
        *   *Appreciate the existence of:*
            *   Edit distance backtracking
            *   METEOR
            *   ROUGE
            *   Damerau-Levenshtein distance
    *   Variable-size sets
        *   Jaccard similarity (intersection over union)
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
*   ~~Less-common string algorithms~~
    *   ~~Longest common substring~~
    *   ~~Sequence alignment / warping~~
    *   ~~Multiple string search (e.g. Aho Corasick)~~
    *   ~~Fuzzy string matching~~


##  Machine Learning (1 month)

*   Supervised Learning
    *   Regression
        *   Linear, ridge, lasso
        *   Logistic
    *   Classification
        *   KNN
        *   Support vector machine (linear SVM for binary classification)
        *   Decision trees
    *   Ensemble
        *   Boosting (e.g. XGBoost, LightGBM)
        *   Stacking
    *   Metrics
        *   Confusion matrix
        *   Recall, precision, F1 score
        *   AUC & ROC curve
        *   Micro and macro averaging
        *   How to choose a threshold
    *   Optimization
        *   Loss function
        *   Bias / variance trade-off
        *   What is over-fitting and under-fitting
        *   Regularization
        *   Cross-validation, hyperparameter tuning
*   Unsupervised Learning
    *   Clustering
        *   K-means
        *   EM GMM
        *   Density
        *   Hierarchical
    *   Anomaly detection
        *   Parametric
        *   Non-parametric
    *   Topic modelling
        *   LSA (or NMF; these are kind of based on factorization)
        *   LDA (based on generative models)
    *   Frequent itemset mining
*   Reinforcement Learning & Genetic Algorithms
    *   Know that they exist and *appreciate their existence*
    *   Why they are different from supervised / unsupervised
    *   And BTW we don’t use or need them (yet)
*   Neural Networks (still work in progress)
    *   Backpropagation
    *   Deep neural networks
        *   Feedforward
        *   CNN, pooling, cross-entropy, softmax
        *   RNN, LSTM
        *   Dropout
*   Tutorials Capstone Project
    *   Pandas
    *   Visualization (charts & graphs)
    *   Titanic with walkthroughs
        *   Optional for those who have done it before
        *   Data exploration and data cleaning
            *   Dealing with missing values
            *   Finding and fixing outliers
        *   Featurization
            *   Categorical to one-hot encoding
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
    *   ~~Recommendation systems~~
*   ~~KL / JS divergence~~
*   ~~Time-series data~~


##  Natural Language Processing (1 month)

*   Text Preprocessing (NLTK)
    *   Tokenization and segmentation (and what is an n-gram)
    *   Stemming and lemmatization
    *   POS tagging
    *   Bag of words / bag of n-grams
*   Word Embeddings (deeplearning.ai)
    *   Word Mover’s Distance
    *   *Please appreciate the existence of:*
        *   Sentence / document embeddings (e.g. doc2vec, Google’s USE)
        *   Cross-lingual embeddings (e.g. RCSLS, LASER)
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
        *   Beam
        *   Viterbi
    *   No need to go into CRFs
*   Information Retrieval and Ranked IR (Stanford NLP)
    *   Inverted index
    *   TF-IDF
    *   *Appreciate the existence of:*
        *   Locality sensitive hashing (e.g. minhash vectors)
        *   Variants of TF-IDF (SMART IR system, Okapi BM25)
        *   ANNOY or FAISS (for indexing vectors)
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

##  Automatic Speech Recognition (1 month)

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
