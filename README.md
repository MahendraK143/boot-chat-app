# boot-chat-app
Using ActiveMQ and STOMP(Simple text oriented message protocol) and Websocket
https://www.javainuse.com/spring/boot-websocket-chat
https://www.javainuse.com/misc/rabbitmq-hello-world
For this tutorial we will be making use of STOMP protocol. STOMP is a simple text-oriented messaging protocol used by our UI Client(browser) to connect to enterprise message brokers.
Clients can use the SEND or SUBSCRIBE commands to send or subscribe for messages along with a "destination" header that describes what the message is about and who should receive it.
It defines a protocol for clients and servers to communicate with messaging semantics. It does not define any implementation details, but rather addresses an easy-to-implement wire protocol for messaging integrations. The protocol is broadly similar to HTTP, and works over TCP using the following commands:
CONNECT
SEND
SUBSCRIBE
UNSUBSCRIBE
BEGIN
COMMIT
ABORT
ACK
NACK
DISCONNECT

Lets Begin-
------------------
Since RabbitMQ is built on top of Erlang, we will first need to install Erlang. Got to the Erlang downloads page and download the erlang binary file for windows which is an executable.
https://www.erlang.org/downloads
after downloading exe application using run as administation to avoid installation issues.

Next run the binary file downloaded and install erlang on your machine.
Go to RabbitMQ downloads page and download RabbitMQ installation.

https://www.rabbitmq.com/install-windows.html

This will be a .exe installation file for windows.
Run this exe and install RabbitMQ on your machine.
We will now start Rabbit. The above installation should have installed the RabbitMQ command prompt. Open it.
Go to the RabbitMQ Server Location and use the command as follows-
>rabbitmq-server start

Next we will install the RabbitMQ plugin which will give use the RabbitMQ Management Console which is accessible using the browser. For this use the command as follows-
>rabbitmq-plugins.bat enable rabbitmq_management

Next go to localhost:15672.We will see the RabbitMQ console. The default username and password is guest.
We are done with installation of RabbitMQ.
Next
We will need to perform one additional step with RabbitMQ - Install STOMP plugin for RabbitMQ so that it can work with STOMP Messages
RabbitMQ STOMP Plugin
>rabbitmq-plugins.bat enable rabbitmq_stomp

