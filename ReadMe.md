Advanced Camel JMS Component Config Example
=========================================

This example shows how to configure a custom class in camel-jms component, just providing the class and altering the dependency injection configuration.

To build this project use

    mvn install


To deploy the project in OSGi. For example using Apache ServiceMix
or Apache Karaf. You can run the following command from its shell:

    osgi:install -s mvn:test/advanced_camel_jms_component_config_example/1.0

Sample log:

```
2017-08-31 16:21:06,499 | INFO  | l Console Thread | MyJmsBinding                     | 291 - advanced_camel_jms_component_config_example - 1.0.0 | _________ - MyJmsBinding Loaded - ___________
2017-08-31 16:21:06,507 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 233 - org.apache.camel.camel-blueprint - 2.17.0.redhat-630284 | Attempting to start Camel Context blueprint-bean-context
2017-08-31 16:21:06,507 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | Apache Camel 2.17.0.redhat-630284 (CamelContext: blueprint-bean-context) is starting
2017-08-31 16:21:06,507 | INFO  | nt Dispatcher: 1 | ManagedManagementStrategy        | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | JMX is enabled
2017-08-31 16:21:06,521 | INFO  | nt Dispatcher: 1 | DefaultRuntimeEndpointRegistry   | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | Runtime endpoint registry is in extended mode gathering usage statistics of all incoming and outgoing endpoints (cache limit: 1000)
2017-08-31 16:21:06,548 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | AllowUseOriginalMessage is enabled. If access to the original message is not needed, then its recommended to turn this option off as it may improve performance.
2017-08-31 16:21:06,548 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | StreamCaching is not in use. If using streams then its recommended to enable stream caching. See more details at http://camel.apache.org/stream-caching.html
2017-08-31 16:21:06,561 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | Route: timerToLog started and consuming from: Endpoint[timer://foo?period=5000]
2017-08-31 16:21:06,561 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | Total 1 routes, of which 1 are started.
2017-08-31 16:21:06,561 | INFO  | nt Dispatcher: 1 | BlueprintCamelContext            | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | Apache Camel 2.17.0.redhat-630284 (CamelContext: blueprint-bean-context) started in 0.054 seconds
2017-08-31 16:21:07,562 | INFO  | #4 - timer://foo | timerToLog                       | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | The message contains whatever
2017-08-31 16:21:07,570 | INFO  | #4 - timer://foo | MyJmsBinding                     | 291 - advanced_camel_jms_component_config_example - 1.0.0 | !!!!!!!!!!! - MyJmsBinding invoked - !!!!!!!!!!!!!!!!
2017-08-31 16:21:07,570 | INFO  | #4 - timer://foo | MyJmsBinding                     | 291 - advanced_camel_jms_component_config_example - 1.0.0 | !!!!!!!!!!! - MyJmsBinding invoked - !!!!!!!!!!!!!!!!
2017-08-31 16:21:12,562 | INFO  | #4 - timer://foo | timerToLog                       | 231 - org.apache.camel.camel-core - 2.17.0.redhat-630284 | The message contains whatever
2017-08-31 16:21:12,570 | INFO  | #4 - timer://foo | MyJmsBinding                     | 291 - advanced_camel_jms_component_config_example - 1.0.0 | !!!!!!!!!!! - MyJmsBinding invoked - !!!!!!!!!!!!!!!!
2017-08-31 16:21:12,570 | INFO  | #4 - timer://foo | MyJmsBinding                     | 291 - advanced_camel_jms_component_config_example - 1.0.0 | !!!!!!!!!!! - MyJmsBinding invoked - !!!!!!!!!!!!!!!!
```

