# HTML Intro

The goal of this project is to get comfortable with editing code using Sublime Text 3, and to get our feet wet with HTML.

The first step will always be to add semantic structure to our content with HTML tags. Later, we'll add styling and positioning with CSS.

## Setup

 - **Fork** this repository to your own account (button in the top right).
 - **Clone** your fork in Desktop (button in the bottom right).

# Part 1: Roster

In the folder you just downloaded, there is a subfolder called `1_roster`. Within that folder, there is another subfolder called `1_semantic`. Within that folder, there is a file called `semantic_start.html`. Open it up in both Sublime and in Chrome. Right now, in Chrome, your version should look like a big wall of text with no formatting.
- There is another file called `semantic_target.html`. Open it up in both Sublime and in Chrome. This one should look slightly better than `semantic_start.html`. Your first job is to edit `semantic_start.html` in Sublime and keep refreshing it in Chrome until it looks like `semantic_target.html`.

**Note: It really helps to have as few tabs as possible open in Chrome; one for the document you are working on, and one for your target. Either close your other tabs, or open a separate window to work in.**

## Add Basic Tags

Right now, `semantic_start.html` contains only raw content, without any HTML structure at all. Your first job will be to go through and add some.

**The Wrap Selection With Tag (Ctrl-Shift-W on Mac, Alt-Shift-W on Windows) keyboard shortcut is your friend.** Highlight the content you want to put opening and closing tags around, then use the shortcut, then type the tag name that you want and it will modify both the opening and closing tags.

All of the content is pretty straightforward; some common tags you might find suitable to describe the content are

 - a
 - dl, dt, dd
 - h1
 - h2
 - ol, ul, li
 - p

Here is a good reference to learn about what these, and all other, tags are meant for:

https://developer.mozilla.org/en-US/docs/Web/HTML/Element

It's pretty remarkable to me that the entire web is built with such a relatively small number of elements. And of that small number, we use even fewer on a daily basis.

Anyway, I usually find it best to head straight for the examples when dealing with programming language documentation:

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl#Examples

## Add styles with CSS

 - Open `2_styling/styling_start.html` in Sublime and Chrome.
 - Open `2_styling/styling_target.html` in Chrome.
 - Edit `styling_start` in Sublime until it looks like `styling_target` in Chrome. You may need to add some extra `<div>`s, `<span>`s, or other elements to act as hooks to hang styles on.

## Add positioning

 - Open `3_positioning/positioning_start.html` in Sublime and Chrome.
 - Open `3_positioning/positioning_target.html` in Chrome.
 - Edit `positioning_start` until it looks like `positioning_target`. There are many different ways of achieving positioning in HTML; but, for learning purposes, let's use a table:


### HTML Tables

An important element in HTML is `<table>`.

`<table>`s in HTML are used to represent two dimensional data. A simple table looks like this:

    <table>
      <tr>
        <th>First</th>
        <th>Last</th>
      </tr>
      <tr>
        <td>John</td>
        <td>Doe</td>
      </tr>
      <tr>
        <td>Jane</td>
        <td>Doe</td>
      </tr>
    </table>

which would produce this:

<table>
  <tr>
    <th>First</th>
    <th>Last</th>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
  </tr>
</table>

The things to keep in mind about tables are:

 - Every piece of data must reside within a cell, a `<td>` element (or maybe a `<th>` element if it's a heading).
 - Every `<td>` or `<th>` element must reside within a row, a `<tr>` element.
 - Every `<tr>` must have the same number of cells, or things get out of whack.

Despite this last rule, you can, however, "merge" cells using the `colspan` and `rowspan` attributes:

    <table>
      <tr>
        <th colspan="2">People</th>
      </tr>
      <tr>
        <td>John</td>
        <td>Doe</td>
      </tr>
      <tr>
        <td>Jane</td>
        <td>Doe</td>
      </tr>
    </table>

produces:

<table>
  <tr>
    <th colspan="2">People</th>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
  </tr>
</table>

You can see that we've merged two cells in the first row together; the `colspan="2"` on the first cell ensures that we don't violate the "every `<tr>` must have the same number of cells" rule.

Similarly, you can merge cells vertically:

    <table>
      <tr>
        <th rowspan="2">People</th>
        <td>John</td>
        <td>Doe</td>
      </tr>
      <tr>
        <td>Jane</td>
        <td>Doe</td>
      </tr>
    </table>

produces:

<table>
  <tr>
    <th rowspan="2">People</th>
    <td>John</td>
    <td>Doe</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
  </tr>
</table>

Now, each row has three cells. The second row doesn't look like it at first glance, but the first cell in the first row is spanning down across two rows, so the second row really does have three cells.

### Using Tables For Positioning

Can you see how you could use a `<table>` to achieve horizontal positioning? In the real world, we would never do this; but, for learning purposes, do it now to achieve the three-column layout we want for our roster.
 
# Part 2: Landing Page with table

 - Open `2_landing_with_table/landing_with_table_start.html` in Sublime and Chrome.
 - Open `2_landing_with_table/solution/landing_with_table_target.html` in Chrome.
 - Add a `<table>` and any necessary `<tr>`s and `<td>`s to `landing_with_table_start` until it looks like `landing_with_table_target` in Chrome.

# Part 3: Landing Page with Bootstrap

 - Open `3_landing_with_bootstrap/landing_with_bootstrap_start.html` in Sublime and Chrome.
 - Open `3_landing_with_bootstrap/solution/landing_with_bootstrap_target.html` in Chrome.
 - Link `landing_with_bootstrap_start` to the external stylesheet `bootstrap.css`. Replace the class names that we made up in Part 3 with Bootstrap's class names until it looks like `landing_with_bootstrap_target` in Chrome.

