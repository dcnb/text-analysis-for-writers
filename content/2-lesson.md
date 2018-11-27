---
title: Voyant
nav: true
layout: full
---

# [Voyant Tools](https://voyant-tools.org/)

Voyant Tools is an extremely powerful and modular online toolset for visualizing one or many documents. It works particularly well across a number of documents, and we will be exploring some of those capacities here. We will be adapting the [tutorial materials](https://voyant-tools.org/docs/#!/guide/tutorial) supplied by Voyant-Tools help pages: 

We tend to view workshops on Voyant as serving two purposes:

1.  how to use Voyant and get a grasp on what's available (how to use it)
2.  how to think differently about texts with tools such as Voyant (why use it)

## Basics of Voyant

The [About](https://voyant-tools.org/docs/#!/guide/about) page contains a useful introduction to Voyant: what it is, who has contributed, and some of the core design principles. It's worth reading as time permits.

Some points on Voyant

*   Voyant Tools fits in a long tradition of humanities scholars building tools for reading, finding, analyzing and visualizing digital texts.
*   Voyant Tools strives to lower the barrier of entry for text analysis and balance user-friendliness with powerful functionality. For instance, no installation or login are required, and you can work with texts in a wide variety of formats (plain text, PDF, XML, MS Word, RTF, etc.).
*   Voyant Tools is open-source and is a work in progress, it may not always work as intended and it's best to approach all observations with some circumspection.
*   Voyant Tools has the advantage of being able to work with almost any language (represented in Unicode) but has the disadvantage that it has almost no language-specific functionality (needed for things like semantic analysis).
*   Voyant Tools is intended as a tool for exploration and to assist with interpretative practices, it is not intended to tell you what questions to ask or to provide irrefutable results, though you may notice some interesting things and you may be led to construct some compelling interpretations while using it.

Ok, that's all somewhat abstract and conceptual, let's jump into using Voyant.

## Create a Corpus

There's more detail in the [Creating a Corpus](https://voyant-tools.org/docs/#!/guide/corpuscreator) page, but there are four main ways of creating and using a corpus in Voyant ("corpus" is another word for a set of documents):

1.  open an existing corpus (click on the "Open" button under the text box)
2.  type or paste text into the main text box (this creates a corpus with one document)
3.  type or paste one or more URLs into the main text box (one URL per line)
4.  click the "Upload" button under the text box to use files from your computer

Take a moment to try each kind of corpus source (open, text, URLs, upload) in the box below (or in a [new window](https://voyant-tools.org/)).

<iframe src="https://voyant-tools.org/" style="width: 90%; height: 520px;"></iframe>

Some tips:

*   typing or pasting text into the box is ok for shorter documents, but for longer documents it's probably best to upload a file
*   when you upload files you can select multiple files at a time
*   if you have several local files to upload, consider creating a zip archive first, then upload just that file
*   URLs need to be visible to the Voyant server (not behind a firewall) so the contents can be fetched
*   some servers (like Gutenberg) may limit the number of requests, which could cause URLs to behave sporadically
*   it can take a while to fetch a long list of URLs, it's probably preferable to use another tool to download the files (or download them manually) and then upload them in a zip archive
*   uploaded plain text files need to be in UTF-8

If an error occurs during corpus creation you may see an error message appear. Unfortunately, sometimes the system just fails silently (especially if you're creating a big corpus and there's a server timeout). One advantage of using a local instance of VoyantServer is that you may see some helpful errors reported in the VoyantServer window.

Voyant can be used with a corpus of variable size, from one document to many. Some of the functionality depends on multiple documents and some tools work less well when there are hundreds or more documents.

It's good to think of a corpus as a fluid concept, you may be able to change the meaning as you proceed. For instance, if you have thousands of tweets, you could treat each one as a separate document, or combine tweets by time, by author, or by some other criteria. Sometimes you might want to edit a corpus or sometimes you might want to create a new corpus for comparison.

We won't experiment for now with more advanced options for Corpus creation, but there are several [options](https://voyant-tools.org/docs/#!/guide/corpuscreator-section-options) available to tweak the processing of text, XML, and even spreadsheets. 

## Explore a Corpus

Once you create a corpus you will arrive at the default "[skin](https://voyant-tools.org/docs/#!/guide/skins)" or arrangement of tools. There is a lot happening at once, but we'll start by describing the tools that you see and how they can interact.

### Default Skin

At first you will see three tool panels along the top and two tool panels along the bottom:

*   [Cirrus](https://voyant-tools.org/docs/#!/guide/cirrus): a kind of word cloud showing the most frequent terms
*   [Reader](https://voyant-tools.org/docs/#!/guide/reader): an efficient corpus reader that fetches segments of text as you scroll
*   [Trends](https://voyant-tools.org/docs/#!/guide/trends): a distribution graph showing terms across the corpus (or terms within a document)
*   [Summary](https://voyant-tools.org/docs/#!/guide/summary): a tool that provides a simple, textual overview of the current corpus
*   [Contexts](https://voyant-tools.org/docs/#!/guide/contexts): a concordance that shows each occurrence of a keyword with a bit of surrounding context

<iframe src="https://voyant-tools.org/?corpus=austen" style="width: 90%; height: 500px;"></iframe>

### Tool Interactions

An essential part of Voyant is that events in one tool can cause changes in other tools (the exact interactions depend on a number of factors, including which tools are visible). For instance, try the following sequence in the window above:

*   click on a word (like "know") in Cirrus, the tool in the upper left
*   notice how the Trends tool (upper right) now shows just the word you clicked
*   click on one of the discs in the Trends tool
*   notice that the Contexts tool (bottom right) has updated with just the clicked word
*   click the first row of the Contexts tool (bottom right)
*   notice how the Reader tool has jumped to a location where that word appears, highlighted

### Cirrus

<iframe src="https://voyant-tools.org/tool/Cirrus/?corpus=austen" style="width: 500px; height: 300px; float: right; padding-left: 1em;"></iframe>

Now let's zoom in for a moment on Cirrus. We might ask ourselves several questions about what we're seeing. For instance, what does size represent? What about colour? What about the placement of words? This is a text in English but the most commonly occurring words aren't there (like "the" and "a"), why not? For a tool like Cirrus some of these questions may be obvious, but for **all** tools it's good to continuing asking ourselves what we're seeing, what we're not seeing, and why.

### Options
{% include figure.html img="cirrus-options.png" alt="Word Cloud options from Voyant Tools" caption="Word Cloud from <a href='https://voyant-tools.org/'>Voyant Tools</a>"  %}

Some options in Cirrus (like other tools) are available directly within the tool panel, like the "Scale" button and the "Terms" slider (experiment with both of these to see what they do). Other options are accessible from the options dialog that appears when you click on slider in the grey bar of the tool (like the image to the left). The full list of options are described in the [Cirrus](https://voyant-tools.org/docs/#!/guide/cirrus-section-options) documentation page, but let's have a quick look at the Stopwords option by clicking the "Edit List" button. 

This will show a dialog box with a long list of words that are excluded from the top frequency words in Cirrus. These are generally "function" words, or words that carry less meaning, but you may be surprised to see some of the words included (like "must" or "nobody"). Likewise, you may want to add a word that's not currently in the list (like "said"). Either way it's good to know what's there and to confirm that's what you want. You can find [more information on stopwords](https://voyant-tools.org/docs/#!/guide/stopwords).

### Summary

One last thing to point out from the Summary tool (bottom left): the "Distinctive words" list. Assuming your corpus has multiple documents, this shows the words that are not only high frequency, but high frequency and relatively distinctive to that document (the frequency is weighted by how often it's found i other documents using something called [TF-IDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)).

<iframe src="https://voyant-tools.org/?corpus=austen&amp;view=summary" style="width: 90%; height: 300px;"></iframe>
 
<br><br><br><br>
## WORK TIME!

{% capture text %}
Go to [Voyant Tools](https://voyant-tools.org/) and visualize your own content or open <a href="../data/sonnet=list-for-voyant.txt">a list of Shakespearean Sonnet URLS</a> we've provied.

If you're having trouble loading the 
{% endcapture %}
{% include alert.md text=text color=secondary %}
<br><br><br><br>



### Additional Tools

Voyant's default view (or skin) shows a collection of 5 tools, but in fact there are many more tools available in Voyant. You may have already discovered one way of accessing some of them: by clicking on a tab (for instance, the Cirrus tool can be replaced by the Terms or Links tools simply by clicking on the tab (and of course you can click on the Cirrus tab to return to the default view).

{% include figure.html img="more-tools.png" alt="More Tools information from Voyant Tools" caption="How to change tools in Voyant Tools" %}

The tabs are pre-programmed alternatives, but you can also choose from a much longer list of tools by clicking on the little window icon that appears when hovering over the header (either the blue header at the top that replaces all of the tools in the window or the grey header in each tool panel that replaces just that tool). Additional tools are organized into the following categories (tools can appear in multiple categories):

*   the first tools above the line are recommended alternatives
*   corpus tools: showing data about the corpus as a whole
*   document tools: showing data about individual documents
*   visualization tools: presenting data as charts, graphs, and other visual forms
*   grid tools: presenting data primarily in tabular form
*   other tools: various other forms of data presentation

Another convenient way of browsing tools is to consult the [list of tools](https://voyant-tools.org/docs/#!/guide/tools), especially as there is a small thumbnail image and short description for each tool.

{% capture more %}
To delve deeper into Voyant, go to the <a href="5-advanced.html">advanced section</a> of this workshop. We will not be covering this section in class today. 
{% endcapture %}
{% include alert.md text=more color=success %}

