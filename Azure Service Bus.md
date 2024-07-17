# Azure Service Bus



Basically a message broker in Azure. You "post" messages to a big list, and they will come out of the other end and be "consumed" by a service.

- It helps to make sure that no data is lost, the messages will be safely stored in the ASB
  - Even if the service processing the message fails, the message is not lost and can be retried



It can operate in one of two fundamental ways:

### Queue

A service posts messages to the ASB and they will be consumed by a specific kind of service on the other end. You <u>**cannot have more than one type of service**</u> listening in for the messages.



## **Topic**

A service posts messages as a "topic", and <u>**one or more services**</u> can "subscribe" to that topic to pull and process the messages. They can each receive all messages or filtered subsets of the messages, and they can each process the messages in independent ways.