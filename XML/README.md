#  XML Files

This directory contains a set of XML data for xRAN YANG models.

* nso-config.xml is the running configuration for the example simulated RU which can be loaded into NSO
* confd-all.xml is the entire set of operational state for the simulated RU which can be loaded into ConfD
* Alternatively, the confd-xxxx.xml files contain the separate sets of operational state associated with individual xRAN YANG models.

## Loading Data

Configuration is loaded into NSO sing the following command

    ncs_load -l -m latestconfig.xml

Operational state is loaded into ConfD using the following command

    env CONFD_IPC_PORT=<insert ipc value> confd_load -lC confd-all.xml
