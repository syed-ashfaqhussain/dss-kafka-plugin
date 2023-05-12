# README

### DSS Kafka Plugin

The DSS Kafka plugin is a custom Python dataset connector that allows Dataiku DSS users to easily consume messages from a Kafka topic as a DSS dataset.

### Requirements

- Dataiku DSS version 8.0 or later
- Kafka cluster

### ****Installation****

1. Download the source code or clone the repository.
2. In DSS, navigate to **Settings > Plugins > Installed** and click on **Install Plugin**.
3. Select the plugin archive (**`plugin.json`**) and click on **Install**.
4. Restart the DSS server.

### Usage

1. In DSS, create a new Python dataset.
2. Copy the code for the Kafka Consumer dataset from **`kafka_consumer.py`** in the plugin directory.
3. Paste the code into the **Python code** section of the dataset.
4. Modify the code to suit your requirements.
5. Save and run the dataset.

### Configuration

The following configuration parameters can be set in the DSS dataset settings:

- **`kafka_bootstrap_servers`**: A comma-separated list of Kafka bootstrap servers.
- **`kafka_topic`**: The Kafka topic to consume messages from.
- **`data_format`**: The format of the messages. Currently, only Avro format is supported.
- **`schema_registry_url`**: The URL of the Confluent Schema Registry.
- **`avro_schema_subject`**: The name of the Avro schema subject in the Schema Registry. By default, it is set to **`<kafka_topic>-value`**.
- **`data_format_schema_subject`**: The name of the schema subject in the schema registry for the specified data format. By default, it is set to **`<kafka_topic>-value`**, but can be customized to match the naming conventions used in the schema registry.

### Support

If you encounter any issues with the plugin, please open an issue on the https://github.com/syed-ashfaqhussain/dss-kafka-plugin.git

### Contributing

If you would like to contribute to the plugin, feel free to submit a pull request on the https://github.com/syed-ashfaqhussain/dss-kafka-plugin.git
