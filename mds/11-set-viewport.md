# Setting the Viewport for Responsive Web Design

Pages optimized for a variety of devices must include a meta viewport tag in the head of the document. This tag tells the browser how to control the page's dimensions and scaling.

## Importance of the Viewport Meta Tag

To provide the best experience, mobile browsers render the page at a desktop screen width (usually about 980px, though this varies across devices). They then try to make the content look better by increasing font sizes and scaling the content to fit the screen. This can make fonts look inconsistent and require users to zoom in to see and interact with the content.

### Example Meta Viewport Tag

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    …
    <meta name="viewport" content="width=device-width, initial-scale=1">
    …
  </head>
  …
```

- - - - 
# Understanding `initial-scale=1` in the Viewport Meta Tag

## What It Does

The `initial-scale=1` value in the viewport meta tag is used to set the initial zoom level when a web page is first loaded. This value tells the browser to set a 1:1 relationship between CSS pixels and device-independent pixels (DIP). Essentially, this means that one CSS pixel will be equal to one DIP.

## Why It's Important

1. **Consistent Rendering**: By setting `initial-scale=1`, you ensure that your web page appears at a natural size, without being zoomed in or out, regardless of the device's screen size.
2. **Full Landscape Width**: This value helps ensure that when the device is rotated to landscape mode, the page takes advantage of the full width available.
3. **User Experience**: Users will not need to zoom in or out to read text or interact with elements on the page, making for a more comfortable and accessible browsing experience.

## Example Usage

Here is how you would include it in the HTML document:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    …
  </head>
  …
</html>
```
- - - - -

In addition to initial-scale, the minimum-scale, maximum-scale, and user-scalable attributes are also available. We don't recommend using these attributes because they can prevent the user from zooming the viewport, potentially causing accessibility issues.

- width=device-width: Sets the width of the page to the width of the device.
- initial-scale=1: Sets the initial zoom level to 1:1.
- maximum-scale: Controls the maximum zoom level.
- minimum-scale: Controls the minimum zoom level.
- user-scalable: Controls whether users can zoom the page.
