# Kafka Real-Time Streaming: Producer & Consumer

This project demonstrates real-time streaming using Confluent Kafka, including schema creation and the implementation of a producer and consumer.

---

## Prerequisites

1. **Confluent Cloud Account**: Create a free account on [Confluent Cloud](https://www.confluent.io/).
2. **CLI Tools**: Install the Confluent CLI. Refer to the [official documentation](https://docs.confluent.io/confluent-cli/current/install.html).
3. **Kafka Client Libraries**: Ensure you have the necessary libraries installed (e.g., `confluent-kafka-python` for Python).

---

## Steps for Setup

### 1. Create Kafka Cluster

1. Log in to your Confluent Cloud account.
2. Create a new Kafka cluster in the desired environment. Use the "Basic" (free) cluster for this project.
3. Note down the **Cluster ID** and bootstrap server URL.

### 2. Create API Key for Kafka Cluster

1. Go to the cluster details page.
2. Navigate to **API Access** -> **Create Key**.
3. Generate an API key and secret for the Kafka cluster.  
   - **Key**: (Keep it safe and secure)
   - **Secret Key**: (Keep it safe and secure)

### 3. Create Schema Registry API Key

1. Navigate to the **Schema Registry** section.
2. Generate a new Schema Registry API key and secret.  
   - **Key**: (Keep it safe and secure)
   - **Secret Key**: (Keep it safe and secure)

### 4. Define Topics and Schema

1. In your cluster, create a **topic** for real-time streaming (e.g., `realtime-stream`).
2. Navigate to **Schema Registry** -> **Subjects** and create schemas for your topic:
   - **Key Schema**: Use a string type schema.
   - **Value Schema**: Use JSON format for the value schema. Example:
     ```json
     {
       "type": "record",
       "name": "SampleValue",
       "fields": [
         { "name": "id", "type": "string" },
         { "name": "timestamp", "type": "string" },
         { "name": "data", "type": "string" }
       ]
     }
     ```
3. Link the schema with the topic using the Data Contracts.

![Screenshot 2024-11-26 100804](https://github.com/user-attachments/assets/19ed7e5e-2a90-445e-9802-b5848cc1d225)


https://github.com/user-attachments/assets/ade7847b-5ab7-43de-a988-9814c1ea12ac



