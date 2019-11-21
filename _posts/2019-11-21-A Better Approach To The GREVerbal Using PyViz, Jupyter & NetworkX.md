---
published: true
---

*Bye Bye boring excel sheets, hello interactive colorful networks!*


![The GreVisualizer](/images/gre_ft.PNG)

>The GreVisualizer!

You have your GRE General Test in 10 days. The scores of this test will play a crucial role in deciding the graduate school you get accepted to. You are tensed. You are cramming those high frequency words but your brain is now saturated. I was in this very situation around a month ago when I was preparing for my GRE.
There must surely be a better way to do this, I thought to myself. A more interactive and visual method could be applied. Humans retain visuals and sounds for much longer than simply plain text. I had an Excel sheet that I had populated during my preparation. This had two sets of words. One set consisted of synonyms while the other had words that were commonly confused. Ingenuous and Ingenious. The Excel sheet was an ingenuous approach, I need an ingenious one.

![This is fun!](/images/excel.PNG)

>This is mundane, bleh



![This is mundane, bleh](/images/fun.PNG).

>This is fun!



I decided to model these groups of words as networks in a graph. In case of synonyms, the central node would be the meaning of the word and all words with that meaning would be attached to it. In case of commonly confused words, they'd all be connected and if you were to hover over the nodes, you'll get their meanings. I used pyViz and NetworkX to model these graphs from my raw Excel file.
All was going good until this point and I was very excited to share this visualizer. I had one major problem though. How do I put it out to the public? The output that I generated from my python code in a Jupyter notebook was an interactive HTML file. I couldn't find a good way to share that for free on the Internet. I mulled over this problem and had reached an impasse, until…

![Pydata](/images/nyc.jpg)

>PyData NYC, 2019!

I was seated at the Fifth floor of Microsoft Convention Center, New York, attending a tutorial. The tutorial was titled Swiftly turn Jupyter notebooks into pretty web apps. It was an informative and captivating session. I walked away with multiple possible solutions to my Visualizer deployment problem.
Once I came back to India, I started working on it. I wanted the User Experience to be seamless and to focus primarily on exploring the graph and not stress on the underlying code. To do that, I used RISE by Jupyter to first convert my notebook to slides (Yes!). This made it much more friendly for someone who had no interest in the code and was here just for the words! I also wanted zero setup time and effort for the end user. To achieve this, I used Binder to deploy my notebook. After that, I simply put the Binder logo on my Github repository, made a walk-through demo GIF and shared it with my network!

![Demo!](https://github.com/arrayslayer/theGREvisualizer/raw/master/demo/demo.gif)

> Here's a demo!

There's is a lot that can still be done in this project. Some features include ability of user to add new links, to search words, and to make questions from the database of words. This is the reason why I have open sourced the code and I would encourage anyone who is interested to help contribute to it. You can try the visualizer out and even contribute to it, if you want, [here!](https://github.com/arrayslayer/theGREvisualizer).
