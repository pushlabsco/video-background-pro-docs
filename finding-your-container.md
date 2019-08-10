# Finding Your Container

## Overview

Finding your container may be the most important aspect of using Video Background Pro. The container tells the plugin where to place the video background.

## What is a container?

A container in Video Background Pro is nothing more than a [CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp). A [selector](https://www.w3schools.com/cssref/css_selectors.asp) allow you to specify what element on a webpage you want to target. If you are new to selectors, I highly recommend taking a look at this w3schools article [CSS Syntax and Selectors](https://www.w3schools.com/css/css_syntax.asp). It will save you a lot of time looking for your container.

## How do I reference a selector/container?

Say we have found the element you want to target for a video background, and it looks like this:

```html
<div id="masthead" class="site-header">
    ...
</div>
```

In Video Background Pro, you can reference this element two ways:

* By the id attribute
* By the class attribute

**In HTML, id attributes have to be unique, however, classes can be used multiple times throughout the web page.**

Because of this, it is best to reference the ID over the class, as it has less of a chance of conflicting with other elements.

When referring to an ID in Video Background Pro, it must be prefixed by a hashtag. This let's the browser know that you are trying to reference an ID. So you would enter the following in the Video Background Pro container field:

```css
#masthead
```

Alternatively, if you wanted to reference the class, you would prefix it with a period:

```css
.site-header
```


