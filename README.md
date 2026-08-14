# Stats preview card component

Hi! This is my solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). I tried my best to make my design match the original as closely as possible.

## Skills that I learned

1. **Mobile-first workflow**: I wrote the mobile styles first (without any media query), then used `@media (min-width: 768px)` to add desktop-only styles on top. This made the process much smoother than my previous desktop-first approach.

2. **Flexbox layout switching**: I used `flex-direction: column` for mobile and `flex-direction: row-reverse` for desktop, so the image and text swap positions and orientation depending on screen size.

3. **`<picture>` element**: Used `<source>` with `media` queries to serve different image files for mobile and desktop, instead of relying on `opacity` tricks (which would load both images unnecessarily).

4. **`mix-blend-mode`**: Used this along with a colored overlay `<div>` to recreate the purple-tinted photo effect from the design.

5. **`line-height` and `text-transform`**: Reviewed how to use these to automatically adjust text presentation. I also learned that besides using `<span>` to style part of a text, tags like `<br>` can be used to force a line break.

## What I struggled with

1. **Layout proportions**: I struggled to get the text content and image to match the design's proportions. Resizing the image sometimes distorted its original ratio. I tried setting fixed widths (35% for text, 65% for image), but eventually learned that the size should be set on the outer `<div>` first. I then used `height: 100%`, `width: 100%`, and `object-fit: cover` on the image itself to maintain its proportion while filling the container.

2. **`rem` base size**: After finishing this project, I realized my `font-size` was set to `1.5rem` rather than using the more common `62.5%` trick for easier rem-to-px conversion. Next time, I'll research the syntax before implementing it.

3. **`box-sizing`**: I learned that `box-sizing: border-box` is essential for controlling layout — without it, padding is added outside the element's defined width, which can throw off the entire layout. I will try this syntax on my next project.

## Demo

https://amyy1210.github.io/stats-preview-card-component/