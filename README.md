# Spring-Boot-Splunk-Docker

Splunk Query
host=splunkforwarder| regex message=(?.(?=Log.)) | stats latest(trace) as trace latest(class) as class latest(message) as message by thread
