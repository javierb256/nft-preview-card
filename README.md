# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./Screenshot.png)

### Links

- Solution URL: [https://github.com/javierb256/nft-preview-card](https://github.com/javierb256/nft-preview-card)
- Live Site URL: [https://nft-preview-card-phi.vercel.app/](https://nft-preview-card-phi.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- SCSS
- Desktop-first workflow

### What I learned


To see how you can add code snippets, see below:

To create the overlay I made a div that would contain the overlay color and an <img> that contains the eyeball image

```html
<div class="image-container">
            <img class="nft-image" src="images/image-equilibrium.jpg" alt="equilibrium NFT"></img>
            <!--overlay markkup when mouse is over the nft image-->
            <div class="nft__overlay">
                <!--eye icon that is displayed on overlay-->
                <img src="images/icon-view.svg" alt="white eyeball">
            </div>
        </div>
```

The css involved having a class for the overlay properties. Its position would be absolute to have it stack on top of the nft image.
The background property has an rgba that would have the cyan color and an opacity of 0.5 to make it transparent. Its opacity would be defaulted as 0 to not show up when not hovered over.
When hovering over the nft image the overlay would change to 1 showing the styling applied. A transition for the opacity effect was added for a cooler effect made.

```css
.image-container {
  position: relative;
  top: 20px;
}

.nft__overlay {
  position: absolute;
  top: 0;
  left: 17px;
  width: 88%;
  height: 100%;
  border-radius: 7px;
  background: rgba(0, 255, 247, 0.5);
  opacity: 0;
  transition: opacity 0.25s;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.nft__overlay:hover {
  opacity: 1;
}
```


### Useful resources

- [Image Hover Text Overlay Effect with HTML & CSS - Web Design Tutorial](https://www.youtube.com/watch?v=exb2ab72Xhs) - This video helped me learn how to create css overlays and helped me gain new css concepts to be used in the future.

## Author

- Github - [javierb256](https://github.com/javierb256/nft-preview-card)

