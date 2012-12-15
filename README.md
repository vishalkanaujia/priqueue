priqueue
========

A priority queue with O(1) operations: C, Linux implementation

I have implemented a priority queue that enable O(1) time complexity for major operations i.e. enqueue and dequeue.
It is C, POSIX compliant code.

Things to note
- It uses buffer pools
- Its behavior is to return the highest priority node from the queue
- If queue is empty/full, we use conditional waits
- Priorities are defined from 0..PRIMAX-1 as an array
- Each priority bucket has a list of node that share that priority
- It is thread-safe implementation
- It could be used between two threads for data exchange (producer/consumer)
