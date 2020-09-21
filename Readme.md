

## Generate logs

Application startup will generate some logs.

Calling the demo endpoint will generate some more logs, with Sleuth trace and Span Ids.

## Testing

http://localhost:8080/log/message

## Splunk Query

host=splunkforwarder| regex  message=(?<field>.*(?=Log.*)) | stats   latest(trace) as trace  latest(class) as class latest(message) as message by thread
```
