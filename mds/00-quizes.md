
# CSS Rule Evaluation Speed
![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/129f7421-6c28-4edb-881d-a75e916c02f8)

## Question
Which rule is faster to evaluate?

1. `h1 { font-size: 16px }`
2. `div p { font-weight: 12px }`
3. No difference!

## Answer
`h1 { font-size: 16px }`

## Explanation
### Specificity and Evaluation

1. **`h1 { font-size: 16px }`**:
   - This rule targets all `<h1>` elements directly.
   - The browser only needs to look for `<h1>` tags in the document.

2. **`div p { font-weight: 12px }`**:
   - This rule targets `<p>` elements that are descendants of `<div>` elements.
   - The browser needs to search for all `<div>` elements and then for each `<div>`, look for its descendant `<p>` elements.

### Performance

Evaluating a CSS rule that targets an element directly (like `h1`) is generally faster than evaluating a rule that targets a nested structure (like `div p`). This is because direct element targeting is simpler and requires less computational work than checking for descendant relationships in the DOM tree.

Therefore, the answer is:

**`h1 { font-size: 16px }` is faster to evaluate.**

- - - -

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/1ea877cf-dedb-46ea-9812-39ac86c54b71)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/987cdd31-027c-482e-ba49-dea52d2d0699)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/60b51360-a285-411f-a226-f119c213c317)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/dd93f515-bad3-4928-ac10-e4d6ab47f80b)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/5cf11bce-5ad3-438c-b441-88291e3d493e)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/59beb1d2-e697-4044-aefa-f426a5d24980)

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/a30e67b6-1e6d-47d3-8ae4-124c221a6015)

```html
<p>Awesome page 
  <script>
    document.write(" with JavaScript ")
  </script> 
  is awesome
</p>
```

The `document.write` function inserts the text " with JavaScript " directly into the HTML at the location where the script tag is placed.
- - - -- 

# Script Loading Examples

![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/ef8a80b0-268b-41ac-a842-f40d08980f01)


## Blocking Script

```html
<!DOCTYPE html>
<html>
<head>
    <title>Blocking Script Example</title>
    <!-- Blocking script -->
    <script src="blocking-script.js"></script>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is an example of a blocking script.</p>
</body>
</html>

```

## Inline Script

```html
<!DOCTYPE html>
<html>
<head>
    <title>Inline Script Example</title>
    <!-- Inline script -->
    <script>
        console.log('This is an inline script.');
    </script>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is an example of an inline script.</p>
</body>
</html>

```

## Async Script 

```html
<!DOCTYPE html>
<html>
<head>
    <title>Inline Script Example</title>
    <!-- Inline script -->
    <script>
        console.log('This is an inline script.');
    </script>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is an example of an inline script.</p>
</body>
</html>

```

# Descriptions

## Blocking Script Example:

- The script is loaded synchronously, which means the browser will stop parsing the HTML until the script is fetched and executed.
- This can cause delays in rendering the rest of the HTML if the script takes time to load.

## Inline Script Example:

- The script is embedded directly in the HTML. It is executed immediately when the parser encounters it.
- There are no additional HTTP requests for this script, but it can still delay rendering if it is complex or long.

## Async Script Example:

- The script is fetched asynchronously and executed as soon as it is available.
- The HTML parsing and rendering continue without waiting for the script to load, improving page load performance.

These examples demonstrate how different script loading strategies can impact the behavior and performance of a web page.
