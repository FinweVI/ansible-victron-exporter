# Ansible Role: victron-exporter

Provision and manage the Prometheus [victron-exporter](https://github.com/suprememoocow/victron-exporter).  
Exporter to report metrics fetched from the MQTT interface on a Victron GX Device.

## Requirements

- Ansible >= 2.8

## Role Variables

Main variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `victron_exporter_version` | 0.2.0 | Victron Exporter version to install |
| `victron_exporter_address` | 127.0.0.1:9226 | Address on which victron-exporter listens |
| `victron_exporter_port` | 8883 | MQTT Port on the GX Device |
| `victron_exporter_repository ` | github.com/suprememoocow/victron-exporter | github link to the source code |
| `victron_exporter_client_prefix` | victron_exporter | Default prefix for exported metrics |
| `victron_exporter_poll_interval_duration` | 10s | Must be a duration. Waiting periods between the exporter communications with the GX Device |
| `victron_exporter_secure` | true | Whether to use the Secure (SSL) Version of the MQTT protocol |
| `victron_exporter_host`\* | None | IP Address of the local GX Device |
| `victron_exporter_username`\* | None | Username for the remote Victron MQTT Service |
| `victron_exporter_password`\* | None | Password for the remote Victron MQTT Service |


\*: You need to either provide the local IP Address or a set of Username/Password for the remote connection.

See the [defaults/main.yml](defaults/main.yml) file for examples.


## Notes

It's Debian-based Only.
It must be possible to make it CentOS (or any other linux-based OS) compatible.
Issues & PR are welcome for any improvement ;-)

This is heavily inspired by [CloudAlchemy]('https://github.com/cloudalchemy/')
