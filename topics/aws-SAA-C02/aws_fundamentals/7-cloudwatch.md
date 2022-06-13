<h1>Cloudwatch</h1>

CloudWatch is a support service that is used by most other AWS services. Cloudwatch performs three main jobs.

Collects and manages operational data (any data generated by an environment, how it performs, logging etc.):
- Metrics, for example, CPU usage, storage usage or maybe number of visitors per second. Some metrics are gathered natively by the product. For example looking at CPU usage of a EC2 instance is done by default. Some types of metric collection need extra piece of software called CloudWatch agent, for example, to gather metrics outside of AWS environment.

- Cloudwatch logs this allows for collections, monitoring and action based on a logging data.

- Cloudwatch events provide two powerful features:
1) If an aws service does something, maybe EC2 instance is terminated, started or stopped then cloudwatch events will generate event which perform another action.
2) It can generate events to do something at a certain time of day or certain days of week.

Cloudwatch namespace can be thought of as a container for monitoring data. It can be used to separate data into different areas.

Namespaces have a name and that can be anything as long as it stays within a ruleset for namespace names. There's one exception and that's all aws data goes into aws namespace which is: "AWS/service", e.g. AWS/EC2. Namespaces contain related metrics.

A metric is a collection of related data points in a time ordered structure. Data point in its most simplest form contains a timestamp and value. Since data points (example CPU usage) can contain data from many servers we can separate them via dimensions.

Dimensions are name-value pairs sent together with data points by the services to help cloudwatch separate things and gain different perspective of things within a metric. Say you have three EC2 instances each sending one data point per second to the CPU utilization metric in cloudwatch. In that case AWS will also send instance ID and instance type as dimensions and this allows you to view data points for particular EC2 instance.

Cloudwatch also allows you to take actions based on the metrics. This is done using alarms. Alarms are created and linked to specific metric. Alarms will take action based on that metric. An alarm can be in OK state but it can also be in "alarm" state and that means something bad has happened. Based on that you can define an action which could send notification to SNS topic, send email etc. Alarms can also be in the third state "insufficient data", that means they haven't received enough data to assess whether everything's OK or not. 