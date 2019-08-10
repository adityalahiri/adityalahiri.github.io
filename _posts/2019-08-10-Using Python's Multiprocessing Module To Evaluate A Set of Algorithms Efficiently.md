---
published: true
---
## Use all your cores, now!

Sometimes, your first intuition after seeing a dataset is to think of more than one algorithm that would probably work well on it. You would then naturally want to try them all out and see how they fare against one another on the baseline results. But there's one factor that always makes you rethink that decision. The factor of time. So, how do we get around it? Let us try multiprocessing.
A process is a unit of work in your computer. In terms of python, you can think of a process to be an instance of a program (e.g. Jupyter notebook, Python interpreter, a standalone script). Your operating system is capable of running multiple processes at a time and you can map processes to the number of cores you have in your system. If you have multiple cores, which you most likely do, you can run more than one process parallelly at the same time on different cores.
The problem at our hand is to evaluate multiple algorithms on the same dataset, get their metrics and see which performs best. This is very well suited to be run on distributed cores easily. This is because each of them is independent of the other. That is, a Random Forest train and test run does not care about intermediate results of an SVM train test evaluation. Hence, we can simultaneously run them on different cores and get results much quicker instead of running them one by one on a single core.
Unfortunately, python code by default runs as a single process on a single core. Fortunately, it is possible to easily make your code run parallelly and exploit all your CPU cores using the in-built multiprocessing module. Let us now get down to the code and see how things work.
Use them all! (Image Source:Vindictus)Assume we already have our train and test data split and ready to be used just as in the regular machine learning pipeline. We also have a function find_rmse(reg) that takes in a regression algorithm function of sklearn and uses it to train and then subsequently test on the datasets and deliver the mean root mean squared error we obtained. The problem is a supervised regression problem and we want to see the results of four algorithms, namely, Random Forests, nuSVM, Ridge Regression and ElasticNet on the same dataset.

```
def find_rmse(reg):
   
    df_train = pd.read_csv('/independent_train.txt', header=None)
    df_test = pd.read_csv('/independent_test.txt', header=None)

    X_train = df_train.drop([df_train.columns[0], df_train.columns[-1]], axis=1)
    y_train = df_train[df_train.columns[-1]]

    X_test = df_test.drop([df_test.columns[0], df_test.columns[-1]], axis=1)
    y_test = df_test[df_test.columns[-1]]

    reg.fit(X_train, y_train)

    y_out = reg.predict(X_test)

    error = np.sqrt(mean_squared_error(y_test, y_out))
                                
    print(str(error)+ repr(reg)[0:4]) #using repr to get initials of the name of the classifier that this run used
  
```

First, we will import the Pool function from the multiprocessing module. The Pool object offers a convenient means of parallelizing the execution of a function across multiple input values, distributing the input data across processes. It takes one argument, which is equal to the number of worker processes you want to spawn. You can keep this equal to the number of cores in your CPU for maximum utilization. Bear in mind, however, that since all of them will mostly be used by this python program, you might not be able to do another processor heavy work on your system while the program executes.

```
from multiprocessing import Pool
```

Then let us create a list of the regressors we want to compare our results on. Our work is very convenient since python can take functions as arguments for functions.



Now, let us map our function that calculates the rmse after training the model using a regressor and testing it, to our list of regressors. This will pass these list of regressor functions to our parent function find_rmse(reg) parallelly!

```
pool.map(find_rmse,regressors_list)
```

Finally, let us bury the remains of our Pool object.

```
pool.close()
pool.join()
```

Voila! We just substantially minimized the time that we would have needed to compare so many regression algorithms. If you do this at scale, which I am currently doing as a part of my research project, it is a difference of days and months that we are talking about. I have a system with 64 CPU cores and using them all helps me achieve this exponentially quicker. But without using this technique, those 64 cores would have just gone to waste. Even your personal machine would usually have >4 cores so you can use this technique to get a substantial speed up as well. Have a happy time parallelizing your learning!
