# Frontend Mentor - Fylo dark theme landing page solution

This is a solution to the [Fylo dark theme landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-dark-theme-landing-page-5ca5f2d21e82137ec91a50fd). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [here](https://rafaeldevvv.github.io/fylo-dark-theme/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I liked this technique because I simply defined it once and didn't need to worry about it in the desktop version. I learned it on a video by Kevin Powell.

```scss
.section-padding {
  padding-inline: min(6vw, 4em);
}
```

In this section I tried to use linear-gradient, but, in my screen, it was a different color for some reason even though I used the same variables as in the footer and main sections. So, I just used two absolutely positioned divs.

```scss
#get-access {
  padding-block: 2em;
  position: relative;

  .back {
    position: absolute;
    z-index: -9999;
    pointer-events: none;
  }

  .main-color {
    inset: 0 0 50% 0;
    background-color: $dark-blue-main;
  }
  .footer-color {
    inset: 50% 0 0 0;
    background-color: $dark-blue-footer;
  }

  .box {
    max-width: 800px;
    margin: 0 auto;
    background-color: $dark-blue-intro;
    padding: 2.6em 2em;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
    border-radius: 10px;
  }

  h2 {
    font-size: 1.2em;
  }

  .inner {
    flex-direction: column;
    gap: 2em;
  }

  .error {
    text-align: left;
    font-size: 0.8em;
    font-weight: 700;

    margin-block-start: 0.5em;
    margin-inline-start: 2.5em;

    display: none;
  }

  form:has(.field:invalid) .error {
    display: block;
  }

  .field,
  .btn {
    width: 100%;
    font-size: 1em;
  }
}
```

Here I used the extend directive because I didn't want to put the gray-text class on every one of the links.

```scss
.footer-list {
  display: flex;
  flex-direction: column;
  gap: 1em;
  white-space: nowrap;

  a {
    @extend .gray-text;
    transition: color 0.2s;
  }
  a:hover {
    color: white;
  }
}
```

This is a class that only work in devices wider than 50em. I used this to increase the space on desktop. It is like a version 2 of the separate-space-1 class.
```scss
.separate-space-1-dk {
  > * + * {
    margin-top: 1.2em;
  }
}
```

### Continued development
I think I did a pretty good job this time. I need to use more sass features in my next projects. This is a very useful pre-processor that I want to master.

## Author

- Frontend Mentor - [@rafaeldevv](https://www.frontendmentor.io/profile/rafaeldevvv)
- Twitter - [@rafaeldevvv](https://www.twitter.com/rafaeldevvv)
