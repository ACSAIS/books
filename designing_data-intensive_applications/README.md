# Designing Data-Intensive Applications

## Part I

### Chapter 1

### Chapter 2

### Chapter 3

### Chapter 4

## Part II

### Chapter 5 Replication

Replication means keeping a copy of the same data on multiple machines that are connected via a network.There are 
several reasons why you might want to replicate data:

- To keep data geographically close to your users (and thus reduce latency)
- To allow the system to continue working even if some of its parts have failed (and thus increase availability)
- To scale out the number of machines that can serve read queries (and thus increase read throughput)

### Chapter 6 Partitioning

Partition == sharding

**Partitioning of key-value data**, hash-function can help to evenly distribute data among all partitions.

**Partitioning Secondary Indexes by document**
![Partitioning Secondary Indexes by document](/designing_data-intensive_applications/img/partition_secondary_indexes_by_document.png "Partitioning Secondary Indexes by document")

Each partition maintains its own secondary indexes, covering only the documents in that partition.

+easy to write

-hard to read(need to check all partitions)
