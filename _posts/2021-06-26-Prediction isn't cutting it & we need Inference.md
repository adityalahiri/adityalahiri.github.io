---
published: true
---
*Prediction != Inference*

For a long time, I used to employ the words "Prediction" and "Inference" interchangeably. I still do sometimes. Heck, industry leaders like [Microsoft](https://azuredata.microsoft.com/articles/ebd95ec0-1eae-44a3-90f5-c11f5c916d15) do it.
But I think now we need to accept that there is a clear demarcation between the two. Let's see what the folks who wrote *An Introduction To Statistical Learning* 
have to say about this.

" When you are interested in simply predicting the value of y given X, then this is a prediction problem. On the other hand, if you want to see how y
is affected by a change in X then you are performing inference"

In both these cases, you estimate a function f(X) that yields the y. However, the intention for doing so is different in both cases. In a prediction mindset,
you do not care if this f(X) is a black box and you do not care about the internal working of the function, as long as your predictions are satisfactory. However,
in an inference setting, you care about how the Xs caused your y to reach a certain prediction value.

With machine learning and deep learning models penetrating critical areas of life such as judicial systems and healthcare, moving from a blind system of high
accuracy predictions to a explainable system of inference is gaining ground. This shall also pave the way for responsible and ethical AI, once we know what our models
are up to!

More power to inference! It is certainly not elementary, Dear Watson :)
