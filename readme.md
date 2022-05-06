# Daqbuffer design and specifications

## Data storage

[Detailed page](data-stores.md)

* Scylla: actual payload data, time series and their supporting structures.
* Postgres: slower transactional data, channel search and lookup.


## Ingest Architecture

[Detailed page](daqingest.md)

* Specific details about [BSREAD ingest](ingest-bsread.md).
* Specifics about [Channel Access ingest](ingest-ca.md).
