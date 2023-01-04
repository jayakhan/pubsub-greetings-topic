## Abstract
The idea behind this project is to facilate the basics of streaming data integration pipeline. A `Pub/Sub` asynchronous messaging service, built on Google platform, is used to trigger a subscriber as soon as a message appears on the `Topic`. 

Below is the simple flow of message via Topic in GCP.

![Alt text](assets/pubsub.png "Architecture")


## Project Description
I have created a topic – subscribe-test on GCP and configured a pub sub trigger to this topic. As soon as this topic receives a message with a person’s name, it triggers a python function – hellopubsub – that greets the person.

## Commands used
```
gcloud functions deploy hello_pubsub \
--runtime python39 \
--trigger-topic subscribe-test


gcloud pubsub topics publish subscribe-test --message Jaya

gcloud functions logs read --limit 10
```


