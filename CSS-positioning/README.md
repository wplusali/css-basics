# Positioning

Work with a partner to implement the following user story:

* As a developer, I want to use the CSS position property to change the layout of my page.

## Instructions

Fix the given code so that:

* `box 2` is positioned in the middle of `square 1` using relative positioning.
* `box 2` is positioned outside of the upper-right corner of `square 2` using absolute positioning.

Your solution must match the following image:

![Box 2 is positioned in the center of Square 1, while in Square 2, Box 2 is positioned outside the square.](./assets/image-1.png)

## 💡 Hints

## How does the CSS `position` property change the document's normal flow? 

The CSS `position` property is used to determine how an element is positioned in the document layout and can significantly alter the normal flow of the document. There are several values that `position` can take, each affecting the document flow in different ways:

1. **Static**:
   - Default value.
   - Elements are positioned in the normal document flow.
   - `top`, `right`, `bottom`, `left`, and `z-index` properties do not affect statically positioned elements.

2. **Relative**:
   - Element is positioned relative to its normal position in the document flow.
   - Does not remove the element from the document flow. Instead, it shifts the element from its normal position without affecting the layout of surrounding elements.
   - Other elements act as though the relatively positioned element is still in its original location.

3. **Absolute**:
   - Element is removed from the normal document flow. It does not affect the layout of other elements.
   - Positioned relative to its nearest positioned ancestor (element with a position other than `static`). If no such ancestor exists, it's positioned relative to the initial containing block (usually the viewport).
   - Can overlap other elements unless managed with `z-index`.

4. **Fixed**:
   - Similar to absolute positioning, but positioned relative to the viewport. This means it stays in the same place even if the window is scrolled.
   - Removed from the normal document flow and does not affect the layout of other elements.
   - Commonly used for headers, footers, or other elements that should remain visible regardless of scrolling.

5. **Sticky**:
   - A hybrid of relative and fixed positioning.
   - The element is treated as relative until it crosses a specified threshold within the viewport (e.g., scrolled to a certain position), after which it becomes fixed.

Each positioning method serves different purposes and can be used to achieve specific layout effects or functional behaviors. For example, relative positioning is useful for small adjustments or for setting a positioning context for absolutely positioned children. Absolute positioning is crucial for overlaying elements, while fixed positioning is ideal for persistent navigation bars. Sticky positioning provides a practical way to keep elements in view during scroll interactions. 

In summary, the `position` property alters the document's normal flow in various ways, from minor adjustments (relative) to completely removing elements from the flow (absolute, fixed), and offers a mix of both behaviors (sticky). Understanding how each type works is essential for effective web layout design.

## 🏆 Bonus

If you have completed this activity, work through the following challenge with your partner to further your knowledge:

## What is the `z-index` property? 

The `z-index` property in CSS is used to control the vertical stacking order of elements that overlap each other. It's particularly useful in complex layouts where elements are positioned using `relative`, `absolute`, `fixed`, or `sticky` positioning. The `z-index` value determines which elements appear in front of others along the Z-axis (perpendicular to the screen).

Here are key points about the `z-index` property:

1. **Integer Values**:
   - The `z-index` property can take integer values (including negative values). A higher value means the element will be stacked on top of elements with lower values.

2. **Applies to Positioned Elements**:
   - `z-index` only works on elements with a `position` value other than `static` (i.e., `relative`, `absolute`, `fixed`, or `sticky`).

3. **Stacking Context**:
   - Each element with a `z-index` value creates a new stacking context. This means its children are stacked relative to it, not just relative to the rest of the page.
   - An element with a higher `z-index` value will cover an element with a lower `z-index` if they overlap.

4. **Default Value**:
   - The default `z-index` value is `auto`, which means the element does not create a new stacking context. Its stacking order is determined by its position in the document flow.

5. **Overlapping Elements**:
   - `z-index` is often used in web design for overlapping elements like modals, dropdown menus, tooltips, and other similar components that need to appear above other content.

6. **Relative Stacking**:
   - The stacking order is not just global; it's relative to the stacking context created by ancestors. An element with a `z-index` of 1 inside a parent with `z-index` of 2 will always appear above an element with a `z-index` of 3 that's part of a different stacking context (like a different parent with a lower `z-index`).

Here's an example of using `z-index`:

```css
.back {
  position: absolute;
  z-index: 1; /* Lower stacking order */
}

.front {
  position: absolute;
  z-index: 2; /* Higher stacking order, will appear above .back */
}
```

In this example, if `.back` and `.front` overlap, `.front` will appear above `.back` due to its higher `z-index` value. Understanding `z-index` is crucial for managing the layering of elements in complex layouts.

---
© 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
