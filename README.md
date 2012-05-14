A fork of: http://www.arcfn.com/2009/08/multi-protocol-infrared-remote-library.html

## About
A fork of the above Library to work with the SymaS107 IR helicopter. Cut down to remove unneeded functionality.
Uses PWM on pin 3.

## Installation

Add folder to `/Applications/Arduino.app/Contents/Resources/Java/libraries/`
or the windows equivalent.

## Example Usage

Sets throttle at 50% constantly:

    #include <SymaRemote.h>

    IRsend irsend;

    void setup() {
      Serial.begin(300);
    }

    void loop() {
      irsend.sendSyma(0x31, 0x3f, 0x3f, 0x3f, 0x3f);
      delay(100);
    }
