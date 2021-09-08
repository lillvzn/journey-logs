# Daily Logs

#### Table of contents

- [Introduction](#introduction)
- [Day 01](#day-01)
- [Day 02](#day-02)
- [Day 03](#day-03)
- [Day 04](#day-04)
- [Day 05](#day-05)

---

**To check out actual progress, hit: https://github.com/daemonslayer/softwareDevelopment-bootcamp**

---

## Introduction

Confusion in life is pretty common isn't it? Let me tell you my story. I started my career as a project manager, I couldn't handle so resigned to pursue data science. 8 months in the course and I started wondering whether this is the right field, did I make the right decision? After loads of thinking, I understood that analytics and statistics isn't what I need and decided not to continue anymore.

I like creating stuff, like to think out of the box. What better choice than software engineering can provide me with such qualities?

#### Past mistakes

During my college days, I had started learning web development, I think it was Colt Steele's course that I took. I finished the course and that's it, I understood the basics of HTML/CSS and some JavaScript. And so I assumed I was proficient in developing websites and ready to move on (_this is where I should've advanced deep into web dev/software engineering..._) Little did I know that I was just getting started, but I went on to choose a more "user-friendly" language, **Python**. I learnt the basics again, it was quite easy but I never really advanced further. By the time I realised that I had already graduated, _touche_.

So here I am, once again starting my journey in web development. But this time I will stick to this no matter how tough it gets in the coming days. The imposter syndrome has already kicked in, _will I be able to do it?_, _I don't think I'm capable of it, maybe software engineering isn't for me_. But I know I need to ignore that and work my way up.

So here I am, once again starting my journey in web development. But this time I will stick to this no matter how tough it gets in the coming days. The imposter syndrome has already kicked in, _will I be able to do it?_, _I don't think I'm capable of it, maybe software engineering isn't for me_. But I know I need to ignore that and work my way up.

**THIS IS REDEMPTION!**

#### [Top](#table-of-contents)

---

## Day 01

Day 1 was chill, it always is. Here's what I learnt:

**HTML fundamentals**

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta/> <!-- to define page's content -->
        <title> Title of the page </title>
    </head>

    <body> <!-- Everything on the webpage visible to user -->
        <header> <!-- The main part of the body goes here -->
            <h1> Heading tag with highest ranking </h1>
            <h6> Being the least ranked </h6>

            <nav> Navigation bar </nav>
        </header>

        <article> <!-- Next important content goes here -->
            <img src="some-image.jpg" alt="This is an image">
            <!-- Image tag, src -> source of the image, alt -> alternate text -->

            <p> Paragaph tag </p>
            <strong> Bold text </strong>
            <em> Emphazised/italic text </em>

            <a href="some-link"> Link explanation </a> <!-- hyperlink -->

            <ul> <!-- unordered list -->
                <li> list element </li>
            </ul>

            <ol> <!-- ordered list -->
                <li> List element </li>
            </ol>

            <button> Text on button </button>
        </article>

        <div> <!-- div tag is used instead of article when content isn't semantically related -->
        </div>

        <aside> Extra content in a page </aside>

        <footer> Footer of the webpage </footer>
    </body>
</html>

```

**CSS fundamentals**

```
inline:
    <h1 style="color:blue;">

internal:
    <style>
        h1 {
            color: blue;
        }
    </style>

external: (different stylesheet)
    h1 {
        color: blue;
    }
```

**class**: can be repeated throughout the file
`<p class="class-name"> Some text </p>`

**id**: can be used only once (rarely used)
`<p id="id-name"> Some text </p>`

#### [Top](#table-of-contents)

---

## Day 02

Explored a bunch of stuff today. CSS is huge TBH, it's quite interesting tho. Priorities, declarations, decorators etc. Here's what I learnt:

**HTML extended**

```
<p class="class-name second-class-name"> some text </p>
<!-- multiple classes can be added to a tag -->
<!-- but only one ID per element is possible -->
```

**More CSS fundamentals**

    Recap

    Types: Inline, Internal, External
    Priority: H to L -->  !important > inline CSS > ID > class/pseudo-class > element selector > universal

```

- { /_ universal declaration _/
  /_ ALWAYS INCLUDE THIS IN STYLESHEETS _/
  padding: 0;
  margin: 0;
  }

.class-name {
property: value;
}

#id-name {
property: value;
}

HTML-element {
property: value;
}

tag:link { /_ pseudo class, same applies to classes and ids _/
property: value;
}

tag::after { /\* pseudo element, same applies to classes and ids
property: value;
}

.class-name {
position: absolute; /_ absolute position wrt that class _/
top: 0;
right: 0;
/_ shows the element at top right position in class-name box _/
}

.class-name {
display: block; /_ displays as block element, one line after the other _/
display: inline; /_ same line _/
display: inline-block; /_ displays inline elements as block container _/

    /*
    inline elements cannot have height, width properties (includes padding margin etc)
    block elements can take such properties
    */

}

.class-name > ul > li:a:link:first-child {
property: value;
/_ property applied to first element (a tag) in li in ul of class-name _/
}

```

#### [Top](#table-of-contents)

---

## Day 03

Today was banging! More CSS. And a lot more confusing challenges, but I came through.
Here's what I learnt:

```
Summary: -> CSS layouts:
         Float (older method to create layouts)
         FlexBox (1-D layouts)
         Grid (2-D layouts)
```

**More CSS**

```
/* LAYOUT: FLOATS */

.class-name {
    float: left/right;
    /* a method to create layouts, not really used these days */
    /* loads of manual labour */
}

.clearfix::after { /* used as a hack to avoid float element overflow */
    clear: both;
    content: "";
    display: block/inline-block;
}

/* LAYOUT: FLEXBOX */

.class-name {
    display: flex;
    /* used instead of FLOAT as there is not necessity to define manual px */

    align-items: value;
    /* aligns items inside container (all div elements) with given property-value */

    justify-content: value;
    /* align flex items to given property-value */
}

.class-name {
    /* default values */
    flex-grow: 0; /* sets flex item's size */
    flex-shrink: 1; /* to overflow content, use 0 */
    flex-basis: auto; /* initial main size of flex item */

    flex: flex-grow flex-shrink flex-basis;
    flex: 1 0 250px;

    gap: value; /* gives gap between layouts */
}

/* LAYOUT: CSS GRID */

.class-name {
    display: grid;
    /* used to create 2-d layouts */

    grid-template-columns: 250px 250px 250px;
    /* create 3 columns of each 250px */

    grid-template-rows: 250px 300px;
    /* create 2 rows of 250px and 300px each */

    /* can also be defined as below */

    grid-template-rows/columns: 1fr 1fr 1fr;
    /* fr short for fraction, used to define size of the layout in grid */
    /* this can also be written as */
    grid-template-rows-columns: repeat(3, 1fr);
}

.class-name {
    /* some grid properties */
    column-gap: value in px;
    row-gap: value in px;

    align-items: start/center...;
    /* aligns items in grid to given value */

    grid-row: 1 / -1;
    /* layout content flows from start end of the given container via row */

    grid-column: 1 / -1;
    /* same as above via column */
    /* these can also be used for shifting layouts inside a grid */
}
```

There are so many others but these are some of the most used ones in CSS world. The important takeaway here is not how many properties you know but how many of them have you understood in a correct way.

#### [Top](#table-of-contents)

---

## Day 04

Quite an interesting day today. Learnt design properties like typography, colors, image and illustrations, white-spaces, shadows, icons, border designs and much more.

Learning UX design patterns and importance of UI/UX was fun too.

It's important to know how to create an excellent looking and functional/logical webpage. Always avoid cluttering elements, keep it minimal yet add in a bit of touch (so called _wow factor_) so that the users feel welcome and not bored.

Use colors that are matching background and text-colors. Make sure the element/ component you want the user to look at is distinguished in a color that's not background or text-color.

Try and use minimal values for shadows. For rounded edges on buttons or boxes, use px levels more than their defaults (_if the box is rectangle_). If it's a square, use 50%.

**CSS in design**

```

/*
SPACING SYSTEM (px)
2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128
FONT SIZE SYSTEM (px)
10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98
*/

/* Using definitive spacing and font-sizes will give less options to explore which inturn provide consistancy in usage */


.class-name {
    border-radius: 5px;
    /* creates curves around an element */

    font-family: serif/sans-serif;
    /* depending on website personality, use font-families */

    line-height: value;
    /* the larger the font-size is, the less the line height */

    stroke: color-value;
    fill: color-value;
    /* coloring icons */

    box-shadow: 0px 0px 0px 0px color;
    /* horizontal vertical blur-value scale (optional) color-value */
}

/* always use better color contrast ratios wrt background color and font-color/main color */

/* always create a hierarchy in the page, more priority towards a component you want the user to notice */
```

#### [Top](#table-of-contents)

---

## Day 05

Building components and layout patterns was amazing. Went through topics like grid, flex, overflow and so much more.

Components like accordion, carousel, pagination, heros and tables were learnt along with some new HTML tags. Damn there's so much!

**Some HTML**

```
<blockquote> Used for quotes </blockquote>

<table> <!-- To create tables -->
    <thead> <!-- head -->
        <tr> <!-- row -->
            <th> Some text </th> <!-- header row data -->
            <th> Some text </th>
        </tr>
    </thead>

    <tbody> <!-- body of table -->
        <tr>
            <td> Some other text </td> <!-- normal data -->
            <td> Some other text </td>
        </tr>
    </tbody>
</table>


<main> represents main content of the body </main>
<menu> represents a menu </menu>

```

**CSS fun**

```

.class-name {
display: grid;

    grid-template-columns: 1fr 1fr 1fr;
    /* coulmns are divided to 3 columns with equal spaces */

    grid-template-rows: 1fr 2fr;
    /* rows divided to 2 with one getting twice the size of the other */

}

.class-name {
overflow: scroll;
/_ set the overflowing content to scroll _/
}

.class-name {
height: 100vh;
/_ view port height, set the content to available viewport dimensions _/
}

.class-name {
transform: translate(-50%, 36px);
/_ transforms in-relation to self _/

    top: 50%;
    /* transforms in-relation to parent element */

}

```

#### [Top](#table-of-contents)

---

## Day 06
