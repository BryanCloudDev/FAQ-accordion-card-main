# Frontend Mentor - Profile card component solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Continued development](#continued-development)
- [Author](#author)


## Overview

### The challenge

Users should be able to:

- Check how the mediaqueries work on different screen sizes
- Check how the check status works in order to show or hide the answers block
- See how we can play with the overflow property in CSS in order to hide some parts of an image.
- See how we can play with the positions in order to accomodate the images in the desktop layout in the way we need.

### Screenshot

#### Mobile design

<img src="https://i.imgur.com/SVdBB3v.png" width="400px" ></a>

#### Desktop design

<img src="https://i.imgur.com/agGs9fa.png" width="600px" ></a>



### Links

- Solution URL: (https://www.frontendmentor.io/solutions/responsive-faq-component-using-sass-and-html-only-4ySHTKgYW)
- Live Site URL: (https://bryanclouddev.github.io/FAQ-accordion-card-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- SASS preprocessor

### What I learned

This was a really tough one for me, I am glad I was able to take my time and do my best to do it properly, I first learnt how to use the ":checked" pseudoclass in order to detect when it is cheked and in this case, be able to either show or hide the answers block and also active the animation for the arrows when chcked too.

```css
.main .card .questionContainer .questions .question input:checked ~ label li .qaContainer .text {
  display: block;
}
.main .card .questionContainer .questions .question input:checked ~ label li .qaContainer .qTitle {
  font-weight: 700;
  color: #1d1e35;
}
.main .card .questionContainer .questions .question input:checked ~ label li .arrow {
  transform: rotate(180deg);
}
```
I was able to use this structure for HTML in order to wrap the questions and answers in a label, using the id "option-1" in this case I was able to link it with the checkbox type "checkbox" since this type of input allows us to select multiple items at the time. I hide the checkbox input and by using the ":checked" pseudoclass, I was able to either show or not the .text element.
```html
<div class="question">
    <input type="checkbox" id="option-1">
    <label for="option-1">
        <div class="qa">
            <div class="qaContainer">
                <h2 class="qTitle">How many team members can I invite?</h2>
                <p class="text">You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.</p>
            </div>
            <div class="arrow">
                <img src="./images/icon-arrow-down.svg" alt="" aria-hidden="true">
            </div>
        </div>
    </label>
</div>
```

In here I was able to learn and apply the positioning absolute and relative, I had to make a research to get the basics again on how they work since flexbox and grid help us a lot with positining and they are very useful too, I used them here in order to locate the main image and the cube image to match it with the design of the image for the layout to achieve.

```css
.main .card .imgContainer {
    width: 50%;
    height: 35.8rem;
    background: none;
    margin-top: 0;
    padding: 0;
    position: relative;
    overflow: visible;
  }
  .main .card .imgContainer .imgWoman {
    position: absolute;
    top: 2rem;
    overflow: hidden;
    width: 100%;
  }
  .main .card .imgContainer .imgWoman .img {
    position: relative;
    left: -7rem;
  }
  .main .card .imgContainer .box {
    display: block;
    position: absolute;
    top: 12rem;
    left: -9.25rem;
    width: 19.1rem;
  }
```
I know I have a lot to improve, but this motivates me because there is a lot of things I still do not know and I can get even better by practicing and reasearching.

I really loved thid challenge, I learned a lot!
### Continued development

I will definetely continue learning on how to use better the positioning when using absolute an relative values, I will also contine learning how to better structure my HTML and avoid semantic errors.


## Author

- Website - [bryancloud.dev](https://bryancloud.dev)
- Frontend Mentor - [@bryan-cloud](https://www.frontendmentor.io/profile/BryanCloudDev)
- Twitter - [@BryanCloudDev](https://twitter.com/BryanCloudDev)
