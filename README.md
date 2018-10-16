# Hacking STEM [![Build Status](https://travis-ci.org/Microsoft/pxt-hacking-stem.svg?branch=master)](https://travis-ci.org/Microsoft/pxt-hacking-stem)

Support for Hacking STEM activities in https://makecode.microbit.org

## Usage

Go to https://makecode.microbit.org, click on the gearwheel menu and select ``Add Package``, search for ``hacking stem`` and select this package.

## Reference

### ``serial.writeMilliNumber`` #serialWriteMilliNumber

The ``||serial:write milli number||`` block scales the input value by 1000 and writes it to the serial as a floating point number.

```sig
serial.writeMilliNumber(1);
```

For example,

```blocks
serial.writeMilliNumber(1);
```

writes the following number to serial

    0.001

This example reads the analog signal on pin ``P0``, scales it to 3.3v and writes it to serial.

```blocks
let mv = 0
basic.forever(() => {
    mv = pins.analogReadPin(AnalogPin.P0) * 3300 / 1023
    serial.writeMilliNumber(mv)
})
```

## License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the [MIT](LICENSE) License.

## Supported targets

* for PXT/microbit
(The metadata above is needed for package search.)


## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
