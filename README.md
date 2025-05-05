# Kafka Data Pipeline

### toll_traffic_generator.py
This script is responsible for simulating toll traffic data and generating messages to be sent to a Kafka topic. It creates synthetic data representing vehicles passing through toll booths, including details such as vehicle type, license plate, timestamp, and toll booth ID. The generated data can be used to test and validate the Kafka data pipeline for real-time processing and analytics.

### streaming-data-reader.py
This script is designed to connect to a MySQL database instance. After successful connection, a Kafka Consumer consumers the streamed data from the `toll` topic. It reads messages in real-time, deserializes the data, and performs some transformation to match the table schema in the target database. Finally, the data is written to the DB in real time.