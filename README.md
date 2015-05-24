# UDPPinger
This program:
1. sends and receives datagram packets using UDP sockets
2. sets a proper socket timeout

The ping protocol allows a client machine to send a packet of data to a remote machine, and have the remote machine return the data back to the client unchanged (an action referred to as echoing). Among other uses, the ping protocol allows hosts to determine round-trip times to
other machines.

The complete code for the Ping server (UDPPingerServer.py) was provided by the course. 30% of the client’s packets are simulated to be lost. The server sits in an infinite loop listening for incoming UDP packets. When a packet comes in and if a randomized integer is greater than or equal to 4, the server simply capitalizes the encapsulated data and sends it back to the client.

The client code was made to implement the following:
1. The client sends 10 pings to the server
2. The client waits up to one second for a reply
3. If reply within one second, the program prints the response message from server and calculates and prints the round trip time in seconds, of each packet
4. If no reply within one second, the program assumes that the packet was lost during transmission across the network and prints “Request timed out”
