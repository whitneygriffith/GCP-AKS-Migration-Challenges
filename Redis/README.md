# Redis on Azure Notes


### Redis Specific 

[Overview](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-overview)
#### User Story: _As a software engineer I need to provision a cache service in Azure_

**Challenge: Create Azure Cache for Redis service**

[Create Azure Cache](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-java-get-started#create-an-azure-cache-for-redis)

**Challenge: Understand Best Practices**

[Cache Best Practices](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-best-practices)

[Considerations for Implementing Azure Redis Cache](https://docs.microsoft.com/en-us/azure/architecture/best-practices/caching?toc=%2Fazure%2Fredis-cache%2Ftoc.json#considerations-for-implementing-caching-in-azure)


**Challenge: Secure your cache**

[Secure usng Virtual Networks](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-how-to-premium-vnet)


### Java Specific

#### User Story: _As a software engineer I need to connect my containerized spring boot applications to use our off-cluster Redis Cache_

**Challenge: Communicate between Java and Azure Cache for Redis**

[Choosing between Jedis and Lettuce Java Libraries](https://gist.github.com/warrenzhu25/1beb02a09b6afd41dff2c27c53918ce7#file-azure-redis-java-best-practices-md)

[Jedis Redis Best Practices](https://gist.github.com/JonCole/925630df72be1351b21440625ff2671f#file-redis-bestpractices-java-jedis-md)
[Lettuce Best Practices](https://gist.github.com/warrenzhu25/181ccac7fa70411f7eb72aff23aa8a6a#file-azure-redis-lettuce-best-practices-md)

##### Tutorials
[Connect to Java Applictaion using Jedis](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-java-get-started#create-a-new-java-app)

[Configure a Spring Boot Initializer app to use Redis in the cloud with Azure Redis Cache](https://docs.microsoft.com/en-us/java/azure/spring-framework/configure-spring-boot-initializer-java-app-with-redis-cache?view=azure-java-stable)

[Configuring Azure Redis Cache to boost Spring Boot performance ](https://dev.to/azure/configuring-azure-redis-cache-to-boost-spring-boot-performance-7-7-52dl)

[Connecting to Azure Redis Cache from redis-cli](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-how-to-redis-cli-tool)
* Redis-cli does not support ssl connections