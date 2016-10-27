# Flexbox Pocket Guide

##### References:
- W3: https://www.w3.org/TR/css-flexbox/
- A Complete Guide to Flexbox: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

### Guides:
- X: main axis
- Y: cross axis

## Properties for container (Flex container)
```scss

  .flex-container {

    display: flex; // new block-level
    display: inline-flex; // new inline-level

    // ==========================================================================
    // Flex direction: Specifies how flex items are placed in the flex container
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

  // ============================================================================
    // justify-content: X axis
    // ==========================================================================
    justify-content: flex-start; //left to right (Default)
    justify-content: flex-end; //right to left
    justify-content: center;
    justify-content: space-between; // The flex items are distributed and a margin start end of first element and finish beginning of the last element.
    justify-content: space-around; // Flex items are evenly distributed in the line, with half-size spaces on either end.


    // ============================================================================
    // align-items: Y axis
    // ==========================================================================
    align-items: stretch; //(Default)
    align-items: flex-start;
    align-items: flex-end;
    align-items: center;
    align-items: baseline;
  }

```
