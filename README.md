#### The code shows how to use Cloud Dataflow to run a batch word count job and store the results to Cloud Storage bucket.
---
1) Run the Maven job, where [PROJECT_ID] is your GCP project ID and [BUCKET] is your bucket with two folders (staging and output): <br/>
```
mvn -Pdataflow-runner compile exec:java \
    -Dexec.mainClass=org.apache.beam.examples.WordCount \
    -Dexec.args="--project=[PROJECT_ID] \
    --stagingLocation=gs://[BUCKET]/staging/ \
    --output=gs://[BUCKET]/output/ \
    --runner=DataflowRunner"
```
