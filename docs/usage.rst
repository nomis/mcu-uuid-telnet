Usage
=====

.. code:: c++

   #include <uuid/telnetd.h>

Create a |uuid::telnetd::TelnetService|_ and call |start()|_.

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

.. literalinclude:: ../examples/Example.cpp

.. |uuid::telnetd::TelnetService| replace:: ``uuid::telnetd::TelnetService``
.. _uuid::telnetd::TelnetService: https://mcu-doxygen.uuid.uk/classuuid_1_1telnetd_1_1TelnetService.html

.. |start()| replace:: ``start()``
.. _start(): https://mcu-doxygen.uuid.uk/classuuid_1_1telnetd_1_1TelnetService.html#TODO

.. |loop()| replace:: ``loop()``
.. _loop(): https://mcu-doxygen.uuid.uk/classuuid_1_1telnetd_1_1TelnetService.html#TODO

.. |uuid::console::Shell::loop_all()| replace:: ``uuid::console::Shell::loop_all()``
.. _uuid::console::Shell::loop_all(): https://mcu-doxygen.uuid.uk/classuuid_1_1console_1_1Shell.html#affe5b4812696a9a53eed1f394301354e
