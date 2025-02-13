# CSS Basics Part II 

## Lecture Overview

In this lecture, I learned about CSS properties related to Positioning and Backgrounds. These properties are fundamental in creating visually appealing layouts and controlling the placement of elements on a webpage.

This document provides a detailed explanation of the properties covered in the lecture, with examples to help us understand how to use them effectively.

---

## Position Properties

CSS `position` defines how an element is positioned in the document flow. There are five main values: `static`, `relative`, `absolute`, `fixed`, and `sticky`. Here's an overview of each:

### 1. position: static (Default)

- **Description:** The default positioning of elements. Elements are placed in the natural flow of the document.
- **Use Case:** No additional positioning; the browser determines the position.

```css
div {
    position: static;
}
```

### 2. position: relative

- **Description:** Positions the element relative to its normal position. You can use top, right, bottom, or left to move it.
- **Use Case:** Useful for slight adjustments or creating offset effects.

```css
  div {
    position: relative;
    top: 10px;
    left: 20px;
}
```

### 3. position: absolute

- **Description:** Removes the element from the document flow and positions it relative to its nearest positioned ancestor (not static).
- **Use Case:** Commonly used for modals, dropdown menus, or overlays.

```css
  div {
    position: absolute;
    top: 50px;
    left: 30px;
}
```

### 4. position: fixed

- **Description:** Positions the element relative to the viewport. The element stays fixed in place when scrolling.
- **Use Case:** Perfect for sticky headers, footers, or side navigation bars.

```css
div {
    position: fixed;
    bottom: 0;
    width: 100%;
}
```

### 5. position: sticky

- **Description:** The element toggles between relative and fixed, depending on the user's scroll position. It "sticks" to a position as long as it's within its parent container.
- **Use Case:** Used for sticky navigation menus or table headers.

```css
div {
    position: sticky;
    top: 0;
}
```

---

## Background Properties

CSS background properties allow us to control the visual style of an element's background, such as color, image, position, and size.

### 1. background-color

**Description:** Sets the background color of an element.
**Values:** Any valid color (red, #ff0000, rgba(255, 0, 0, 0.5)).

```css
div {
    background-color: lightblue;
}
```

### 2. background-image

**Description:** Sets an image as the background of an element.
**Values:** URL of the image.

```css
div {
    background-image: url('background.jpg');
}
```

### 3. background-repeat

- **Description:** Specifies if/how the background image repeats.
- **Values:**
     - `repeat` (default): Repeats both horizontally and vertically.
     - `repeat-x`: Repeats horizontally.
     - `repeat-y`: Repeats vertically.
     - `no-repeat`: Does not repeat.

```css
div {
    background-image: url('pattern.png');
    background-repeat: no-repeat;
}
```

### 4. background-size

- **Description:** Specifies the size of the background image.
- **Values:**
   - `auto:` Default size.
   - `cover:` Scales the image to cover the entire container.
   - `contain:` Scales the image to fit within the container.

```css
div {
    background-image: url('hero.jpg');
    background-size: cover;
}
```
  
### 5. background-position

- **Description:** Positions the background image.
- **Values:** Keywords like `top`, `center`, `bottom`, `left`, `right` or precise values like `50% 50%`.

```css
div {
    background-image: url('banner.jpg');
    background-position: center;
}
```

### 6. background-attachment

- **Description:** Controls whether the background image scrolls with the page or is fixed.
- **Values:**
    - `scroll`: Background scrolls with the content.
    - `fixed`: Background stays fixed in place.
    - `local`: Background scrolls within the element.

```css
div {
    background-image: url('parallax.jpg');
    background-attachment: fixed;
}
```

### 7. Shorthand: background

The background shorthand combines multiple background properties into one line.

```css
div {
    background: url('background.jpg') no-repeat center/cover;
}
```

---

## Summary of Properties

### Position Properties

The table below summarizes the common positioning properties, their values, and descriptions:

| **Property**         | **Values**                   | **Description**                     |
|-----------------------|-----------------------------|-------------------------------------|
| **position**         | `static`, `relative`, `absolute`, `fixed`, `sticky` | Controls element placement.         |
| **top / right / bottom / left** | Length values (`px`, `%`)         | Moves positioned elements.          |

---

## Background Properties

The table below summarizes common background properties, their values, and descriptions:

| **Property**           | **Values**                                | **Description**                                        |
|-------------------------|-------------------------------------------|-------------------------------------------------------|
| **background-color**   | Any valid color (`red`, `#hex`, `rgba`)   | Sets the background color.                           |
| **background-image**   | `url('path-to-image')`                    | Sets a background image.                             |
| **background-repeat**  | `repeat`, `no-repeat`, `repeat-x`, `repeat-y` | Controls how the image repeats.                     |
| **background-size**    | `auto`, `cover`, `contain`, custom sizes  | Scales the background image.                         |
| **background-position**| Keywords (`center`, `top`) or percentages | Positions the background image.                      |
| **background-attachment** | `scroll`, `fixed`, `local`             | Controls scrolling behavior of the background image. |
