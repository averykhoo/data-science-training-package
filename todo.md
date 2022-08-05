# TODO

(split off from main readme to reduce clutter)

## Future Plans

* [x] split up the syllabus and the curriculum for this package (this makes it easier to look for new and better
  materials, and to make updates to the curriculum, while at the same time making sure the scope of the training package
  doesn’t drift too much as stuff is added or removed)
  * [x] the [syllabus](syllabus.md) notes down things that need to be learned and outcomes that should be achieved
  * [ ] the curriculum collates and orders the material needed to cover the syllabus
* [ ] cover deep learning in the ML module in a bot more depth
* [ ] update ASR
* [ ] notes on timeseries data
  * fb prophet
  * changepoint detection
  * model / data drift, and how to detect it
  * how to split training and test sets (and how NOT to)
    * split by time (or in some cases, some other time-dependent variable)
    * splitting randomly leaks labels into the training set
      * remember that near-100% results are suspicious
  * 

### Excessively long list of resources we can consider for inclusion

* [deep learning specialization course](https://www.deeplearning.ai/deep-learning-specialization/) (free to audit)
* [google ML crash course](https://developers.google.com/machine-learning/crash-course)
* [glossary](https://developers.google.com/machine-learning/glossary/)
* [rules for ML](https://developers.google.com/machine-learning/guides/rules-of-ml/)
* [how to work with users](https://pair.withgoogle.com/guidebook/)
* [technical debt in ML](https://ai.google/research/pubs/pub43146)
* [wizard of oz models](https://medium.com/google-design/human-centered-machine-learning-a770d10562cd)
* [see sidebar for titanic walkthroughs](https://techdevguide.withgoogle.com/paths/machine-learning/sequence-2/kaggle-competition-titanic/#!)
* [10 rules for better Jupyter notebooks](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007007)
* [Elements of Statistical Learning (book)](https://web.stanford.edu/~hastie/Papers/ESLII.pdf)
* [Data Science and Machine Learning: Mathematical and Statistical Methods](https://people.smp.uq.edu.au/DirkKroese/DSML/)
  * [with associated Python code](https://github.com/DSML-book/)
* Unicode
  * [Joel Spolsky’s article on Unicode](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)
  * http://reedbeta.com/blog/programmers-intro-to-unicode/
  * see also [grapheme](https://github.com/alvinlindstam/grapheme), which is a library for working with what you
    probably think are unicode characters
  * see also [wcswidth](https://github.com/jquast/wcwidth), which gives you the length of a string, double-counting CJK
    characters since those are double-wide