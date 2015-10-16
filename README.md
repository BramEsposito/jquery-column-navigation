# jquery-column-navigation
jQuery plugin to provide a column hierarchy navigation from a list

Cloned from: https://code.google.com/p/jquery-column-navigation/

----

Column Navigation provides a Mac OS X/NeXTStep style navigation for ordered and unordered HTML lists.

It has been designed to progressively enhance list information by refactoring it into columns of data. Each column represents the children of the proceeding selected item.

This is especially useful for formatting long hierarchy structures.

# Quick Example
The column navigation plugin is very quick an easy to use. It provides a very fast way to arrange and interface with large hierarchial sets of data in a familiar interface, especially for Mac OS X users.

You require a unordered list currently (more to follow in later versions) with nested unordered lists. Each nesting will create a new level within the tree.

## HTML Example
```html
<html>
<body>
        <ul id="myTree">
                <li>
                        <a href="./">Homepage</a>
                        <ul>
                                <li><a href="./contact">Contact</a></li>
                                <li><a href="./tsandcs">Terms &amp; Conditions</a></li>
                                <li><a href="./privacy">Privacy information</a></li>
                        </ul>
                </li>
                <li>
                        <a href="./contents">Contents</a>
                        <ul>
                                <li><a href="./page1/">Page 1</a></li>
                                <li><a href="./page2/">Page 2</a>
                                        <ul>
                                                <li><a href="./page2.1/">Page 2.1</a></li>
                                                <li><a href="./page2.2/">Page 2.2</a></li>
                                        </ul>
                                </li>
                                <li><a href="./page3/">Page 3</a></li>
                        </ul>
                </li>
        </ul>
</body>
</html>
```

## Javascript Example
```javascript
$("ul#myTree").columnNavigation();
```
## Options
This plugin takes a large number of configuration options, all are defaulted for quick access. You can control the styling properties of almost every attribute of style and animation.

All configuration items should be declared on initialisation.
```javascript
$("div#myTree").conlumnNavigation({
        containerBackgroundColor                : "rgb(255,255,255)",
        columnFontFamily                        : "Arial,sans-serif",
        columnScrollVelocity                    : 400,
        callBackFunction                        : function() {
                alert( $(linkObject).attr("href") );
        }
});
```
The example above sets some attributes on the column navigation object.

Notice the callBackFunction. You can attach an additional function to act. The callback function can be called on the dblClick event if you supply one, the 'a' element is passed as the object to your handler.
