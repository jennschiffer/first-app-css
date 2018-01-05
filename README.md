# My New Year's Resolution App

This is the second of a week-long series that will help you build your first Glitch app in 2018 - an app where you can keep your friends, family, and audience up to date on whether or not you're achieving your New Year's Resolution goals. Not doing New Years resolutions? Choose any yes or no status, like "Is it too cold for Jenn to drink iced almond milk lattes?" 

Coding is challenging, but if you take it day by day and practice, you can build the app of your dreams in no time - and we at Glitch and in the community are here to help!


## Here is a very short introduction to CSS

CSS stands for Cascading Style Sheets, which is a language for styling elements on a web page or app. In CSS, we write rule sets for setting the style of an element, starting with a "selector" which describes what element we want to style. For each selector we list one or more "declarations" which have a property and a value. The following is the syntax:

```
selector {
  property: value;
  another-property: another-value;
}
```

Let's use our app HTML as an example. Let's say we want our body element (our whole page) to have a different background color than the default white that our browsers typically set:

```
body {
  background-color: magenta;
}
```

In this case, we are selecting all `<body>` elements and setting the `background-color` property to "magenta". We can add more style to the body by adding more rules to this ruleås set:

```
body {
  background-color: magenta;
  font-family: 'Georgia', 'Times New Roman', serif;
}
```

The added declaration above sets the font to "Georgia" followed by some fall-backs in case the user's computer doesn't have that font. Make sure you choose readable fonts - even if you have great eyesight, a lot of people don't, and you don't want to make your content hard to read!

Like with most languages, there is syntax for leaving comments in CSS. The following comment doesn't change the style, but it gives info to you and others viewing the source, making the code more readable and maintainable.

```
/* the following css changes font size. "em" is a 
    unit that means multiple of the current font size - 
    so 2em is 2x the set font size. browsers tend 
    to default to 16px (px meaning pixels) as the font size. */
body {
  background-color: magenta;
  font-size: 2em;
}
```

There are many kinds of selectors besides HTML element tags. You can also select elements of a certain id or class (remember id and class are attribute options for HTML elements. In this app, we only want the body element to be centered on the index page, so I added an id attribute to the body tag in index.html:

```
<body id="index">
```

Now I can select that element so my code only affects the body element with that id:

```
#index {
  text-align: center;
}
```

id selectors are prefixed with `#` while class selectors are prefixed with a period - `.`

There are so many ways you can style your elements in CSS, that the best way to learn is to view the source of existing CSS files. Check out `style.css` in this app to see existing rule sets. 

Having your CSS in a .css file allows you to maintain a clean separation of languages between CSS and HTML. But you have to tell the app to use that file, so some HTML is required. Between the `<head></head>` tags we have to tell the browser to import our file like so:

```
<link rel="stylesheet" href="style.css" />
```

Every html page that you have the code in will import the CSS from that file. You can also write CSS in HTML by putting it within `<style></style>` tags in the `<head></head>` tags instead:

```
<style>
  /* make the text inside all paragraphs orange */
  p {
    color: orange;
  }
</style>
```

## You know a little about CSS, but there is a lot more!

There are many resources to learn more about CSS. Googling what you're looking to do, or to look up a rule you don't recognize, is usually effective. I also highly recommend [MDN's CSS documentation](https://developer.mozilla.org/en-US/docs/Web/CSS), which includes info on these and other selectors and properties. Their [CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) article is a great start.

Probably the most fun way to dive into CSS is to just go for it - check out the files in this project and play around until your site looks like what you want it to look - here is where you can best express yourself!

Tomorrow, we'll learn about JavaScript (JS) and how to use it to get information and update our page at different times!


ヽ(๏∀๏ )ﾉ

## What files are in this project?

### assets

This is a folder where you can upload assets like images. This project has an illustration of books because the example resolution has to do with reading.

### ← README.md

This file you're reading is a file written in Markdown - which is shorthand for HTML. Developers use README files to describe what their project is, along with any other info they have for contributors and users. In this project's README.md file, we talk about what the project is and list the files that are within it. You should keep this file up to date as you add features and pages to your app!

### ← index.html

This is the home page of our app and it's written entirely in HTML. Keep it updated to let users know what the date is and if you're achieving your resolution goals or whatever status you want to track this month!

### ← about.html

This is another HTML page that we link to in `index.html`. In it, talk about what your resolution is and anything else that you want your audience to know about you and your goals this year!

### ← style.css

This is the newest file in the app and it contains the CSS (Cascading Stylesheet) styling markup code for making our HTML content look nice.