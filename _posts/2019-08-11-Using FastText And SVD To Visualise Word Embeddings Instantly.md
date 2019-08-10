---
published: false
---
Man->King. Woman->Queen. (?!)

When I began with the basics of Natural Language Processing a while back, I was fascinated by the way in which words were represented as vectors. Even more enthralling was words being plotted on a graph with those having similar meaning and context grouped together. So, I struggled with generating my own embedding and it was a " struggle " because of the lack of computation power I had. Word2Vec for generating vectors and T-SNE for visualising were popular choices but took a lot of time with the resources I had.
Well, that has not changed till now. However, I came across Facebook's fasttext that blew me away. It takes seconds to do things which used to take hours earlier with almost same performance results. In addition to that, I used some linear algebra to find out the way which is perhaps the " fastest " to generate your own word embedding visualisations. Let's dive right into the process now and write some code.

## 1.Getting the data
I decided to take chat data from Whatsapp. I took up the data of The Literary And Debating Club (LDC) of my college. This is because we have blabbered there on a wide range of topics and also the data amounted to nearly 1.1 Mb which was good enough for the task.
## 2. Some Pre-processing
There were some issues that needed attention. First, there were phone numbers of people at the beginning of each new line if there contact name was not saved. Also, there were weird special characters that represented emoticons in the chat but were a headache for our task. So, I used some Regular Expression tricks to clean the text.

## 3. Setting up FastText
Let us now move onto the big guy. Getting Facebook's FastText set up is a piece of cake. All you need is a modern C++ compiler (C++ 11) followed by a make command. FastText is written in pure C++ which is another reason for its insanely quick implementation.
a. Go to https://github.com/facebookresearch/fastText and clone the repo.
b. Switch to the downloaded directory and type make command on your terminal
c. Voila! FastText is ready to use.
4. Using FastText on our Data
We shall now use the fasttext library to generate word vectors for our cleaned data. To do so, open up your terminal in the fasttext directory and type-
'''./fasttext skipgram -input ldc_clean.txt -output model'''
Let me break down that statement down for you.
./fasttext - Use the fasttext module we just compiled a step back, duh?
skigram - There are two popular methods to generate vector representations of words. CBOW and Skipgram. We choose skipgram here.
-input ldc_clean.txt - We specify as the input argument our file name that contains text data.
-output model - This specifies the name with which FastText will generate our two output files. model.vec is a text file containing the word vectors, one per line. model.bin is a binary file containing the parameters of the model along with the dictionary and all hyper parameters
## 5. Setting up python lists from the generated model.vec
We now have our words and vectors in a .vec file but in order to plot them and also to perform SVD on the vectors, we need to convert the words to a list and the corresponding vectors to another list. Along the way, we also need to convert vector values from string to numpy's float32 type to allow the above said operations.


## 6. Using Singular Value Decomposition to reduce dimensions.
When I googled around for the first time, I found T-SNE being used everywhere to generate some amazing visualisations by reducing dimensionality. No doubt, I am a big fan of it. But sadly my computation power isn't. So, I decided, why not use the good old SVD. It worked like a charm. It als o contributed to the whole point of using FastText in the first place, that is, giving real quick results.



## 7. The fun part. Plotting our data to create insightful visualisation
Now, we have everything we need. A nice list that has all words and a wonderfully reduced representation our originally high dimensional vector representation, courtesy, SVD. All we got to do now is use Matplotlib and generate some visual awesomeness.



That right there folks, was perhaps the quickest way you'll ever find to take a raw piece of data, train it in seconds to generate vector representations of words using Facebook's FastText and then do a bit of Linear Algebra magic to get the visualisations up in absolutely no real time.
I plan to release a post explaining all the mathematical intricacies that lie under the hood. It will deal with how FastText achieves SOTA results in such little time and what helps it to beat the existing competition like Word2Vec , especially in terms of training time. So, if you liked this you will surely love that. So, stay tuned and keep embedding!

![Debate night?](https://cdn-images-1.medium.com/max/1200/1*YQ92Vbw2NSwh70nDR8P7VQ.png)

Who's up for a debate night?P.S - The image is highly zoomed in because of the extremely dense nature of the visualisations. Use matplotlib's zoom feature to do that.