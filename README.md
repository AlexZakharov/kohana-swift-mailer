# Email Module For Kohana 3.3

__Attention!__ This module is very different from the original module. The structure
of this module has been heavily reworked to be more in line with the principles
used in Kohana.

## Installation

Edit your bootstrap file `APPPATH/bootstrap.php` and enable sender module:

~~~
Kohana::modules(array(
  // Some modules
  'sender' => MODPATH.'sender',
  // Some other modules
  ));
~~~

Then copy `MODPATH/sender/config/sender.php` to `APPPATH/config/sender.php`.
Well done!

## Example of usage

~~~
Sender::instance()
  ->from('sender@example.com')
  ->to('first.recipient@example.com')
  ->to('second.recipient@example.com', 'Mr. Recipient')
  ->subject('Hi there!')
  ->message('Hi, guys! This is my awesome email.')
  ->send();
~~~

Enjoy, guys!
