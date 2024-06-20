# DOM, CSSOM, and Render Tree

## DOM (Document Object Model)
- **Definition**: A tree structure representing the HTML content of a web page.
- **Structure**: Nodes representing elements, attributes, and text.
- **Purpose**: Provides an interface for scripts to update the document content and structure.

## CSSOM (CSS Object Model)
- **Definition**: A tree structure representing the CSS styles of a web page.
- **Structure**: Nodes representing CSS rules and their properties.
- **Purpose**: Provides an interface for scripts to update the styles and allows the browser to apply styles to the DOM.

## Render Tree
- **Definition**: A tree structure that combines the DOM and CSSOM.
- **Structure**: Nodes representing the visual elements to be displayed, excluding non-visual elements (`display: none`).
- **Purpose**: Used by the browser to paint content on the screen.

## Process of Creating the Render Tree
1. **Parsing HTML**: The browser parses the HTML and constructs the DOM.
2. **Parsing CSS**: The browser parses the CSS and constructs the CSSOM.
3. **Creating the Render Tree**: The browser combines the DOM and CSSOM, including only the visible elements with applied styles.
