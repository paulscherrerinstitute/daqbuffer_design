# DAQ Ingest

## Goals

* Read from BSREAD and ChannelAccess and put events into Scylla.
* Detect unresponsive/disconnected/dead sources.
* Limit maximum frequency/bandwidth per channel.


## Definitions / Diagramm

* CA Ingestor.
* BSREAD Ingestor.
* Data store.
* Retrieval.


## Ingestors' responsibilities

* Increase `ts_msp` such that partition size is reasonable.
* Each time `ts_msp` is increased, must insert it also into table `ts_msp`.
* Avoid thundering hordes: incorporate a series-specific offset in `ts_msp`.
