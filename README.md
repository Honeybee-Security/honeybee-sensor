# HONEYBEE SENSOR

## What is it?

The Honeybee sensor is the collection of software that is installed on a network device to capture, analyze, and transmit network traffic. 

## Building

The build process.

If you're developing on an Alpine linux host skip making the VM.
Create a VM with Alpine installed on it.
On the Alpine VM install git, alpine-sdk, docker, docker-compose

On your host create an SSH server.
From the Alpine host run:
git clone ssh://<host ip>/<host path to this repo>

On Alpine run:
gradle :make-alpine-package

## TODO

Switch to building stuff in an Alpine docker container instead of needing a VM.

## Organization

The sensor uses various software packages including [Zeek](https://zeek.org/), [Wazuh](https://wazuh.com/), and [Filebeat](https://www.elastic.co/beats/filebeat). Each of these components is run in a Docker container. The host OS is Alpine Linux. Various scripts and services are used to control and integrate these components. A frontend hosted on [Nginx](https://www.nginx.com/) is developed in the repo [kropotkin-sensor-frontend](https://github.com/Kropotkin-Security/kropotkin-sensor-frontend).

## License

The code developed by Kropotkin is licensed under the Apache 2.0 license. All other software is licensed under various licenses.
