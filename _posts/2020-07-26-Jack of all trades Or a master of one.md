---
published: true
---
*No, AI is not going to take your job (yet)*

The hype is real. Cherry-picked results in 30 second videos lead us to believe that Skynet is here. People are running around to apply the latest State of The Art models
for each and every business use case. Unfortunately, we are not there yet.
 <br />
 <br />
 <br />
![Sentiment](/images/sentiment.png)

*Pretty contradictory :)*
<br />
<br />
<br />

**Do you use generalised models that have been trained over billions of data points
and seek to solve for multiple tasks. Or, do you use deterministic methodologies to solve specific problems. The latter seems to work better in real life.**
The idea of companies like Google and DeepMind releasing trained models with billions of parameters to help one in multiple downstream task does not
seem to scale well with real world data.
Take for example, a task to detect occurences of currency in a statement. You may want to use the best Entity recognition NLP models to do that for you.
And they might work for some of your cases. But they will not work for others. The point is, these are too brittle. A dangling comma or a full stop, or just
a rephrasing of the sentence, makes them fail. They are built to do a lot of things. But they are not built to do any of those things very well. You might
be better of by writing a regular expression to capture monetary entities or just searching for certain keywords.
<br />
<br />
<br />

![Works](/images/NER_success.png)
*This works as the ORG entity is detected for Apple.*
<br />
<br />
<br />

![Fails](/images/NER_fail.png)
*But this does not. We come up empty after a simple restructure*
<br />
<br />
<br />

My ML professor at college told me once, " The best way to do ML is to not do it." 
<br />
Sounds about right. Use it as a last resort rather than your first shot.
You do not use a sword to knit a scarf. Use your needles, please.

*The examples are taken from State Of The Art models hosted at Allen NLP. You can try out for yourself at https://demo.allennlp.org/named-entity-recognition*

<script src="https://utteranc.es/client.js"
        repo="arrayslayer/arrayslayer.github.io"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
