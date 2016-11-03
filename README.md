# Flexbox Pocket Guide

##### References:
- [W3] (https://www.w3.org/TR/css-flexbox/)
- [A Complete Guide to Flexbox] (https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### Guides:
- X: main axis
- Y: cross axis

### Summary of Flexbox Properties

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content
- order
- align-self
- flex-grow
- flex-shrink
- flex-basis
- flex

## Properties for container (Flex container)
```scss

.flex-container {

  display: flex; // new block-level
  display: inline-flex; // new inline-level

  // ==========================================================================
  // flex-direction: Specifies how flex items are placed in the flex container
  // ==========================================================================
  flex-direction: row; // left to right (Default)
  flex-direction: row-reverse; // right to left
  flex-direction: column; // top to bottom
  flex-direction: column-reverse; //bottom to top

  // ==========================================================================
  // flex-wrap: Controls whether the flex container is single-line or multi-line
  // ==========================================================================
  flex-wrap: nowrap; // single-line (Default)
  flex-wrap: wrap; // multi-line - left to right
  flex-wrap: wrap-reverse; // multi-line - right to left

  // ==========================================================================
  // flex-flow: shorthand
  // ==========================================================================
  flex-flow: <flex-direction> || <flex-wrap>; // row nowrap (Default)

  // ==========================================================================
  // justify-content: X axis
  // ==========================================================================
  justify-content: flex-start; // left to right (Default)
  justify-content: flex-end; // right to left
  justify-content: center;
  justify-content: space-between; // The flex items are distributed and a margin start end of first element and finish beginning of the last element.
  justify-content: space-around; // Flex items are evenly distributed in the line, with half-size spaces on either end.


  // ==========================================================================
  // align-items: Y axis
  // ==========================================================================
  align-items: stretch; // (Default)
  align-items: flex-start;
  align-items: flex-end;
  align-items: center;
  align-items: baseline;


  // ==========================================================================
  // align-content: Aligns the flex items on the Y axis when there is extra space
  // ==========================================================================
  align-content: stretch; // (Default)
  align-content: flex-start; // lines packed to the start of the container
  align-content: flex-end; //lines packed to the end of the container
  align-content: center; // lines packed to the center of the container
  align-content: space-between; // lines evenly distributed; the first line is at the start of the container while the last one is at the end
  align-content: space-around; // lines evenly distributed with equal space around each line

}

```

## Properties for item (Flex items)

```scss

.flex-item {

  // ==========================================================================
  // order: controls the order in which they appear in the flex container.
  // ==========================================================================
  order: <integer>;


  // ==========================================================================
  // flex-grow: (width) Determines how much the flex item will grow relative
  // to the rest of the flex items.
  // ==========================================================================
  flex-grow: <number>; // default 0


  // ==========================================================================
  // flex-shrink: (width) Determines how much the flex item will shrink relative
  // to the rest of the flex items
  // ==========================================================================
  flex-shrink: <number>; // default 1


  // ==========================================================================
  // flex-basis: This defines the default size of an element before the
  // remaining space is distributed.
  // ==========================================================================
  flex-basis: <length> | auto; // default auto


  // ==========================================================================
  // flex
  // ==========================================================================
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ];


  // ==========================================================================
  // align-self: This allows the default alignment (or the one specified
  // by align-items) to be overridden for individual flex items.
  // ==========================================================================
  align-self: auto | flex-start | flex-end | center | baseline | stretch;

}

```

> Note that float, clear and vertical-align have no effect on a flex item.


## Aligning with auto margins

One use of auto margins in the main axis is to separate flex items into distinct "groups".

```scss

.menu-flex {
  display: flex;

  &__item {
    padding: 1em;

    &--modifier {
      margin-left: auto; // Can set top, right, bottom
    }
  }
}

```
