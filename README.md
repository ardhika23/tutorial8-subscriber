# 📝Tutorial & Exercise📝

**Student Details :**

|  `Attribute`  | `Information`              |
|---------------|----------------------------|
| Name          | Ardhika Satria Narendra    |
| Student ID    | 2206821866                 |
| Class         | Advanced Programming KKI   |

---
<details>
<summary>Module 08: Software Architectures</summary>

## Questions and Answers

### -> Reflection 

#### a. what is amqp
AMQP stands for Advanced Message Queuing Protocol. It is an open standard protocol for message-oriented middleware, enabling interoperability between different systems and platforms that involve message-oriented communication.

#### b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?

The URL amqp://guest:guest@localhost:5672 is used to connect to a message broker, which in this case is configured to run on the local machine. Here, the first 'guest' is the username and the second 'guest' is the password for the RabbitMQ server. The localhost:5672 specifies that the RabbitMQ server is running locally on port 5672, which is the default port for RabbitMQ.

#### Simulating slow subscriber

![alt text](image.png)

The RabbitMQ dashboard shows a peak in the queue, indicating the publisher is sending messages faster than the subscriber can process them. The total queue count reveals the system's current load; my queued messages reflect the consumer's pace, which in this case, is 40. 

#### Running at least three subscribers

![alt text](image-1.png)

![alt text](image-2.png)

It's clear that by running multiple instances of the subscriber (`cargo run` in separate consoles), the processing of messages becomes more efficient. The screenshot of the RabbitMQ management interface shows that after increasing the number of subscribers, the queued messages are handled more rapidly, leading to a quicker reduction in the queue's size. This indicates that distributing the workload across multiple subscribers can effectively mitigate the issue of a slow consumer.

---

</details>

