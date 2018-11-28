---
title: Intro
nav: true
---

# Introduction -- Tokenization, Lemmatization, and Stemming 

In order to do any sort of textual analysis, a computer needs to "tokenize" the text being analyzed. What that means is that the text input into the system is broken down into tokens, the smallest of which are words. Tokens are also made of the sentences and any other structures required (3 word phrases, paragraphs, etc.). 

Often the phase "bag of words" is used to describe this process. These words/tokens, however, can be further atomized via lemmatization and/or stemming, which are similar processes. Stemming is the "cruder" of the two, as it simply chops off the ends of a word to make sure it matches all words that derive from the same stem. 

So, for instance all these words: driver, drivers, drive, driven, driving, via stemming, would be represented as "driv." The problem, however, is what then to do with the word "drivel." 

Lemmatization is the answer, as this process attempts to recover the base, or dictionary form of a word, e.g. "drive," and then connect all the other words with that word. Another example: am, are, is --> b. 

(The above example and much of this summary comes from [Introduction to Information Retrival](https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html), which can be found via the pages of the [Stanford Natural Language Processing Group](https://nlp.stanford.edu/).)

## the Bags of Words, or, Don't Fear Word Clouds

Word clouds demonstrate the basic function of textual analysis quite succinctly. Every tool we'll look at today includes some type of word cloud. There are also many tools online that will produce word clouds from various sources. 

[Wordle](http://www.wordle.net/) helped to make Word Clouds prominent but the technology it used to create the word clouds is no longer supported by most browsers. 

One online word cloud creator we often use is [TagCrowd.com](https://tagcrowd.com/). You can see these clouds in many of our digital collections to provide an overview of the collection and a browsing mechanism. 

{% include figure.html img="tagcloud-hjccc.png" alt="tag cloud from the Historical Japanese Ceramic Comparative Collection" caption="A word cloud from the <a target='_blank' href='https://www.lib.uidaho.edu/digital/hjccc/subjects.html'>Historical Japanese Ceramic Comparative Collection</a>" width="75%" %}

## WORK TIME! 

{% capture text %}
Go to [TagCrowd.com](https://tagcrowd.com/) and visualize your own content or the <a href="../data/sonnets-text.txt">plain text version of the Shakespearean Sonnets</a> we've provied. Mess with some of the settings and the stop words to generate a few different clouds.
{% endcapture %}
{% include alert.md text=text color=secondary %}

# Word Tree

Word Trees help you track usage across a document and can uncover particularly interesting patterns connected to individual words. 

Jason Davies' [Wordtree](https://www.jasondavies.com/wordtree/) is particularly useful for first visualizing a document. He provides a number of documents to start, including a couple Obama speeches and The Cat in the Hat. The token here is essential a three word phrase (connected to every other three word phrase).

{% include figure.html img="dylan.png" alt="Word Tree of Bob Dylan's Blowin' in the Wind" caption="<a target='_blank' href='https://www.jasondavies.com/wordtree/?source=blowin.in.the.wind.txt&prefix=How'>Word Tree of Bob Dylan's Blowin' in the Wind</a>"  %}

You can paste in your own text as well.


## WORK TIME! 

{% capture text %}
Go to [Wordtree](https://www.jasondavies.com/wordtree/) and visualize your own content or the <a href="../data/sonnets-text.txt">plain text version of the Shakespearean Sonnets</a> we've provied.

Hold shift down and select different words within the document to explore various connections. 
{% endcapture %}
{% include alert.md text=text color=secondary %}

