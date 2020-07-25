# ActiveMQ dockerfile

## Build instruction
- Run `docker build --rm --build-arg ACTIVEMQ_VERSION=<ActiveMQ version you want> --tag activemq:<version> .`
- Run `docker run --rm -it activemq:<version>`
- Run `docker ps` to inspect the port mapped to 8161
- Visit `http://127.0.0.1:<port mapped to 8161>` for web console

## Configurations
- Please check ActiveMQ site for the configuration file values. You can mount the folders/files to /activemq