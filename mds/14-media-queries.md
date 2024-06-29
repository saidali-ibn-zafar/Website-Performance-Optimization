## Media Queries

- Media queries let you create a responsive experience that applies specific styles to specific screen size. Queries for screen size can test for the following things:

  - width (min-width, max-width)
  - height (min-height, max-height)
  - orientation
  - aspect-ratio

```css
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Media Queries Example</title>
  <style>
    body {
      margin: 0;
      padding: 20px;
      font-family: Arial, sans-serif;
      transition: background-color 0.5s, font-size 0.5s;
    }

    /* Width-based media queries */
    @media (min-width: 600px) {
      body {
        background-color: lightblue;
      }
    }

    @media (max-width: 599px) {
      body {
        background-color: lightgreen;
      }
    }

    /* Height-based media queries */
    @media (min-height: 800px) {
      body {
        font-size: 18px;
      }
    }

    @media (max-height: 799px) {
      body {
        font-size: 14px;
      }
    }

    /* Orientation-based media queries */
    @media (orientation: landscape) {
      body {
        background-color: lightcoral;
      }
    }

    @media (orientation: portrait) {
      body {
        background-color: lightgoldenrodyellow;
      }
    }

    /* Aspect-ratio-based media queries */
    @media (min-aspect-ratio: 16/9) {
      body {
        background-color: lightpink;
      }
    }

    @media (max-aspect-ratio: 4/3) {
      body {
        background-color: lightseagreen;
      }
    }

    /* Combined media query */
    @media (min-width: 600px) and (orientation: landscape) {
      body {
        background-color: lightcyan;
      }
    }
  </style>
</head>
<body>
  <h1>Responsive Design with Media Queries</h1>
  <p>Resize the browser window or change the device orientation to see the effect of the media queries.</p>
</body>
</html>

```
