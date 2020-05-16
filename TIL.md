A daily log of little things I learn pertaining to Computer Science and AI/ML.
(Inspired by [Seth Godin](https://seths.blog/))

## 16/5/20

* N/A

## 15/5/20

* N/A

## 14/5/20

* Use %env magic command in jupyter to set environment variables.

## 13/5/20

* Started learning about active learning with [this introductory article at DataCamp.](https://www.datacamp.com/community/tutorials/active-learning)
* Came across this active learning library called [AlpacaTag](https://github.com/INK-USC/AlpacaTag) which allows UI based annotation too

## 12/5/20

* To insert a dict into sql table, best way for now seems to be putting in a string and then use ast literal eval after retreiving it.

## 11/5/20

* Came across text matching using deep learning library called [deepmatcher](https://github.com/anhaidgroup/deepmatcher)
* Found the easiest way in sublime to fix space and tab indentation issues in python.


## 10/5/20

* Went through the [Pytorch 60 minutes blitz](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html).

## 9/5/20

* Attented Milind Tambe's (Google Research, AI For Good) webinar to learn about their projects. Super interesting problems!

## 8/5/20

* Submitted my first paper abstract!

## 7/5/20

* Came across this new time zone called Anywhere On Earth, which is the most lagging time zone, ie, everyhwere else the day is completed before this time zone completes their day!

## 6/5/20

* Learnt about [literal_eval](https://kite.com/python/docs/ast.literal_eval) in python for interpreting and parsing strings as python commands!
* Used [fuzzyset](https://pypi.org/project/fuzzyset/) for the first time.

## 5/5/20

* N/A

## 4/5/20

* Listened to [this Self Explaining AI discussion](https://podcasts.google.com/?feed=aHR0cHM6Ly9kYXRhc2tlcHRpYy5saWJzeW4uY29tL3Jzcw&ep=14&episode=OWI2NDY2MjgtNTllZC00YjU1LTg4MTUtZjVhMWNiZGJjNzdm). Very interesting idea.


## 3/5/20

* [Passing variable into bash(!)](https://stackoverflow.com/questions/35497069/passing-ipython-variables-as-arguments-to-bash-commands) command in Jupyter.

## 2/5/20

* N/A

## 1/5/20

* N/A

## 30/4/20

* [Easy progress bar for any pandas apply operation](https://stackoverflow.com/questions/18603270/progress-indicator-during-pandas-operations). Anxiety Saver!


## 29/4/20

* Finally used ravel() in real life.
* Get only idf from tfidf vectorizer in sklearn using _idf attribute

## 28/4/20

* Send one hot labels in OneVsRest to make it multi label.

## 27/4/20

* Famous papers have shady experiments and even shadier implementations.
* Simply used nlp("Sentence...").vector in SpaCy to get consistent dimensions embeddings for any sentence!
* Learnt that [sklearn does a linear normalization](https://stats.stackexchange.com/questions/374913/summing-predicted-probabilities-from-logistic-regression-using-one-vs-rest) (not softmax!) of all output probabilites

## 26/4/20

* [Chapter 2](https://course.spacy.io/en/chapter2) of the Advanced NLP with SpaCy course.
* The importance of constraints while working on a problem. Read [How can Data Scientists survive layoffs?](https://peadarcoyle.com/2020/04/26/how-can-data-scientists-survive-layoffs/)

## 25/4/20

* N/A

## 24/4/20

* Used [Count Vectorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html) for the first time. And understood it.(Two very different things!)
* Started with [this Adv NLP with SpaCy](https://course.spacy.io/) interactive course!

## 23/4/20

* Used "Convert to Smart Art" in powerpoint for first time. Handy life hack!
* Reminder that PCA is deterministic as no parameters.

## 22/4/20

* Used Solr for the first time.
* Made changes inside a library's code which makes me wonder how 99% of work is understanding the code and 1% is adding your stuff in it.


## 21/4/20

* [Setup remote local sftp on Sublime](https://medium.com/@daniwhkim/remote-ftp-sftp-with-sublime-de7d71a2b400). Life gets simpler!
* Wrote the first functional test of my life. Hard work!


## 20/4/20

* Symlinks! Used Symlink in [Jupyter](https://cyberhelp.sesync.org/faq/how-to-create-a-symlink-to-research-directory-in-Jupyter-lab.html) to get another folder in sidebar to access files on server. So, neat!
* Learnt why people simply do not use one hot econding instead of embeddings in text models -> High dimensionality!

## 19/4/20

* Discovered [LALE](https://github.com/IBM/lale) library by IBM for semi automated Data Science workflow.
* Read Chapter 1 of the [Causal Reasoning Book](https://causalinference.gitlab.io/causal-reasoning-book-chapter1/). Coming to this after reading The Book Of Why and wanting a more machine learning oriented resource. Aim to use Causal Reasoning as aid to Machine Learning Interpretability.

## 18/4/20

* N/A

## 17/4/20

* Used Multioutput classification for the first time

## 16/4/20

* Used tf-idf irl for first time.
* Read about [dataset shift](https://www.analyticsvidhya.com/blog/2017/07/covariate-shift-the-hidden-problem-of-real-world-data-science/)

## 15/4/20

N/A

## 14/4/20

* Realized that I should brush up on SQL and not resort to doing everything via pandas.
* Found this new pandas function to stack columns down. [pd.stack](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.stack.html)

## 13/4/20

* Ctrl+Shift+P and then clear cell output to clear the output of a current Jupyter cell
* Found this [spelling correction library](https://github.com/wolfgarbe/SymSpell)

## 12/4/20

* Read this [new paper](https://arxiv.org/abs/2002.11097) that highlights the problems in using Shapely values for feature attribution.
* Got mind blown by Microsoft's Power Point's [enhanced design recommendations](https://www.microsoft.com/en-us/microsoft-365/blog/2019/06/18/powerpoint-ai-upgrade-designer-major-milestone-1-billion-slides/)!

## 11/4/20

* Went through [Stanford's Karel Bot](https://compedu.stanford.edu/karel-reader/docs/python/en/chapter1.html)which used to teach Intro to programming at Stanford. So neat!

## 10/4/20

* If stuck between too many little fixes, just start all over again! Far more efficient.
* Discovered Google's [diff_match_patch](https://github.com/google/diff-match-patch) to find diff, match and patch (:P) text.
* Appreciating the need to write quality generalised tests for modules! Avoid hard coding as much as you can.

## 9/4/20

* To get to end of line in VI, command mode then $
* PDFs can be opened in Jupyter Lab!
* Discovered [this](https://explosion.ai/demos/displacy) cool application of what we learned in Compilers course !
