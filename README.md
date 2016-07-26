## docker-flume

  Docker image containing [Apache Flume](https://flume.apache.org/)

## Build Instructions

    docker build -t flume .

## Available environment variables

 * `FLUME_AGENT_NAME` - name of flume agent to run. **Required**
 * `FLUME_CONF_FILE` - location of flume configuration file. **Required**
 * `FLUME_CONF_DIR` - directory for flume environment/configuration files. Defaults to `/opt/flume/conf`
 * `FLUMR_CONF_FILE_CONTENTS` - if set, gets written out to the FLUME_CONF_FILE file

## Example usage

    docker run \
      -e FLUME_AGENT_NAME=someagent \
      -e FLUME_CONF_FILE=/var/tmp/flume.conf \
      -e FLUME_CONF_FILE_CONTENTS="`cat flume.conf`"
      lokkju/flume-hdfs:latest
