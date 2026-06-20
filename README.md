# kafkacodebase

mkdir kafka-101-consumers && cd kafka-101-consumers
python3 -m venv env
source env/bin/activate
pip install confluent-kafka

confluent kafka cluster describe

confluent api-key create --resource {ID}

confluent api-key use {API Key} --resource {ID}

chmod u+x consumer.py
./consumer.py config.ini



confluent kafka topic consume --from-beginning orders

confluent kafka topic consume --value-format avro --schema-registry-api-key {API Key} --schema-registry-api-secret {API Secret} orders

confluent kafka topic consume --from-beginning inventory