# Box Generator

This HTML file generates a specified number of boxes with random background colors.

## How it works

1. The user enters the number of boxes they want to generate in the input field with the `id="boxNum"`.
2. The user clicks the button with the `id="draw"` to generate the boxes.
3. The `boxGenerator()` function is called when the button is clicked.
4. The `boxGenerator()` function uses the `colorGenerator()` function to generate random background colors for each box.
5. The boxes are created and displayed in the `div` with the `id="container"`.

## Functions

### colorGenerator()

This function generates and returns a random hexadecimal color code.
```jQuery
function colorGenerator() {
            var letters = '0123456789ABCDEF';
            var color = '#';
            for (var i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }
```

### boxGenerator()

This function generates the specified number of boxes with random background colors and displays them in the `div` with the `id="container"`. The boxes are created using jQuery and are appended to the container.
```jQuery
function boxGenerator() {
            var temp = "";
            var margin = 5;
            var container = $("#container");
            var number = $("#boxNum").val();
            container.html("");
            for (var start = 1; number >= start; start += 1) {
                temp = colorGenerator()
                firstBox = $("<div></div>");
                firstBox.addClass("box");
                firstBox.html(start);
                firstBox.css("background-color", temp);
                firstBox.css("margin-left", margin + "px");
                container.append(firstBox);
                margin = margin * 2;
            }
        }
```
