# PhoneNumberJSFormatting

This code snippet provides functionality to format a phone number input field in a specific format while allowing only numeric values and certain special keys. The code enforces a US phone number format `(XXX) XXX - XXXX` for the input value.

## Key Functions

### `isNumericInput(event)`
This function checks whether the key pressed is a numeric value from either the number line or the number pad. It returns `true` if the key is a numeric value, and `false` otherwise.

### `isModifierKey(event)`
This function checks for special keys that allow modifying the input field, such as Shift, Home, End, as well as keys for editing the text, such as Backspace, Enter, etc. Additionally, it allows specific combinations of Control/Command key and A/C/V/X/Z. It returns `true` if the key is a modifier key, and `false` otherwise.

### `enforceFormat(event)`
This function is triggered on the `keydown` event and prevents events that are neither numeric values nor modifier keys. It cancels the event if the key pressed does not match the expected criteria.

### `formatToPhone(event)`
This function is triggered on the `keyup` event and formats the input value into a US phone number format. It extracts the first ten digits (area code, prefix, and line number) from the input and places them in the specified format. If the input contains more than six digits, it formats the number as `(XXX) XXX - XXXX`. If the input has more than three digits but less than seven, it formats the number as `(XXX) XXX`. If the input has at least one digit but less than four, it formats the number as `(XXX)`.

## Usage

To use this phone number formatting code, follow these steps:

1. Include the provided `<script>` tag in your HTML file or template.
2. Add an input element with the ID `phonenumber` to the desired location in your HTML.
   ```html
   <input type="text" id="phonenumber" name="phonenumber">
   ```
3. The code will automatically add event listeners for both the `keydown` and `keyup` events on the `phonenumber` input element.
4. When users enter a phone number in the input field, it will be formatted in real-time according to the US phone number format.

## Additional Functions

This code snippet also includes two additional functions that can be used separately:

### `handleKeyDown(event)`
This function logs the key pressed by the user to the console. It can be used as an event handler for the `keydown` event on any element.

### `handleBlur()`
This function triggers the `focus()` method on an element with the ID `myInput` when the associated element loses focus. It can be used as an event handler for the `blur` event on any element.

Feel free to customize and integrate these additional functions into your project as needed.

## Author: Austen James Green
