# Finding Your Container

<div style="padding-top: 56.25%; position: relative;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/oTHcCfta1Q0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Overview

Finding your container may be the most important aspect of using Video Background Pro. The container tells the plugin where to place the video background.

## What Is a Container?

A container in Video Background Pro is nothing more than a [CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp). A [selector](https://www.w3schools.com/cssref/css_selectors.asp) allow you to specify what element on a webpage you want to target. If you are new to selectors, I highly recommend taking a look at this w3schools article [CSS Syntax and Selectors](https://www.w3schools.com/css/css_syntax.asp). It will save you a lot of time looking for your container.

## How Do I Find My Container?

In order to find your container, you'll need a browser with developer tools. I would recommend using Google Chrome for this.

1. Start by hovering your mouse over the area in which you want the video background to appear.
2. Right click and select the **inspect** menu item. This will open the developer tools.
3. You'll notice a new window pops up with a hierarchical list of elements to the left. This is called the [DOM](https://www.w3schools.com/js/js_htmldom.asp). It is a tree of HTML elements. One of these elements is your container.
4. Since you were hovering over the area where you want your video background to be placed, the selected element should be close, if not correct. You'll know that the selected element is your container when you hover over it, and blue and or green fill up the entire area of where you want the video background to be placed. Feel free to watch the tutorial above for a more in depth demonstration.

[For an in depth dive into finding selectors, take a look at this tutorial by Google.](https://developers.google.com/web/tools/chrome-devtools/dom/)


## Once I Have Found My Container, How Do I Reference It?

Say we have found the element you want to target for a video background, and it looks like this:

```html
<div id="masthead" class="site-header">
    ...
</div>
```

In Video Background Pro, you can reference this element two ways:

* By the id attribute
* By the class attribute

**In HTML, id attributes have to be unique while classes can be used multiple times throughout the web page.**

Because of this, it is best to reference the ID over the class, as it has less of a chance of conflicting with other elements.

When referring to an ID in Video Background Pro, it must be prefixed by a hashtag. This let's the browser know that you are trying to reference an ID. So you would enter the following in the Video Background Pro container field:

```css
#masthead
```

Alternatively, if you wanted to reference the class, you would prefix it with a period:

```css
.site-header
```

