- The render tree captures both the content of the webpage (as represented by the DOM) and the styles (as represented by the CSSOM)

## Content (DOM Tree)
- The DOM (Document Object Model) tree is a hierarchical representation of the HTML document. Each node in the DOM tree corresponds to an element or a piece of content in the HTML document.

## Styles (CSSOM Tree):
- The CSSOM (CSS Object Model) tree is a hierarchical representation of all the CSS rules that apply to the elements in the DOM tree.

## Render Tree:
- The render tree is created by combining the DOM tree and the CSSOM tree.
- The render tree excludes nodes that do not affect the layout, such as <head>, <script>, and elements with display: none.
