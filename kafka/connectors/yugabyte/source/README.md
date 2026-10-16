# Debezium and CDC in YugabyteDB

https://docs.yugabyte.com/stable/integrations/cdc/debezium/

<!-- THIS IS THE MOST IMPORTANT DOC YET -->

https://debezium.io/documentation/reference/stable/transformations/outbox-event-router.html#basic-outbox-table


<!-- Notes -->
1. Unlike yboutput, pgoutput is unaware of the internal CHANGE identity format of YugabyteDB and rejects it: plugin.name: yboutput
2. PGCompatible unwraps the {value, set} columns of yboutput so EventRouter sees the envelope (like pgoutput): transforms: pgcompat,outbox