<h1>Services that a Transport-layer can offer</h1>

<h2>Reliable Data Transfer</h2>

For many applications data loss can have devastating consequences. If a protocol
provides a guaranteed data delivery service, it is said to provide **reliable
data transfer**. One important service that a transport-layer protocol can 
potentially provide to an application is process-to-process reliable data 
transfer. The sending process then can pass its data to the socket and know 
for sure that data will arrive without errors at the receiving process. 

<h2>Throughput</h2>

Available throughput, in the context of a communication session between two 
processes along a network path, is the rate at which the sending process can 
deliver bits to the receiving process. Transport-layer protocol can provide 
guaranteed available throughput at some specified rate. 

<h2>Timing</h2>

A transport-layer protocol can also timing guarantees. These can come in many 
different shapes and forms. An example might be that every bit that the sender
pumps into socket arrives at the receiver's socket no more than 100 msec later. 

<h2>Security</h2>

Transport-layer protocol can provide an application with one or more security 
services. For example, in the sending host, a transport protocol can encrypt 
all data transmitted by the sending process, and in the receiving host, 
the transport-layer procotol can decrypt the data before delivering the data to 
the receiving process. 
