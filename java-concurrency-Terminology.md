from https://vijay-vk.github.io/java-concurrency/terminology.html

# 并发（Concurrency） vs. 并行（Parallelism）
  并发和并行性是相关的概念，但是有很小的差异。  
  并发意味着即使两个或多个任务可能未同时执行，它们也正在取得进展。例如，这可以通过时间分片来实现，在时间分片中，部分任务按顺序执行并与其他任务的一部分混合。  
  另一方面，当执行可以真正同时执行时，就会出现并行性。  

![并发vs并行](https://vijay-vk.github.io/java-concurrency/images/parallel.png)

From https://medium.com/@deepshig/concurrency-vs-parallelism-4a99abe9efb8  
From https://doc.akka.io/docs/akka/2.5/general/terminology.html  

# 同步（Synchronous） vs. 异步（Asynchronous）
  如果在方法返回值或引发异常之前调用者无法取得进展，则该方法调用被视为同步。  
  另一方面，异步调用允许调用者在有限数量的步骤后继续进行，并且该方法的完成可以通过一些其他机制来发出信号（可能是已注册的回调，Future或消息）。  
![同步vs异步](https://vijay-vk.github.io/java-concurrency/images/async.png)  
From http://tutorials.jenkov.com/software-architecture/index.html  
From https://doc.akka.io/docs/akka/2.5/general/terminology.html  

# 非阻塞（Non-blocking） vs. 阻塞（Blocking）  
  如果一个线程的延迟可以无限期地增加其他一些线程的延迟，我们考虑到阻塞的问题。  
  一个很好的例子是由一个线程使用互斥的方式使用资源。  
  如果线程无限期地占用资源（例如，意外运行无限循环），则等待该资源的其他线程将无法进行。相反，非阻塞意味着没有线程能够无限期地延迟其他线程。  
![阻塞vs非阻塞](https://vijay-vk.github.io/java-concurrency/images/io.png)  
From http://tutorials.jenkov.com/java-nio/nio-vs-io.html  
From https://doc.akka.io/docs/akka/2.5/general/terminology.html  

# 进程（Process） vs. 线程（Threads）
  一个进程可以包含多个线程。进程和线程之间的最大区别是，每个进程都有自己的地址空间，而（同一进程的）线程在共享内存空间中运行。  
![进程vs线程](https://vijay-vk.github.io/java-concurrency/images/process.jpg)  
From https://i4mk.wordpress.com/2013/03/13/processes-vs-threads/
