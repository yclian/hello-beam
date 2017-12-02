# Hello Apache Beam

## Run

### Run with Docker

    docker run -it --rm --name hello-beam \
      -v ~/.m2:/root/.m2 -v "$PWD":/usr/src/hello \
      -w /usr/src/hello maven:3.5-jdk-8 \
      mvn compile exec:java -Dexec.mainClass=org.apache.beam.WordCount \
      -Dexec.args="--inputFile=pom.xml --output=counts" -Pdirect-runner


## References

 - [Quick start](https://beam.apache.org/get-started/quickstart-java/)
 - [Pipeline design](https://beam.apache.org/documentation/pipelines/design-your-pipeline/)

