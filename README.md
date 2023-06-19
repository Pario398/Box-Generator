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

### boxGenerator()

This function generates the specified number of boxes with random background colors and displays them in the `div` with the `id="container"`. The boxes are created using jQuery and are appended to the container.
