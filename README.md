# assignment-2-carlangelo-hernandez

**. Why is message passing required in distributed systems?**
Within distributed systems, individual processes operate in isolation without access to a common memory space, which prevents them from directly reading or modifying each other's data. To overcome this barrier, these processes rely on message passing as their primary communication mechanism, exchanging specific packets of information to stay synchronized. This interaction is vital; without a structured way to send and receive data, independent nodes would be unable to coordinate their efforts or combine their results into a unified task.

**2. What happens if one process fails?**
In a distributed environment, a single process failure can lead to a systemic deadlock where surviving processes hang indefinitely while awaiting data that will never arrive. Because standard Message Passing Interface (MPI) implementations typically lack built-in fault tolerance or automatic recovery protocols, such a stall often forces the entire application to crash or terminate prematurely.

**3. How does this model differ from shared-memory programming?**
Message-passing and shared-memory represent two distinct approaches to process communication. In message-passing systems, processes remain isolated and interact solely through the exchange of data packets, as they lack a common memory pool. Conversely, shared-memory programming allows multiple processes to inhabit the same memory space for direct data access, which often yields higher performance. However, this speed comes with the added complexity of synchronization; without strict management, simultaneous data modifications by different processes can lead to significant errors or data corruption.
