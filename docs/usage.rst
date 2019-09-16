Usage
=====

.. code:: c++

   #include <uuid/telnet.h>

Create a |uuid::telnet::TelnetService|_ and call |start()|_.

Call |loop()|_ regularly and when WiFi connectivity is available
connections will be accepted.

Call |uuid::console::Shell::loop_all()|_ regularly to process open
connections.

The `binary <https://tools.ietf.org/html/rfc856>`_, `echo
<https://tools.ietf.org/html/rfc857>`_ and `suppress go ahead
<https://tools.ietf.org/html/rfc858>`_ telnet `options
<https://tools.ietf.org/html/rfc855>`_ will be negotiated.

Example
-------

.. literalinclude:: ../examples/DigitalIO.cpp

.. |uuid::telnet::TelnetService| replace:: ``uuid::telnet::TelnetService``
.. _uuid::telnet::TelnetService: https://mcu-doxygen.uuid.uk/classuuid_1_1telnet_1_1TelnetService.html

.. |start()| replace:: ``start()``
.. _start(): https://mcu-doxygen.uuid.uk/classuuid_1_1telnet_1_1TelnetService.html#aa3f64dc0c3b0b8f561c004bdeb5dbcb7

.. |loop()| replace:: ``loop()``
.. _loop(): https://mcu-doxygen.uuid.uk/classuuid_1_1telnet_1_1TelnetService.html#ab08b97b1afc1a8c82de5fe7dac0d890e

.. |uuid::console::Shell::loop_all()| replace:: ``uuid::console::Shell::loop_all()``
.. _uuid::console::Shell::loop_all(): https://mcu-doxygen.uuid.uk/classuuid_1_1console_1_1Shell.html#affe5b4812696a9a53eed1f394301354e
