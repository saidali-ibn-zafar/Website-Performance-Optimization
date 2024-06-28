## Images

An image with fixed dimensions causes the page to scroll if it's larger than the viewport. We recommend giving all images a max-width of 100%, which shrinks images to fit the available space while preventing them from stretching beyond their initial size.

you can do:

```css
img {
  max-width: 100%;
  display: block;
}
```

Even when you set max-width: 100%, we still recommend adding width and height attributes to your <img> tags so the browser can reserve space for images before they load. This helps prevent layout shifts.

- - - - - 

## Layout
  ### Flexbox 
  - Use Flexbox when you have a set of items of different sizes and you want them to fit comfortably in a row or multiple rows, with smaller items taking up less space and larger ones taking more space.

    ```css
    .items {
    display: flex;
    justify-content: space-between;
    }
    ```

    ![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/aa342464-5fd3-4139-87b5-43019e55a347)


## CSS Grid Layout
  - CSS Grid Layout creates flexible grids. You can improve the earlier floated example using use grid layout and the fr unit, which represents a portion of the available space in the container.

    ```css
    .container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    }
    ```

    ![image](https://github.com/saidali-ibn-zafar/Website-Performance-Optimization/assets/120341849/d49d20e9-ca86-4eb8-a565-27eff541e6db)
