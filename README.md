# CSS Flexbox Layout

This project is a sample of how to use the flexbox layout module.

The Flexbox Layout provides an efficient way to lay out, align and distribute space among items in a container, even if their size is unknown or dynamic.

The main goal of a flex layout is to give the container the ability to alter its items width and height to best fill the available space. The container expands items to fill the space or shrinks them to avoid overflow.

We can separate the flexbox system in two main groups, called `container` and `item(s)`, which will be
explained below.

![alt text](https://github.com/felipesantanadev/css-flexbox/blob/master/images/flexbox.jpg)


## Container

A flex container is a container with `dislay` property sets to `flex`.

```
.container {
  display: flex; /* or inline-flex */
}
```

We can see some important container's properties below:

- `flex-direction`  
  Defines the direction flex items are placed in the flex container. It can has the following values:  
  
  1. row (default): left to right
  2. row-reverse: right to left
  3. column: top to bottom
  4. column-reverse: bottom to top


- `flex-wrap`  
  Allow the items to wrap as needed. It can has the following values:  

  1. nowrap (default): all flex items will be on one line
  2. wrap: flex items will wrap onto multiple lines, from top to bottom
  3. wrap-reverse: flex items will wrap onto multiple lines from bottom to top


- `flex-flow`  
  This is a shorthand for the flex-direction and flex-wrap properties.  

  `flex-flow: <‘flex-direction’> || <‘flex-wrap’>`


- `justify-content`  
  It distributes extra free space leftover when either all the flex items on a line are inflexible or are flexible but have reached their maximum size. It can has the following values:  

  1. `flex-start` (default): items are packed toward the start of the flex-direction
  2. `flex-end`: items are packed toward the end of the flex-direction
  3. `start`: items are packed toward the start of the writing-mode direction
  4. `end`: tems are packed toward the end of the writing-mode direction
  5. `left`: items are packed toward left edge of the container, unless that doesn't make sense with the flex-direction, then it behaves like start
  6. `right: items` are packed toward right edge of the container, unless that doesn't make sense with the flex-direction, then it behaves like start
  7. `center`: items are centered along the line
  8. `space-between`: items are evenly distributed in the line. First item is on the start line, last item on the end line
  9. `space-around`: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren't equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
  10. `space-evenly`: items are distributed so that the spacing between any two items (and the space to the edges) is equal.


- `align-items`  
  This defines the default behavior for how flex items are laid out along the cross axis on the current line. It can has the following values:  

  1. `stretch` (default): stretch to fill the container (still respect min-width/max-width)
  2. `flex-start / start / self-start`: items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the flex-direction rules or the writing-mode rules.
  3. `flex-end / end / self-end`: items are placed at the end of the cross axis. The difference again is subtle and is about respecting flex-direction rules vs. writing-mode rules.
  4. `center`: items are centered in the cross-axis
  5. `baseline`: items are aligned such as their baselines align


- `align-items`  
  This aligns a flex container's lines within when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis. It can has the following values:  

  1. `flex-start / start` : items packed to the start of the container. The flex-start honors the flex-direction while start honors the writing-mode direction.
  2. `flex-end / end`: items packed to the end of the container. The flex-end honors the flex-direction while end honors the writing-mode direction.
  3. `center`: items centered in the container
  4. `space-between`: items evenly distributed. The first line is at the start of the container while the last one is at the end
  5. `space-around`: items evenly distributed with equal space around each line
  6. `space-evenly`: items are evenly distributed with equal space around them
  7. `stretch (default)`: lines stretch to take up the remaining space



## Items

The items are the contents packaged inside a container. We can see some important properties below.

- `order`  
  The order property controls the order in which they appear in the flex container.

- `flex-grow`  
  This defines the ability for a flex item to grow if necessary.  It dictates what amount of the available space inside the flex container the item should take up.

- `flex-shrink`  
  This defines the ability for a flex item to shrink if necessary.

- `flex-basis`  
  This defines the default size of an element before the remaining space is distributed. It can be a length (e.g. 20%, 5rem, etc.) or a keyword. The auto keyword means "look at my width or height property" (which was temporarily done by the main-size keyword until deprecated). The content keyword means "size it based on the item's content" - this keyword isn't well supported yet, so it's hard to test and harder to know what its brethren max-content, min-content, and fit-content do.

- `flex`  
  This is the shorthand for flex-grow, flex-shrink and flex-basis combined. The second and third parameters (flex-shrink and flex-basis) are optional. Default is 0 1 auto.

- `align-self`
  This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items. Its values are equals to the `align-items` property of containers.


## References

These README explanations were got from [CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).