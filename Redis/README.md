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
[Connect to Java Applictaion using Jedis](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-java-get-started#create-a-new-java-app)
[Jedis](https://github.com/xetorthio/jedis)

[Configure a Spring Boot Initializer app to use Redis in the cloud with Azure Redis Cache](https://docs.microsoft.com/en-us/java/azure/spring-framework/configure-spring-boot-initializer-java-app-with-redis-cache?view=azure-java-stable)
