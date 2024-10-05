Java's Stream API provides a functional approach to processing collections of objects. Stream APIs deal with data by abstracting it, providing a common way to read and write data stored in various ways. Stream APIs, therefore, allow you to handle not only arrays or collections, but also data stored in files in the same way.

Stream API is **not related** to Java I/O streams.
# Stream API feature
1. Unlike collections that work through external iterations, streams work through internal iteration.
2. Unlike reusable collections, streams can only be used once.  
3. The stream does not change the original data.  
4. The operation of the stream uses a filter-map-based API to optimize performance through a delay operation.  
5. Stream supports easy parallelism with `parallelStream()` methods.
# Stream API workflow
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*QCmZZpGs_rcF5y2-.png)
1. Generation of streams  
2. Intermediation of streams (transformation of streams)  
3. Final operation of stream (use of stream)


---
Reference link 🙂       
https://medium.com/analytics-vidhya/java-stream-api-with-examples-part-1-279c8804981f