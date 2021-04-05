# My Tutorial

## Step 1

Make the code start on button_a press
```blocks
input.onButtonPressed(Button.A, function ())
```
## Step 2

Wait for input from the pin
```blocks
while (pins.analogReadPin(AnalogPin.P0) < 5) {
        continue;
    }
```
## Step 3

Save the starttime 
```blocks
Starttime = control.millis()
```
## Step 4

wait for 1 second starting from starttime
```blocks
while (control.millis() < Starttime + 1000) {
        continue;
    }
```
## Step 5

save the value from the pin
```blocks
fev1 = pins.analogReadPin(AnalogPin.P0)
```
## Step 6

wait for and save the maximal value
```blocks
while (pins.analogReadPin(AnalogPin.P0) >= maxpower) {
        maxpower = pins.analogReadPin(AnalogPin.P0)
    }
```
## Step 7

Save the endtime
```blocks
endtime = control.millis() - Starttime
```
## Step 8

Final code
```blocks
input.onButtonPressed(Button.A, function () {
    while (pins.analogReadPin(AnalogPin.P0) < 5) {
        continue;
    }
    Starttime = control.millis()
    basic.showNumber(Starttime / 1000)
    while (control.millis() < Starttime + 1000) {
        continue;
    }
    fev1 = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(fev1 / 100)
    while (pins.analogReadPin(AnalogPin.P0) >= maxpower) {
        maxpower = pins.analogReadPin(AnalogPin.P0)
    }
    endtime = control.millis() - Starttime
    basic.showNumber(endtime / 1000)
    basic.pause(1000)
    basic.showNumber(maxpower / 100)
})
```

> Open this page at [https://theinventor007.github.io/propeller-hardware-tutorial2/](https://theinventor007.github.io/propeller-hardware-tutorial2/)

# Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/theinventor007/propeller-hardware-tutorial2** and import

# Edit this project ![Build status badge](https://github.com/theinventor007/propeller-hardware-tutorial2/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/theinventor007/propeller-hardware-tutorial2** and click import

# Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/theinventor007/propeller-hardware-tutorial2/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
