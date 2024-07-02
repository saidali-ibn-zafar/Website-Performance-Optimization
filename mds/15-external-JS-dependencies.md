Inline Script Approach:
![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/3e79edd3-933b-4a55-9ce6-f7c14c9e6465)

External Script Approach: 
![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/20ded456-1592-4f2c-bb4b-659455816c85)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/24f8aa16-e117-47ef-928d-b336297f5711)

# Explanation of the Diagram

## Build DOM
The browser begins parsing the HTML and building the DOM (Document Object Model).

## Blocked
When the browser encounters the `<script src="write.js"></script>` tag, it must pause DOM construction to fetch and execute the external JavaScript file.

## GET write.js
The browser sends an HTTP request to retrieve the external script `write.js`.

## Response
The browser waits for the server to respond with the contents of `write.js`.

## Run JS
Once the script is received, the browser executes it.

## Continue Building DOM
After executing the script, the browser resumes building the DOM.


--------

__Both Inline and External has pros and cons, as an example I can say that if we work on multiple files then external file can help us to use multiple times, other wise inline also works fine!__

