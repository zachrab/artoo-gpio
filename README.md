# Artoo Drivers For GPIO Devices

This repository contains the Artoo (http://artoo.io/) standard drivers for analog, digital, PWM, and servo devices.

Artoo is a open source micro-framework for robotics using Ruby.

For more information abut Artoo, check out our repo at https://github.com/hybridgroup/artoo

[![Code Climate](https://codeclimate.com/github/hybridgroup/artoo-gpio.png)](https://codeclimate.com/github/hybridgroup/artoo-gpio) [![Build Status](https://travis-ci.org/hybridgroup/artoo-gpio.png?branch=master)](https://travis-ci.org/hybridgroup/artoo-gpio)

## Installing

```
gem install artoo-gpio
```

## Using

Normally, this gem is automatically included as part of using an Artoo adaptor that can connect to your hardware. For example, artoo-arduino and artoo-digispark both make use of the drivers in this gem. 

Here is the "led" driver being used in an Arduino:

```ruby
require 'artoo'

connection :arduino, :adaptor => :firmata, :port => '127.0.0.1:8023'
device :led, :driver => :led, :pin => 13

work do
  every 1.second do
    led.toggle
  end
end
```

Here is the same "led" driver being used by a Digispark.

```ruby
require 'artoo'

connection :digispark, :adaptor => :littlewire, :vendor => 0x1781, :product => 0x0c9f
device :led, :driver => :led, :pin => 1

work do
  every 1.second do
    led.toggle
  end
end
```

## Devices supported

The following GPIO hardware devices have Artoo driver support:
- Button
- LED
- Maxbotix ultrasonic range finder
- Analog sensor
- Motor (DC)
- Servo


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
