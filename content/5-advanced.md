---
title: Deeper into Voyant
nav: true
---
## Digging Deeper with Voyant

Voyant is an ongoing negotiation between simplicity and power: the design tries to simplify (relatively) the interface while still allowing more advanced operations.

### Search

<iframe src="https://voyant-tools.org/tool/CorpusTerms/?corpus=austen" style="width: 350px; height: 350px; float: right;margin-left:20px;"></iframe>

A good example of this is [search](https://voyant-tools.org/docs/#!/guide/search), which is supported in several of the tools (including Reader, Trends and Contexts in the default view). It's possible to search for a single word, but more advanced searches are also supported with a special syntax (hovering over the question mark in the search box shows examples of the syntax). Try the search terms (in bold) in the list below (you can remove a query by hitting x in the box surrounding the query, or hitting backspace to delete it). Also notice that Voyant tries to suggest search terms as you type, you can click on a suggestion to add it to the queries.

*   **love**: exact word match
*   **lov***: combine all words that start with "lov"
*   **^lov***: separate all words that start with "lov"
*   **love|loves**: combine all words separated by a pipe |
*   **"he loves"**: exact phrase match
*   **"she he love*"~10**: all words within a proximity of 10 words

The notion of boolean operators (AND, OR) isn't relevant for most tools since we're querying for any instance of any of the **words** (unlike when we're wanting to find **documents** that contain any or all queries). Note also that Voyant doesn't support directly notions like singular and plural forms, but that you can determine what forms are present ("**^dog***") and then decide if you want to combine forms ("**dog|dogs**") or keep them separate ("**dog,dogs**"). That helps for individual queries but of course doesn't help much when you would want to see all singular and plural forms combined in a frequency list.

### Grids

Another example of somewhat hidden power in the Voyant interface can be found in most grid-based tools (that look like spreadsheets, like Contexts in the default view). This is an overview of some of the functionality that may not be obvious:

*   hover over the column header to get a short description of the column values
*   some columns allow you to sort values by that column by clicking on it (and clicking again to reverse the order)
*   most columns can be reordered by dragging and dropping the column headers
*   most grids allow for row selection: select a row by clicking on it, select multiple rows by using the Shift or Ctrl/Command key
*   some grids have checkboxes (leftmost column) that facilitate selecting multiple items
*   selected rows should persist even when querying for additional data
*   some grids have a plus icon (leftmost colunm) that allows the user to expand more information about that row
*   most grids have "infinite scrolling" which means that more rows will be loaded dynamically as needed and as available
*   hovering over most column headers will cause an arrow to appear in the right part of the column header, click on it for further options:
    *   another way of sorting
    *   a way of selecting additional columns to display

<div style="max-width: 450px;">

{% include figure.html img="grid.png" alt="Grid example from Voyant Tools" caption="Grid example from Voyant Tools" %}

</div>