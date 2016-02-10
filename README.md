# sorttable
Mirror from http://www.kryogenix.org/code/browser/sorttable/

## Make all your tables sortable

While the web design community gradually moves away from using tables to lay out the structure of a page, tables really do have a vital use, their original use; they're for laying out tabular data.

Pretty simple. But if you saw that table in a client-side application, you'd expect to be able to click on the headers and have the table sort, would you not? I know it always annoys me when you can't.

 A fair few web applications do allow this; most of them, which are pulling this data by submitting a SQL query to a relational database (an environment eminently suited to tabular data) implement this by resubmitting the whole page with something like ordercolumn=4 in the URL, and then adding an ORDER BY clause to their SQL query to return the data from the DB ordered by the specified column.

Resubmit the page? Just to sort data we already have? I'm sure we can do better than that.

As you can see, the above table now has clickable headers that sort the table by the clicked column. Note how the numeric and date columns all sort properly, too, rather than sorting alphanumerically.

This is not a new trick, sorting a table using the DOM. However, this mini-library has two nice attributes; the first is, unsurprisingly, that it follows my principles of unobtrusive DHTML, as you'll see below. The second is that, as mentioned above, it knows how to sort a variety of different data types, and it works them out for itself -- you don't have to tell it.

Now, how to use it. To make a table of your choice sortable, there are three steps:

  1. Download the Javascript library
  2. Include the Javascript library, by putting a link to it in the HEAD of your page, like so:

    ```<script src="sorttable.js"></script>```

  3.  Mark your table as a sortable one by giving it a class of "sortable":

      ```<table class="sortable">```

*Note that the library's JavaScript file is called sorttable (two Ts), but the class you add to the table is sortable (one T).*

And that's all you need. Your table will now have column sorting available by clicking the headers. For niceness, you might want to add the following styles to your stylesheet, or make up some of your own based on this:


    /* Sortable tables */
    table.sortable thead {
        background-color:#eee;
        color:#666666;
        font-weight: bold;
        cursor: default;
    }

This is version 2 of sorttable, released April 2007 and tweaked continually since.

For advance usage read the original page:
http://www.kryogenix.org/code/browser/sorttable/
