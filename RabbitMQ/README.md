# RabbitMQ on Azure Notes

Links:

- [Messaging - RabbitMQ, Azure (Service Bus), Docker and Azure Functions - Dot Net Sheff - May 2018](https://youtu.be/zfmjJw3zDZQ)
- [Bitnami RabbitMQ](https://bitnami.com/stack/rabbitmq/cloud/azure)
- [HOW TO SET UP A RABBITMQ CLUSTER ON AZURE](https://www.linkedin.com/pulse/how-set-up-rabbitmq-cluster-azure-akshay-kunila/)
- [Setup RabbitMQ on Azure Container Service using Kubernetes and Helm](https://ppolyzos.com/2017/07/19/setup-rabbitmq-on-azure-container-service-using-kubernetes-and-helm/)
- [.NET Tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-dotnet.html)
- [Clustering](https://www.rabbitmq.com/clustering.html) & [Monitoring](https://www.rabbitmq.com/monitoring.html)

# Challenge 1 

How does one test RabbitMq locally? 

Discuss with your team the merits of Events, Command and Messaging in a Microservices Architecture. 

# Challenge 2 

Use docker to host RabbitMQ in a container in Azure. 

Then connect the two using a client of your choice. 

How does your team translate and interpret messages between disparate systems in your architecture? 

# Challenge 3 

Your customer only wants messages that are related to specific data fields. How do you configure this with RabbitMQ

How does the ability to filter and route messages change the integration patterns of your application?  

# Other challenges

- Can you deal with a down container? What hosting mechanism do you choose and why? 
- How can you ensure RabbitMq health, performance, and service availability? 
- Can you connect two container's together? (maybe use a logic app to tie them together?) 
