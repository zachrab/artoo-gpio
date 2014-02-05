# Commands

## on → true | nil

Public: Turns LED on.

Returns true | nil

## off → true | nil

Public: Turns LED off.

Returns true | nil

## on? → true | false

Public: Returns true if LED is on, otherwise returns false.

Returns true | false

## off? → true | false

Public: Returns true if LED is off, otherwise returns false.

Returns true | false

## toggle → true | nil

Public: Turns the LED on, or off, depending on if it is already off, or on, respectively.

Returns true | nil

## brightness(brightness_int) → true | nil

Public: Sets brightness of the led to the specified brightness value passed to brightness(brightness_int) using PWM, brightness can be any integer value between `0` and `255`.

- **brightness_int** - params , the brightness value

Returns true | nil