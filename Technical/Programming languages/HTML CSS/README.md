# HTML CSS
**Q: What is the difference between the `visibility` and `display` CSS properties?**  
Answer: The `visibility` property determines whether an element is visible or not, but the element still takes up space in the layout. The `display` property determines how an element should be displayed and whether it should take up space in the layout or not.

**Q: How do you center an element horizontally and vertically in CSS?**  
Answer: One way to center an element horizontally is to set its `margin` property to `auto` and give it a fixed width. To center an element vertically, you can use the `flexbox` or `grid` layout.

**Q: What is the difference between the `float` and `position` CSS properties?**  
Answer: The `float` property is used to move an element to the left or right and allow other content to wrap around it. The `position` property is used to control the positioning of an element on the page.

**Q: How do you create a responsive website in CSS?**  
Answer: You can use media queries to define different styles for different screen sizes, and use flexible layouts like `flexbox` and `grid` to adapt to different screen sizes.

**Q: What is the `z-index` CSS property used for?**  
Answer: The `z-index` property is used to control the stacking order of elements on the page, with higher values placing an element on top of lower values.

**Q: What is the `overflow` CSS property used for?**  
Answer: The `overflow` property controls what happens when the content of an element overflows its container. It can be set to `hidden`, `scroll`, `auto`, or `visible`.

**Q: What is the difference between `padding` and `margin` in CSS?**  
Answer: The `padding` property adds space inside an element's border, while the `margin` property adds space outside an element's border.

**Q: How do you create a sticky header in CSS?**  
Answer: You can use the `position: sticky` property to make an element stick to the top of the page as the user scrolls.

**Q: What is the difference between the `em` and `rem` units in CSS?**  
Answer: The `em` unit is relative to the font size of the parent element, while the `rem` unit is relative to the font size of the root element (`<html>`).

**Q: How do you create a responsive image in CSS?**  
Answer: You can use the `max-width: 100%` property to make an image scale down proportionally to fit its container on smaller screens, while still maintaining its original aspect ratio.

**Q: What is position relative and what is the difference with position absolute?**  
In CSS, `position: relative` is a property value that positions an element relative to its original position in the normal document flow. This means that the element will still take up space in the layout, and other elements will still be positioned as if the relative element was in its original position.

On the other hand, `position: absolute` is a property value that positions an element relative to its nearest positioned ancestor (an element that has a position value of anything other than `static`) or to the initial containing block if there is no positioned ancestor. This means that the element is completely removed from the normal document flow, and other elements will be positioned as if the absolute element was not there.

In summary, `position: relative` allows an element to be positioned relative to its original position while still taking up space in the layout, while `position: absolute` allows an element to be positioned relative to its nearest positioned ancestor or the initial containing block, completely removing it from the normal document flow.
