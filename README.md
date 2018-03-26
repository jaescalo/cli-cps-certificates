# Akamai CLI: CPS (Certificate Provisioning System) Retrieve Certificates and Expiration Date

This tool is an example module written in Python for the Akamai CLI Tool although it can be executed individually. After the execution of this tool a report on athe available certificates and their expiration dates will be generated.


## Install

Installation is done via `akamai install`:

```
$ akamai install cps-certificates
```

Running this will run the system `python setup.py` automatically. 

## Updating

To update to the latest version:

```
$ akamai update cps-certificates
```

## Usage:
```
usage: akamai cps list --certs [--edgerc EDGERC] [--section SECTION]
                          [--verbose]

required arguments:
  --certs            Get the certificates expiration date

optional arguments:
  --edgerc EDGERC    Config file [default: ~/.edgerc]
  --section SECTION  Config section in .edgerc
  --verbose          Enable an interactive verbose mode
```

The --verbose mode goes through every step for every API call and showing the user the generated JSON requests and responses.

### Example 2: generate the list using the default values

Defaults are:
`--edgerc: ~/.edgerc
--section: papi
--verbose: OFF`

```
$ ./akamai-cps.py list -certs

```

### Example 2: generate the list overrriding the default values


```
$ ./akamai-cps.py list -certs --edgerc <~/other_location/.edgerc> --section <other_section> --verbose
```
