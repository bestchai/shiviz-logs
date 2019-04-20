# Twittor

A TOR-based message board application

There are nodes that act as relay nodes and there are host servers that act as a
message board. A client can connect to a (relay) node and send a
message via a certain route to the host server. Onion routing is used
to send messages to the host server, so that the author of the message
is not obvious to anyone spying on the traffic (when the network is
saturated enough). There are a total of 5 relay nodes and the message
will go through only 2 other nodes (3 if you include the first node to
which the client was connected).

The difference between executions is that the set of relay nodes differ
in the executions.


Parsing regexp: ```(?<host>\S*) (?<clock>{.*})\n(?<event>.*)```
