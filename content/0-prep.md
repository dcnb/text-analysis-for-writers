---
title: Prep
nav: true
--- 


# Workshop Prep

You will need three things for this workshop:

2. some content (hopefully you have your own; we will also provide some)
1. a Laptop (we have some to hand out if you need one)
3. a text editor (although really you could get away without one. )


## Some Content
Textual analysis works by converting a text/texts into a proverbial "bag of words." These words become the "data" that the computer then counts, weighs, and measures in a variety of ways. 
In order to prepare your texts for computational analyses, you'll often need to prepare your text(s) in some fashion. 

If you don't have text of your own, we've provided some here, using Shakespeare's Sonnets: 

- [Shakespeare's Sonnets URLs in a CSV](/data/sonnets.csv)
- [Shakespeare's Sonnets in a CSV](/data/sonnets-text.csv)
- [Shakespeare's Sonnets in Plain Text](/data/sonnets-text.txt)


# Text Editors, Get One

Some tools will allow you to use PDFs and Word Documents, for instance,but other tools and processes might require you transform your text(s) into a [plain text](https://en.wikipedia.org/wiki/Plain_text) format (TXT). To do this, you'll need to download and install a text editor that will allow you to import, clean, and save text in this format, or in other plain formats, like a [Comma Separated Variables (CSV)](https://en.wikipedia.org/wiki/Comma-separated_values) file, which stores information in a table (TABULARLY!) and is very much like a spreadsheet. 

Many of us here use [Visual Studio Code]((https://code.visualstudio.com/)), from Microsoft, which is free and works on both Mac and PC computers. Another cross-platform text editor to consider is [Atom](https://atom.io/).

Windows users should consider [Notepad++](https://notepad-plus-plus.org/), which is simple to use and free. It also has a good find and replace function that works across files in a directory or files open in the editor. This is especially helpful for editing a larger number of files at the same time. 

{% include alert.md text="Note that Windows notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications." align="center" color="warning" %}
 
Mac users can also look at TextWrangler or BBEdit. Also TextEdit, the default text editor on Mac, is useful for simple tasks, like making a document plain text. 

On linux, Gedit will suffice. 

# What is Plain Text

Plain text is basically just what it describes, a file format that saves within it the bare minimum amount of information presented to it. Whereas a Microsoft Word document file will save within it a variety of inforamtion about the font, layout, and properties of the document prepared, a plain text file will save just that information. 

The following exercise will demonstrate the differences. This is adapted from a tweet by [Alex Gil](https://twitter.com/elotroalex?lang=en) (that I can't find at the moment). 

{% capture text %}
1. Open your text editor and create a TXT file that includes only the letter "a" (no spaces or breaks), then save this as "a.txt" in a new folder. 
2. Now open Word and create a similar file that only includes "a" and save it as "a.docx in that same folder.
3. Open your new folder via the Finder or Explorer and examine the file sizes. Notices anything?
4. Optional: If you're using a windows computer, change the file extension of the .docx file to ".zip." Open the .zip file by clicking on it and examine all the accompanying files within. What do you see? Try opening some of those files with your text editor!
{% endcapture %}
{% include card.md text=text header="Plain Text vs. Word Doc" %}
