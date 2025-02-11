# Keypad

Post Lab Qns
(a) Do all keypresses show up on the display?
Answer: Yes, keypresses are detected and updated dynamically on the LCD.

(b) How do you debounce the keypresses?
Answer: A software debouncing mechanism is implemented by:
  Adding a small delay before registering a keypress.
  Ensuring that the key is released before accepting another press.

(c) Explain the keyscan algorithm.
Answer: The algorithm:
  Drives one row LOW at a time while keeping others HIGH.
  Reads column values to check which key is pressed.
  Uses a lookup table to map row-column combinations to key values.
  Debounces the input before displaying the key on the LCD.

(d) Why did we need external pullup resistors instead of the built-in ones?
Answer: Internal pull-ups in STM32 are weak (~40kΩ), causing unreliable key detection.
  Using 2.2kΩ external pull-ups ensures stable and accurate keypress recognition.
