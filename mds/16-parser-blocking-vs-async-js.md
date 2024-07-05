## Adding Interactivity with JavaScript 

 JavaScript allows us to modify just about every aspect of the page: content, styling, and its response to user interaction. However, JavaScript can also block DOM construction and delay when the page is rendered. To deliver optimal performance, make your JavaScript async and eliminate any unnecessary JavaScript from the critical rendering path.

- JavaScript can query and modify the DOM and the CSSOM.
- JavaScript execution blocks on the CSSOM.
- JavaScript blocks DOM construction unless explicitly declared as async.

JavaScript is a dynamic language that runs in a browser and allows us to alter just about every aspect of how the page behaves: we can modify content by adding and removing elements from the DOM tree; we can modify the CSSOM properties of each element; we can handle user input; and much more.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <link href="style.css" rel="stylesheet" />
    <title>Critical Path: Script</title>
  </head>
  <body>
    <p>Hello <span>web performance</span> students!</p>
    <div><img src="awesome-photo.jpg" /></div>
    <script>
      var span = document.getElementsByTagName('span')[0];
      span.textContent = 'interactive'; // change DOM text content
      span.style.display = 'inline'; // change CSSOM property
      // create a new element, style it, and append it to the DOM
      var loadTime = document.createElement('div');
      loadTime.textContent = 'You loaded this page on: ' + new Date();
      loadTime.style.color = 'blue';
      document.body.appendChild(loadTime);
    </script>
  </body>
</html>
```

First, notice that in the above example our inline script is near the bottom of the page. Why? Well, you should try it yourself, but if we move the script above the span element, you'll notice that the script fails and complains that it cannot find a reference to any span elements in the document; that is, getElementsByTagName(‘span') returns null.

- - - - - 

## Async 


```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <link href="style.css" rel="stylesheet" />
    <title>Critical Path: Script Async</title>
  </head>
  <body>
    <p>Hello <span>web performance</span> students!</p>
    <div><img src="awesome-photo.jpg" /></div>
    <script src="app.js" async></script>
  </body>
</html>
```

Adding the async keyword to the script tag tells the browser not to block DOM construction while it waits for the script to become available, which can significantly improve performance.
