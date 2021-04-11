"# rabbitmq_demo" 

## Enable Admin console
Go to rabbit mq command prompt
1. rabbitmq-plugins enable rabbitmq_management
2. rabbitmq-server -detached


## Delayed messsage
Enable plugin

    rabbitmq-plugins enable rabbitmq_delayed_message_exchange

One senario for the feature is, 
when an order created, items will reserved in the stock
but if no payment is done in 30 mins, the order will be cancelled and return reserved items to stock.

A 30 mins delay message can be published when the order created.
