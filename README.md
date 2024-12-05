# Retail Data Streaming with Confluent Kafka  

## Overview  
This project demonstrates a real-time data streaming pipeline using **Python**, **Pandas**, **Confluent Kafka**, and **VS Code**. It utilizes retail data sourced from Kaggle, where a producer publishes data to a Kafka cluster, and multiple consumers subscribe to Kafka topics to consume the data.  

Key features include:  
- **Data Streaming**: Real-time data flow from producer to consumers.  
- **Dynamic Observations**: Changes observed based on read strategies, addition/deletion of consumers, and partition number.  
- **Scalability**: Designed to handle real-time streaming with a fixed partition number.  

## Project Features  
- **Producer**: Publishes retail data to Kafka topics.  
- **Consumer**: Consumes data from Kafka topics using a subscription model.  
- **Partition Observations**: Behavior analysis with a fixed partition number.  
- **Concurrency**: Supports multiple consumers.  

## Technologies Used  
- **Python**: Programming language for producer and consumer code.  
- **Pandas**: Library for data manipulation.  
- **Kafka**: Distributed messaging system for real-time data streaming.  
- **Confluent Kafka**: Managed Platform for Kafka used for this project.  
- **VS Code**: Code editor.  
- **Dataset**: Retail data sourced from Kaggle.  

## Prerequisites  
To run this project, you need:  
1. **Python** (version 3.8 or higher).  
2. **Confluent Kafka** managed Kafka platform.  
3. **confluent-kafka** library installed:  
   ```bash  
   pip install confluent-kafka  
   ```  
4. **pandas** library installed:  
   ```bash  
   pip install pandas  
   ```  
5. **Retail dataset** from Kaggle.

## Getting Started

### Step 1: Setting Up Kafka Cluster

1. Install Confluent Kafka and set up a Kafka cluster.
2. Create a topic in Kafka (e.g., `retail_data_topic`).

### Step 2: Configure the Producer and Consumer

1. Update the **topic name** and **Kafka server configurations** in `producer.py` and `consumer.py`.
2. Ensure the dataset is placed in the `dataset/` folder and its path is correctly referenced in `producer.py`.

### Step 3: Run the Producer

Execute the producer to start streaming data to the Kafka topic:

```bash
python producer.py  
```

### Step 4: Run the Consumer(s)

Start one or more consumers to subscribe to the topic and consume data:

```bash
python consumer.py  
```

### Step 5: Observe the Behavior

- Monitor data consumption and changes when:
  - Adding or removing consumers.
  - Adjusting read strategies in the consumer.

## Observations

- **Partition Number**: The project uses a fixed partition number due to limitations in Confluent Kafka's dynamic resizing.
- **Consumer Behavior**: Real-time insights into how Kafka handles consumer addition and deletion.
