point-dyndns
============

A Dynamic DNS client for PointDNS users.

This Python uses http://icanhazip.com/ and the PointDNS API to implement
a simple Dynamic DNS system. It checks if your public IP address has changed,
and if so, updates a specified DNS record to use the new address.

It depends on Mike Yumatov's pointhq module, but for now, I would recommend
using my fork of the module rather than default version from PyPI. My fork fixes
a couple bugs and enables HTTPS by default. It can be installed as follows:

`pip install git+git@github.com:vortura/pointhq.git@master#egg=pointhq`

Installation
------------

Clone the repository to a suitable location, rename `dyndns.cfg.example` to
`dyndns.cfg` and edit it to include your authentication details and the dynamic
DNS entry you'd like to manage.

Run the script with 

    ./dyndns-client -h
    usage: dyndns-client [-h] [-c CONFIG]

    Simple PointDNS dynamic DNS client

    optional arguments:
      -h, --help            show this help message and exit
      -c CONFIG, --config CONFIG
                            Specify config file location (default ./dyndns.cfg)
