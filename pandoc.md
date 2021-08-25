# Create Webpages With Emmet

### So what is Emmet?

According to the [Emmet](https://emmet.io) website its "the essential toolkit for web developers."

With very little effort you can create the skeleton of an HTML (Hypertext Markup Language) very quickly. In this tutorial I will show you how to create most aspects of html using CSS (Cascading Style Sheets) type of formatting.

You can turn the following one line of HTML code from this:

```
#page>div.logo+ul#navigation>li*5>a{Item $}
```

Into this:

```
<div id="page">
    <div class="logo"></div>
    <ul id="navigation">
        <li><a href="">Item 1</a></li>
        <li><a href="">Item 2</a></li>
        <li><a href="">Item 3</a></li>
        <li><a href="">Item 4</a></li>
        <li><a href="">Item 5</a></li>
    </ul>
</div>

```

The first concept I'm going to discuss is how emmet handle the creation of HTML elements.

### Elements

You can use elements’ names like `div` or `p` to *generate* HTML tags. Emmet doesn’t have a predefined set of available tag names, you can write any word and transform it into a tag: `div` → `<div></div>`, `foo` → `<foo></foo>` and so on.


#### Nesting Operators

Nesting operators are used to position abbreviation elements inside generated tree: whether it should be placed inside or near the context element.


##### Child: `>`

You can use `>` operator to nest elements inside each other:

```
div>ul>li
```

...will produce

```
<div>
    <ul>
        <li></li>
    </ul>
</div>

```

##### Sibling: `+`

Use `+` operator to place elements near each other, on the same level:

```
div+p+bq
```

...will output

```
<div></div>
<p></p>
<blockquote></blockquote>

```
