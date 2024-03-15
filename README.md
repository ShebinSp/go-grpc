A simple grpc server written in Go with all four types of streams.

gRPC is a modern framework developed by Google for building efficient and fast communication systems between different software applications. It stands for "gRPC Remote Procedure Call".

Here's a simple explanation:

Imagine you have two computers, and you want them to talk to each other over the internet. Traditionally, this might involve sending messages back and forth in a way that both computers can
understand. gRPC makes this process easier by providing a way for computers to communicate using a standardized set of rules and procedures.

In more technical terms, gRPC uses a special kind of communication called Remote Procedure Calls (RPCs). RPCs allow one computer to call functions or procedures on another computer as if they
were local, meaning the programmer doesn't have to worry about the nitty-gritty details of network communication.

gRPC also uses a language-agnostic data serialization system called Protocol Buffers to efficiently encode and decode data being sent between computers. This makes it easy for applications
written in different programming languages to communicate with each other seamlessly.

Overall, gRPC simplifies the process of building distributed systems by providing developers with a powerful and easy-to-use framework for defining and implementing communication protocols
between their applications.


The four types of streams are :

1. Unary RPC
  * Unary RPC is the smallest form of communication in gRPC.
  * It involves a single request from the client to the server and single response from the server to the client.
  * This type of communication is similar to  traditional HTTP request-response interactions.

2. Server Streaming RPC
  * In server streaming RPC, the client sends a single request to the server, and the server responds with a stream of messages.
  * The server sends multiple messages back to the client over a single connection.
  * The client reads the stream of messages until the server indicates that it has finished sending them.

3. Client Streamin RPC
  * In client streaming RPC, the client sends a stream of messages to the server, and the server responds with a single message.
  * The client sends multiple messages over a single connection to the server.
  * Once the client has finished sending messages, it waits for the server to responds with a single message.

4. Bidirectional Steaming RPC
  * Bidirectional streaming RPC involves both the client and server sending stream of messages to each other.
  * The client and server communicate asynchronously, with each side sending and receiving messages independently.
  * This type of communication is useful for scenarios where both sides need to send and receive data concurrently.

* To generate greet_grpc.pb.go & greet.pb.go codes, use the command : protoc --go_out=. --go-grpc_out=. proto/greet.proto
