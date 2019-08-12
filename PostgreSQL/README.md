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

[Firewall rules](https://docs.microsoft.com/en-us/azure/postgresql/concepts-firewall-rules)

[Create and manage firewall rules](https://docs.microsoft.com/en-us/azure/postgresql/howto-manage-firewall-using-portal)

**Challenge: Configures the server's firewall to accept connections from all Azure resources**

NB: All Azure resources, including resources not in your subscription will have access. When selecting this option, make sure your login and user permissions limit access to only authorized users. 

[Connecting to the server from Azure](https://docs.microsoft.com/en-us/azure/postgresql/concepts-firewall-rules#connecting-from-azure)

**Challenge: Connect to your Azure Database for PostgreSQL server  using Azure Data Studio** 

[Connect to PostgreSQL with Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-postgres?view=sql-server-2017)
* Once you install the PostgreSQL extension for Data Studio you may need to restart the application to see it available as a server connection type






## TODO 

### Connection to Redis Cache 

#### User Story: _As a software engineer I need to connect my managed PostgreSQL service to Redis Cache_

### Connection to Containerized applications

#### User Story: _As a software engineer I need to connect my containerized spring boot applications to use our off-cluster PostgreSQL data service_


**Challenge: Communicate between AKS and Azure PostgreSQLr**

[Concept behind connecting AKS and Azure PostgreSQL (Single Server)](https://docs.microsoft.com/en-us/azure/postgresql/concepts-aks)


1. Via Connection String: 

    ```
    String host = "mydemoserver.postgres.database.azure.com";
    String database = "mypgsqldb";
    String user = "mylogin@mydemoserver";
    String password = "<server_admin_password>";
    ``` 

2. Using Open Service Broker

    *  [Connect applications running in Kubernetes to Azure Database for PostgreSQL using the Open Service Broker for Azure](https://azure.microsoft.com/en-us/resources/videos/postg-osba-vid/)
    
    * [Example Architecture](https://azure.microsoft.com/en-us/solutions/architecture/migrate-existing-applications-with-aks/)

3. ExpressRoute circuit using private peering 

4. Within Java Application 
    *    [Guide on using PostgreSQL JDBC Driver](https://docs.microsoft.com/en-us/azure/postgresql/connect-java) 

5. VNet Service Endpoints (Often the best option)  

    [How To Guide: Create and manage VNet service endpoints and VNet rules in Azure Database for PostgreSQL - Single Server by using the Azure portal](https://docs.microsoft.com/en-us/azure/postgresql/howto-manage-vnet-using-portal)
    * [Microsoft.Sql](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-supported-services) is the formal Azure Service Type Name/Tag needed to be applied to a VNet service endpoint. This will configure service endpoint traffic for all Azure SQL Database, Azure Database for PostgreSQL and Azure Database for MySQL servers on the subnet [Ref to PostgreSQL VNet Concepts](https://docs.microsoft.com/en-us/azure/postgresql/concepts-data-access-and-security-vnet)
    * When configuring the PostgreSQL Service Connection Security (VNet), if a VNet does **not** exist, within the PostgreSQL's Connection Security you can create a new VNet and then you will have to return there and do the Add Existing Virtual Network step. 
	* Support for VNet service endpoints is only for General Purpose and Memory Optimized servers.


#### User Story: _As a software engineer I need to be aware of best practices and performanace metrics around my managed PostgreSQL service_

* [Monitor and gain query Performance Insights (Single Server)](https://docs.microsoft.com/en-us/azure/postgresql/tutorial-monitor-and-tune) 
    * [TODO: Query Performance View Not Available](https://docs.microsoft.com/en-us/azure/postgresql/concepts-query-performance-insight)
* [Data Backup](https://docs.microsoft.com/en-us/azure/postgresql/concepts-backup)
    * Choose between locally redundant or geo-redundant backup service
        * Cannot switch between redundant or geo-redundant once the server is provisioned
    * The minimum retention period for backups is seven days. You can set a retention period of up to 35 days.  
* Storage
    * Can add additional storage capacity (automatically or manually) after the creation of the server but storage can only be scaled up, not down. [Ref](https://docs.microsoft.com/en-us/azure/postgresql/concepts-pricing-tiers#storage)
* Security 
    * Turn on [Advanced Threat Protection](https://docs.microsoft.com/en-us/azure/postgresql/concepts-data-access-and-security-threat-protection) 


#### User Story: _As a software engineer I need to be aware of the known limitations of  my managed PostgreSQL service_

[What it means to have an Azure Managed Database](https://azure.microsoft.com/en-us/product-categories/databases/)

[Latest Version generally available: PostgreSQL 11](https://azure.microsoft.com/en-us/updates/postgresql-11-is-now-generally-available-in-azure-database-for-postgresql/)

[Single Server Limits](https://docs.microsoft.com/en-us/azure/postgresql/concepts-limits)

[Hyperscale (Citus)]()


## Stretch Goals 

1. Migrating Existing Data into Azure Postgres 
2. Continue along with PostgreSQL [docs](https://docs.microsoft.com/en-us/azure/postgresql/tutorial-design-database-using-azure-portal)

