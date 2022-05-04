# Frontend Mentor - Loopstudios landing page solution

This is a solution to the [Loopstudios landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/loopstudios-landing-page-N88J5Onjw). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)

- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)



## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page



## My process
Men, I dont know where to start from it was really stressful

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow
- Inline JS


### What I learned

I thought of this technique on my own with the little knowledge I had, I used it create a fading-in navigation when you tap on the navigation button.

```html
<button aria-label="Open navigation" class="open-nav-btn">
  <svg width="28px" height="100%" viewBox="0 0 24 16" xmlns="http://www.w3.org/2000/svg"><g fill="currentColor" fill-rule="evenodd"><path d="M0 0h24v2H0zM0 7h24v2H0zM0 14h24v2H0z"/></g></svg>
</button>

<nav class="home-nav nav-bar">

  <button aria-label="Close navigation" class="close-nav-btn"><svg  width="28px" height="100%"  viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17.778.808l1.414 1.414L11.414 10l7.778 7.778-1.414 1.414L10 11.414l-7.778 7.778-1.414-1.414L8.586 10 .808 2.222 2.222.808 10 8.586 17.778.808z" fill="currentColor" fill-rule="evenodd"/></svg></button>

  <ul class="home-nav-list nav-list">
    <li><a class="nav-link home-nav-link" href="#">About</a></li>
    <li><a class="nav-link home-nav-link" href="#">Careers</a></li>
    <li><a class="nav-link home-nav-link" href="#">Events</a></li>
    <li><a class="nav-link home-nav-link" href="#">Products</a></li>
    <li><a class="nav-link home-nav-link" href="#">Support</a></li>
  </ul>
</nav>

```
```css
.home-nav{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    opacity: 0;
    z-index: -1;
    background-color: black;
    transition: ease-in-out .5s;
}

.nav-open{
    opacity: 1;
    z-index: 6;
}


.open-nav-btn{
    border: 0;
    color: white;
    background: 0;
    cursor: pointer;
}

.close-nav-btn{
    position: absolute;
    right: 0;
    top: 0;
    border: 0;
    color: white;
    background: 0;
    cursor: pointer;
    padding: 30px;
    margin-top: 35px;
}

```
```js
  const closeButton = document.querySelector('.close-nav-btn');
  const openButton = document.querySelector('.open-nav-btn');
  const nav = document.querySelector('.home-nav');

  closeButton.addEventListener("click", () => {
  nav.classList.remove('nav-open');
  }); 

  openButton.addEventListener("click", () => {
  nav.classList.add('nav-open');
  }); 

```



### Continued development

*CSS GRID

### Useful resources

https://www.w3docs.com/tools/code-editor/18672
(this helped me in centering pseudo elements)


## Author
- Ephraim John
- WhatsApp - [@2349157795679]
- Twitter - [@Ephraimswagkid](https://www.twitter.com/Ephraimswagkid)


## Acknowledgments

Hat tip to EVERYONE GOOGLE, STACKOVERFLOW and NUPAT BOOTCAMP

