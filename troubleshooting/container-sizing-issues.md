# Container Sizing Issues

In Video Background Pro, the video background is always the size of the container that you specify. This means that if the container is an element with 50 pixels in width and height, that will be the size of the video background. **Additionally, if your container's height is 0 pixels or it does not have any content inside of it, the video background will not show up since the container is essentially non-existent.**

The best way to control the size of the container is to use CSS. Say you have a container:

```html
<div class="my-video-background">
    ...
</div>
```

That means that you can use the CSS selector `.my-video-background` to modify the height of the container:

```css
.my-video-background {
    height: 500px;
}
```

This code, however, is not very responsive. You could use media queries to take care of that!

```css
.my-video-background {
    height: 500px;
}

@media (max-width: 960px) {
    .my-video-background {
        height: 400px;
    }
}

@media (max-width: 560px) {
    .my-video-background {
        height: 250px;
    }
}
```

These values are likely not the best, but they illustrate how this could be achieved.

## Using Aspect Ratios

My favorite approach is to use aspect ratios, since they are percentage based, making them responsive by nature. However, these require a bit more thought and coding experience. [You can take a look at using aspect ratios in css here.](https://www.w3schools.com/howto/howto_css_aspect_ratio.asp)