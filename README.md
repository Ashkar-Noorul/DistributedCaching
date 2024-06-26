# DistributedCaching
ASP.NET Core supports both in-memory application-based caching and distributed caching. Unlike in-memory caching, which resides within the application, distributed caching is external to the application. It does not live within the application itself and does not need to be present on the same server.

A distributed cache can be shared by one or more applications, instances, or servers, making it ideal for scenarios where you have multiple instances of your application running. It helps ensure that all instances have consistent data. However, it’s highly recommended placing your distributed cache instance as close to your application as possible to minimize network latency.

Like an in-memory cache, a distributed cache can significantly improve your application’s response time. However, the implementation of a distributed cache is specific to the application, meaning there are multiple cache providers that support distributed caching.

The most popular distributed cache provider is Redis. Redis offer robust features and scalability options, making it suitable for various applications and deployment scenarios.

In this article, we will focus on building an ASP.NET Core application that caches data to a Redis instance, which runs locally on a Docker Container
