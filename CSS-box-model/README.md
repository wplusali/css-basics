# Box Model

Work with a partner to implement the following user story:

* As a developer, I want to use the CSS box model properties to position four boxes inside a frame.
  
## Instructions

* Correct the code so that each box has a defined:
  * `padding` property
  * `margin` property
  * `border` property

Your solution should match the following image:

![Four numbered, differently colored boxes appear evenly spaced inside a larger box.](./assets/image-1.png)

## 📝 Notes

Refer to the documentation: 

[MDN Web Docs on CSS basic box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model)

[MDN Web Docs on padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

[MDN Web Docs on margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)

[MDN Web Docs on border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

## 💡 Hints

## How can we use the `margin` property to define space between elements?

The `margin` property in CSS is used to create space around elements, outside of any defined borders. Margin does not have a background color, and it is completely transparent. The space created by `margin` ensures that elements do not touch each other, which can be crucial for both the aesthetics and functionality of a layout.

Here's how you can use the `margin` property to define space between elements:

1. **Individual Sides**:
   - You can set margin for each side of an element (top, right, bottom, and left) individually.
   ```css
   .element {
     margin-top: 10px;    /* Space above the element */
     margin-right: 15px;  /* Space to the right of the element */
     margin-bottom: 20px; /* Space below the element */
     margin-left: 5px;    /* Space to the left of the element */
   }
   ```

2. **Shorthand Property**:
   - The `margin` shorthand property allows you to set all four margins in one line. The values are applied in a clockwise rotation (top, right, bottom, left).
   ```css
   .element {
     margin: 10px 15px 20px 5px; /* top right bottom left */
   }
   ```

3. **Symmetrical Margins**:
   - If the top and bottom margins are the same, and the right and left margins are the same, you can use a shorter shorthand.
   ```css
   .element {
     margin: 10px 20px; /* vertical horizontal */
   }
   ```

4. **Uniform Margin**:
   - If all four margins are the same, you can specify a single value.
   ```css
   .element {
     margin: 15px; /* applies to all four sides */
   }
   ```

5. **Auto Margin for Centering**:
   - You can use `margin: auto;` to horizontally center an element within its container, given that the element has a specified width.
   ```css
   .element {
     width: 50%;
     margin: auto;
   }
   ```

6. **Collapsing Margins**:
   - Vertical margins (top and bottom) of adjacent block-level elements may collapse into a single margin, which is the larger of the two margins. This does not happen with horizontal margins (left and right).

7. **Negative Margins**:
   - Negative values are also allowed for `margin`. This can be used to pull elements closer together or overlap them.

8. **Responsive Margins**:
   - Margins can also be set in percentages or viewport units (like `vw` and `vh`), which can be useful for responsive designs.

In summary, the `margin` property is a versatile tool for controlling the space around elements, helping to improve readability and create a visually appealing layout. It's one of the fundamental aspects of CSS that contributes to effective web design.

## 🏆 Bonus

If you have completed this activity, work through the following challenge with your partner to further your knowledge:

## What is the CSS `float` property?

The CSS `float` property is a positioning property that places an element to the left or right of its container, allowing text and inline elements to wrap around it. It's often used for wrapping text around images or creating layouts with columns. When an element is floated, it is taken out of the normal flow of the document and shifted to the left or right until it touches the edge of its containing box or another floated element.

Here are the key aspects of the `float` property:

1. **Values**:
   - `left`: The element floats to the left of its container.
   - `right`: The element floats to the right of its container.
   - `none`: The default value. The element does not float and will be displayed in the normal flow of the document.
   - `inherit`: The element inherits the `float` value from its parent.

2. **Usage**:
   - **Text Wrap**: Commonly used to wrap text around images. For example, an image in a paragraph with `float: left;` will allow the text to flow around the right side of the image.
   - **Creating Columns**: By floating elements like divs to the left or right, you can create simple multi-column layouts.

3. **Clearing Floats**:
   - Since floating elements are removed from the normal flow, other elements might behave unexpectedly. The `clear` property is used to prevent elements from wrapping around a floated element.
   - `clear` can take `left`, `right`, `both`, or `none` as values. If an element is set to `clear: left;`, it will not be displayed to the left of a floated element.

4. **Containing Floated Elements**:
   - Parent elements of floated elements can collapse because floated elements are not part of the flow. To prevent this, you can use the "clearfix" hack, which involves adding a pseudo-element with `clear: both;`.

5. **Limitations and Modern Alternatives**:
   - While `float` is useful, it has limitations in complex layout designs. Modern CSS offers better layout tools like Flexbox and CSS Grid, which provide more control and are more suited for complex layouts.

Here's a simple example of using `float`:

```html
<!DOCTYPE html>
<html>
<head>
<style>
.image {
  float: left;
  margin-right: 10px;
}
</style>
</head>
<body>

<img src="path/to/image.jpg" alt="Descriptive Image" class="image">
<p>Here is some text wrapping around the floated image. The text flows around the image on the right side.</p>

</body>
</html>
```

In this example, the image will float to the left, and the text in the `<p>` tag will wrap around the right side of it.

---
© 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
