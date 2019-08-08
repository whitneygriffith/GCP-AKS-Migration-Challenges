# PostgreSQL on Azure Notes

### PostgreSQL Specific 

#### User Story: _As a software engineer I need to provision a managed PostgreSQL service in Azure_

Deployment Options: 
1. Single Server 
2. [Hyperscale (Citus)]((https://www.citusdata.com/blog/2019/05/06/introducing-hyperscale-citus-on-azure-database-for-postgres/)) 

**Challenge: Make a deployment choice** 

[Choosing between Single server vs Hyperscale (Citus)](https://docs.microsoft.com/en-us/azure/postgresql/overview)
    
Comparison | Single Server | Hyperscale (Citus)
--- | --- | ---
Use Cases | | Multi-Tenant Applications or Requires Data Analytics Insights for a large data set, and streaming events
Load of data (1M events) | 4 minutes | 30 seconds with 32 shards
Data Workload | | >= 100 GB of data, ideally 1TB 
Best For | Broad range of traditional transactional workloads | Ultra-high performance. Multi-tenant applications and real-time analytical workloads that need sub-second response.
Scales | Up to 64 vCores. Dynamic scaling available | Horizontally scales across multiple machines. 32 


**Challenge: Create Azure Database for PostgreSQL**

[Single Server](https://docs.microsoft.com/en-us/azure/postgresql/quickstart-create-server-database-portal)
 OR [Hyperscale (Citus)](https://docs.microsoft.com/en-us/azure/postgresql/quickstart-create-hyperscale-portal)

**Challenge: Configure a server-level firewall rule by adding your client IP address**

**Challenge: Connect to your Azure Database for PostgreSQL server  using Azure Data Studio** 

#### User Story: _As a software engineer I need to know what azure tools I can use to connect to my PostgreSQL service_

[Connect to PostgreSQL with Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-postgres?view=sql-server-2017)
* Once you install the PostgreSQL extension for Data Studio you may need to restart the application to see it available as a server connection type






## TODO 

### Connection to Redis Cache 

#### User Story: _As a software engineer I need to connect my managed PostgreSQL service to Redis Cache_

### Connection to Containerized applications

#### User Story: _As a software engineer I need to connect my containerized spring boot applications to use our off-cluster PostgreSQL data service_

**Challenge: Communicate between AKS and Azure PostgreSQLr**

[Concept behind connecting AKS and Azure PostgreSQL (Single Server)](https://docs.microsoft.com/en-us/azure/postgresql/concepts-aks)


1. Using Open Service Broker

    *  [Connect applications running in Kubernetes to Azure Database for PostgreSQL using the Open Service Broker for Azure](https://azure.microsoft.com/en-us/resources/videos/postg-osba-vid/)
    
    * [Example Architecture](https://azure.microsoft.com/en-us/solutions/architecture/migrate-existing-applications-with-aks/)

2. Site to Site VPN  / VNet peering 

3. ExpressRoute circuit using private peering 

4. Within Java Application 

    *    [Guide on using PostgreSQL JDBC Driver](https://docs.microsoft.com/en-us/azure/postgresql/connect-java) 
    
    * Connection Information Needed:

    ```
    String host = "mydemoserver.postgres.database.azure.com";
    String database = "mypgsqldb";
    String user = "mylogin@mydemoserver";
    String password = "<server_admin_password>";
    ``` 

#### User Story: _As a software engineer I need to be aware of best practices around my managed PostgreSQL service_

1. For reading and writing data 
2. Security 
    *  Securing my data access end points
    * Securing data at rest and in motion. 
3. Optimizing Performance
    * Queries
    * Response Latency  
5. [Data Backup](https://docs.microsoft.com/en-us/azure/postgresql/concepts-backup)
    a. Choose between locally redundant or geo-redundant backup service 
6. Geo-replication
7. Access Control using AAD 


#### User Story: _As a software engineer I need to be aware of the known limitations of  my managed PostgreSQL service_

[Azure Managed Databases](https://azure.microsoft.com/en-us/product-categories/databases/)

[Latest Version generally available: PostgreSQL 11](https://azure.microsoft.com/en-us/updates/postgresql-11-is-now-generally-available-in-azure-database-for-postgresql/)

[Single Server](https://docs.microsoft.com/en-us/azure/postgresql/concepts-limits)

[Hyperscale (Citus)]()


## Stretch Goals 

1. Migrating Existing Data into Azure Postgres 
2. Continue along with PostgreSQL [docs](https://docs.microsoft.com/en-us/azure/postgresql/tutorial-design-database-using-azure-portal)

