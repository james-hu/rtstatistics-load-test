# Load testing rtstatistics.com

## JMeter

Apache JMeter is used to run the load tests. The following plugins are needed:

* Plugins Manager - https://jmeter-plugins.org/wiki/PluginInstall/
* 3 Basic Graphs - https://jmeter-plugins.org/wiki/ResponseTimesOverTime/
* 5 Additional Graphs - https://jmeter-plugins.org/wiki/ResponseCodesPerSecond/
* Throughput Shaping Timer - https://jmeter-plugins.org/wiki/ThroughputShapingTimer/


## Sending

### Parameters

Some parameters defined as user defined variables can be changed:

* DATASET_ID - ID of the dataset for sending data to and querying from
* SEND_KEY_AUTH - the encoded send key that will be sent in the HTTP request headers. 
    You may use `echo -n 'SEND_KEY' | base64` to get it.
* BATCH_SIZE - Number of messages to be sent in one HTTP POST request, can be 1, 5, or 10. 
* TARGET_RPS - Target requests per second
* DURATION - Number of seconds for keeping the load at TARGET_RPS
* THREADS - Number of threads