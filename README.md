# log-forwarder

Ansible role which sets up a stable version of [log-forwarder][] to
forward logs from files to Splunk

## Usage

Apply `MailOnline.log-forwarder` role to your hosts:

    - hosts: appservers
      roles:
        - role: MailOnline.log-forwarder
          lfw_address: splunk-host:228
          lfw_pattern: /var/log/upstart/log/someapp.log

## Variables

Required variables:

- `lfw_pattern`: file name pattern of log files to forward

- `lfw_address`: address to forward logs to (something like `splunk-indexer:228`)

Optional variables:

- `lfw_instance`

[log-forwarder]: https://github.com/MailOnline/forwarder
