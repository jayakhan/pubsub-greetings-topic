I have created a topic – subscribe-test on GCP and configured a pub sub trigger to this topic. As soon as this topic receives a message with a person’s name, it triggers a python function – hellopubsub – that greets the person.

Commands used:
```
gcloud functions deploy hello_pubsub \
--runtime python39 \
--trigger-topic subscribe-test


gcloud pubsub topics publish subscribe-test --message Jaya

gcloud functions logs read --limit 10
```


