# Component Variations

### Presentation on how to create component variations without repeating yourself.

Component based development is one of the hottest trends in web development because they present so many advantages over the traditional web development approach.

One big advantage of components is, if they are built properly, they can be reused througout your website without repeating code.

## What are component variations
Component variations is the ability to take a pre-existing component and modify it without altering the original component.  Component variations is usually achieved by using *modifier css classes* which are used when a different look or behavior needs to be achived.

## Example of a component variation

Let's start with a pretty basic button component.
```html
  <a class="button">I'm a button</a>
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

![Primary button](btn.png)

### Creating variations

Now, without affecting the original button above, we will create two new variations in which we will change the background color of the button.  We will use the css classes `button--secondary` and `button--tertriary` to achive the new variation.  These new classes are appended to the original class of `button`

### Secondary button
```html
<a class="button button--secondary">I'm a button</a>
```

```scss
.button--secondary{
  background: #c0392b;
}
```

![Primary button](btn-secondary.png)


### Tertriary button
```
<a class="button button--tertriary">I'm a button</a>
```
```
.button--tertriary{
  background: #2980b9;
}
```

![Primary button](btn-tertriary.png)








