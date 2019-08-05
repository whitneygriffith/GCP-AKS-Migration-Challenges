# PostgreSQL on Azure Notes

### PostgreSQL Specific 
_As a software engineer I need to provision a managed PostgreSQL service in Azure_

1. Azure Portal 
2. ARM Templates

_As a software engineer I need to optimize the performance of my PostgreSQL service_

1. Choosing between Single server vs Citus: Hyperscale
    
    Action | Single Server | Hyperscale 
    --- | --- | ---
    Load of data (1M events) | 4 minutes | 30 seconds with 32 shards

_As a software engineer I need to know what tools I can use to connect to my PostgreSQL service_

[Connect to PostgreSQL with Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-postgres?view=sql-server-2017)

#### Citus/HyperScale 

[Citus Azure PostgreSQL Announcement](https://www.citusdata.com/blog/2019/05/06/introducing-hyperscale-citus-on-azure-database-for-postgres/)

_As a software engineer I need to be aware of the known limitations of  my PostgreSQL service_

_As a software engineer I need to be aware of best practices around my managed PostgreSQL service_

1. For reading and writing data 
2. Securing my data access end points
3. Optimizing Latency 
4. Optimizing Queries 
5. [Data Backup](https://docs.microsoft.com/en-us/azure/postgresql/concepts-backup)
    a. Choose between locally redundant or geo-redundant backup service 
6. Geo-replication
7. Access Control using AAD 

### Connection to Redis Cache 

_As a software engineer I need to connect my managed PostgreSQL service to Redis Cache_

### Connection to Containerized applications

_As a software engineer I need to connect my containerized spring boot applications to use our off-cluster PostgreSQL data service_

#### Open Service Broker- Communication Tool 
[Connect applications running in Kubernetes to Azure Database for PostgreSQL using the Open Service Broker for Azure](https://azure.microsoft.com/en-us/resources/videos/postg-osba-vid/)
[Example Architecture](https://azure.microsoft.com/en-us/solutions/architecture/migrate-existing-applications-with-aks/)

## Stretch Goals 

### Migrating Existing Data into Azure Postgres 

