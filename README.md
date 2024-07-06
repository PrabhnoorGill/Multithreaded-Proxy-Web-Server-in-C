HTTP Proxy Server in C

Welcome to the HTTP Proxy Server project! This repository contains a lightweight and efficient HTTP proxy server implemented in C. The server acts as an intermediary for requests from clients seeking resources from other servers.
Features

    Request Forwarding: Intercepts and forwards HTTP requests from clients to the target server.
    Response Handling: Receives responses from the target server and forwards them back to the clients.
    Caching: Implements basic caching mechanisms to store frequently accessed resources for quicker response times.
    Logging: Logs client requests and server responses for monitoring and debugging purposes.
    Concurrency: Supports handling multiple client connections simultaneously using multi-threading and semaphore-based synchronization.

Implementation Details
Multi-threading

    Semaphore-based Synchronization: Utilizes semaphores instead of condition variables for thread synchronization.
    Thread Management: Employs pthread_join() and pthread_exit() for thread management. Semaphores' sem_wait() and sem_post() are used as they don't require passing the thread ID, simplifying synchronization.

Motivation and Goals

    Understanding Network Requests: Gain insights into how requests from a local machine reach a server.
    Handling Concurrent Requests: Learn to manage multiple client requests simultaneously.
    Concurrency Locking: Explore locking mechanisms for concurrency control.
    Caching Concepts: Delve into caching mechanisms used by browsers and implement an LRU cache.

Proxy Server Benefits

    Performance Enhancement: Speeds up processes and reduces server-side traffic.
    Access Control: Can be configured to restrict access to specific websites.
    Anonymity: A good proxy can mask the client's IP, enhancing privacy.
    Security: Proxies can be modified to encrypt requests, enhancing security.

Operating System Components

    Threading
    Locks
    Semaphores
    Cache (using LRU algorithm)

Limitations

    Cache Duplication: If a URL generates multiple clients, each response is stored separately, potentially causing incomplete retrieval.
    Fixed Cache Size: Large websites may not fit in the cache due to size constraints.

Future Enhancements

    Multiprocessing: Implement multiprocessing for improved parallelism and speed.
    Access Control: Extend the code to control access to specific types of websites.
    POST Requests: Add support for handling POST requests.
