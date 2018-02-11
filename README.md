# Component Variations

### Presentation on how to create component variations without repeating yourself.

Component based development is one of the hottest trends in web development because they present so many advantages over the traditional web development approach.

One big advantage of components is, if they are built properly, they can be reused througout your website without repeating code.

## What are component variations
Component variations is the ability to take a pre-existing component and modify it without altering the original component.  Component variations is usually achieved by using *modifier css classes* which are used when a different look or behavior needs to be achived.

## Example of a component variation

Let's start with a pretty basic button component.
```html
  <a href="#" class="button">Learn More</a>
```

Here are the styles which will apply to any element with the class of `button`.
```scss
.button {
  background: #000;
  border: 0;
  border-radius: 2px 2px 2px 2px;
  box-shadow: none;
  color: white;
  cursor: pointer;
  display: inline-block;
  font-family: Verdana, sans-serif;
  font-size: 16px;
  font-weight: lighter;
  letter-spacing: 2px;
  padding: 18px 50px;
  text-align: center;
  text-transform: uppercase;
}
```

![Primary button](images/btn.png)

---

## Creating variations

Now, without affecting the original button above, we will create two new variations in which we will change the background color of the button.  We will use the css classes `button--secondary` and `button--tertiary` to achive the new variation.  These new classes are appended to the original class of `button`

### Secondary button
```html
<a href="#" class="button button--secondary">Learn More</a>
```

```scss
.button--secondary {
  background: #c0392b;
}
```

![Primary button](images/btn-secondary.png)

---

### Tertiary button
```
<a href="#" class="button button--tertiary">Learn More</a>
```
```
.button--tertiary {
  background: #2980b9;
}
```

![Primary button](images/btn-tertiary.png)

Pretty cool huh? :metal:

---

Each of the examples above starts by using the default class of `button` to inherit all base button styles.  Whenever we want to use a different color button we append the class `button--secondary` or `button--tertiary` which overrides the original background color property and assigns a new color.  All other original button styles remain unchaged.

## More advanced variations
Now that we have a basic concept on variations, let's create a more advanced example.  This time we will start by creating a Card component which contains the following attributes:
* Image
* Title
* Excerpt text
* Link

This is how our default card looks like
![Default state of Card](images/card.png)

This is the markup and styles for our card:

*Markup*
```html
<div class="card">
  <div class="card__media">
    <img src="https://placeimg.com/640/350/nature" alt="Card component">  
  </div>

  <div class="card__text">
    <h2 class="card__text--title">Welcome to SandCamp</h2>
    <p class="card__text--teaser">Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Cras justo odio, dapibus ac facilisis in, egestas eget quam.</p>
    <a href="#" class="card__cta">Learn more</a>
  </div>
</div>
```

*Styles*
```css
@import url(https://fonts.googleapis.com/css?family=Roboto:400,700,300);

body {
  font-family: 'Roboto', 'Verdana', sans-serif;
  font-size: 16px;
  line-height: 1.5;
  background: #00BCD4;
  color: #444;
}

a {
  color: #FF1744;
  text-decoration: none;
  text-transform: uppercase;
}

.card {
  position: relative;
  max-width: 640px;
  background: #fff;
  margin: 40px auto;
  border-radius: 2px;
  box-shadow: 0 27px 55px 0 rgba(0, 0, 0, 0.3), 0 17px 17px 0 rgba(0, 0, 0, 0.15);
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}

.card__text {
  padding: 20px;
  left: 0;
  right: 0;
  bottom: 0;
}

.card__text--title {
  margin: 0;
  font-size: 24px;
  font-weight: 400;
}
```







