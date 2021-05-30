# Exceptions

The library contains many exceptions to adapt to your needs:

```
ICMPLibError
 ├─ NameLookupError
 ├─ ICMPSocketError
 │  ├─ SocketAddressError
 │  ├─ SocketPermissionError
 │  ├─ SocketUnavailableError
 │  ├─ SocketBroadcastError
 │  └─ TimeoutExceeded
 │
 └─ ICMPError
    ├─ DestinationUnreachable
    │  ├─ ICMPv4DestinationUnreachable
    │  └─ ICMPv6DestinationUnreachable
    │
    └─ TimeExceeded
       ├─ ICMPv4TimeExceeded
       └─ ICMPv6TimeExceeded
```

### ICMPLibError

Exception class for the icmplib package.

### NameLookupError

Raised when the requested name does not exist or cannot be resolved. This concerns both Fully Qualified Domain Names and hostnames.

### ICMPSocketError

Base class for ICMP sockets exceptions.

### SocketAddressError

Raised when the requested address cannot be assigned to the socket.

### SocketPermissionError

Raised when the privileges are insufficient to create the socket.

### SocketUnavailableError

Raised when an action is performed while the socket is closed.

### SocketBroadcastError

Raised when a broadcast address is used and the corresponding option is not enabled on the socket.

### TimeoutExceeded

Raised when a timeout occurs on a socket.

### ICMPError

Base class for ICMP error messages.

### DestinationUnreachable

Base class for ICMP Destination Unreachable messages.

Destination Unreachable message is generated by the host or its inbound gateway to inform the client that the destination is unreachable for some reason.

### TimeExceeded

Base class for ICMP Time Exceeded messages.

Time Exceeded message is generated by a gateway to inform the source of a discarded datagram due to the time to live field reaching zero. A Time Exceeded message may also be sent by a host if it fails to reassemble a fragmented datagram within its time limit.