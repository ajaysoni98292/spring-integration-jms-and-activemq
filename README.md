JMS Sample
==========

This example demonstrates the following aspects of the Java Message Service (JMS) support available with *Spring Integration*:

1. JMS Message-driven Channel Adapter
2. JMS Inbound Gateway
3. JMS Outbound Gateway

It also uses the following components:

1. Poller
2. Stdout Channel Adapter (from Stream support Module)
3. Stdin Channel Adapter (from Stream support Module)

It also shows an example of using Spring profiles to modify the configuration for test cases.

The Stdout and Stdin Channel Adapters will allow you to interact with JMS via the console. It uses an embedded ActiveMQ broker.

You will then be prompted to run one of two demos:

* **GatewayDemo**
* **ChannelAdapterDemo**

The console output should look like:

	=========================================================

	    Welcome to the Spring Integration JMS Sample!



	=========================================================
	16:48:21.158 INFO  [org.springframework.integration.samples.jms.Main.main()][org.springframework.integration.samples.jms.ActiveMqTestUtils] Refreshing ActiveMQ data directory.

	    Which Demo would you like to run? <enter>:

		1. Channel Adapter Demo
		2. Gateway Demo

When running either one of the demos you will see the following prompt:

	> Please type something and hit <enter>

* **GatewayDemo** uses the *DemoBean* service, which will echo the response and upper-casing it.
* **ChannelAdapterDemo** will simply echo the response


There are also test cases that exercise both demos; utilizing Spring 3.0 profiles to route the output to a QueueChannel instead of stdout.
