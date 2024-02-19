# How to Center a DIV without knowing the parent's width

Today I'd like to demonstrate how you can center a `div` inside of its parent `div`, without needing to know the `width` or the `height` of its parent.

HTML:

```html
<!doctype html>
<html lang="en-us">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />

        <title>Centering a DIV</title>
    </head>
    <body>
        <div id="container">
            <div id="sub-container">
                <p>Hello.</p>
            </div>
        </div>
    </body>
</html>
```

CSS:

```css
#container {
    display: table;
    
    background-color: rgb(245, 245, 245);
    border-radius: 7px;
    
    width: 220px;
    height: 128px;

    padding: 12px;
}

#sub-container {
    display: table-cell;

    background-color: khaki;
    border-radius: 7px;

    padding: 12px;
}
```

Most of the code above is not necessary; it's just there to make the `div`s look nice. What we're looking out for here are the `display` properties for both `div`s.

The parent `div`, called `container`, has its `display` property set to `table`. All we need to do now, in order to center the `sub-container` `div` horizontally is to set its `display` property to `table-cell`.
