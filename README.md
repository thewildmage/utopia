# Personal Utopia

Inspired and informed by [Utopia](https://utopia.fyi), these are my own personal Utopia-like defaults.

I've made a few changes from the original. Here's what and why (a.k.a. notes to my future self to help me remember details around decisions):

-   I've recreated all the underlying calculations in CSS. I did this because I wanted to use the more modern `clamp` function, but still wanted to be able to adjust the input configuration from within the CSS, without having to go back to Utopia's generators to copy/paste out updates. (The type scale calculator currently spits out things like `--step-0: clamp(1.31rem, calc(1.24rem + 0.37vw), 1.50rem);` when you opt for `clamp`.) This change also enables me to pull in the default `utopia.css` from here and then easily override the configuration from within any given project, thanks to the cascade.
-   I personally found the difference between `--step--1` and `--step-1` a bit difficult to read, so I've opted instead for a numbering scheme that already exists in CSS, the one used by `font-weight`. This means that the scale is centered at `400` and moves up and down by increments of 100. I hope to never need it, but this also gives me room to easily add partial steps without shifting the entire scale (e.g. `--size-450`).
-   I'm not overly fond of using T-shirt sizing because I don't like the suggestion that "medium" is the normal, default, centered part of a scale and the way that maps back out to people. Since I decided to change the naming scheme for the space scale anyway, I opted for consistency and used the same scale for spaces as for font sizes.
