# A flash card style study guide for the MongoDB Associate Developer Certificate exam

### Operations requiring availability of CPU cycles:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Page Compression</li>
    <li>Data Calculation</li>
    <li>Aggrgation Framework Operations</li>
    <li>Map Reduce</li>
	</ul>
</details>

### Main resources MongoDB relies on to operate:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>CPU for processing and calculations</li>
    <li>Memory for execution -> IMPORTANT!</li>
    <li>Disk and IO for persistency and communications between servers or within host processes</li>
	</ul>
</details>

### RAM having come down in price makes prevalence of dbs that are designed around usage of memory. It's also 25x faster than SSD's.

### Operations depending heavily on memory include:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Aggregation</li>
    <li>Index Traversing</li>
    <li>Write Operations</li>
    <li>Query Engine (to retrieve query results)</li>
    <li>Connections (~1MB per established connection)</li>
	</ul>
</details>

### MongoDB uses CPU for:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Storage Engine</li>
    <li>Concurrency Model</li>
	</ul>
</details>

### MongoDB uses CPU for:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Storage Engine</li>
    <li>Concurrency Model</li>
	</ul>
</details>

### By default, MongoDB will try to use all available cores to respond to incoming requests.

### MongoDB RAID Consideratons - Preferred RAID - Non-preferred RAID:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>DO NOT USE RAID 5, RAID 6.</li>
    <li>Also avoid RAID 0 - has good write performance but limited availability, can lead to reduced performance on read operations.</li>
    <li>RAID 10 provides benefits needed by MongoDB</li>
	</ul>
</details>

### Networking performance considerations:

<details>
  <summary>Click here for the solution</summary>
    <ul>
        <li>Types of network switches</li>
        <li>Load balancer</li>
        <li>Firewalls</li>
        <li>How far apart cluster nodes are (across different data centers or regions)</li>
        <li>Types of connections between data centers (i.e. latency - can't go faster than speed of light)</li>
	</ul>
</details>

### IOPS

<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>Input/Output operations per second provided by server. The faster this is, the faster mongo can read/write data. Type of disk will greatly affect MongoDB performance.</li>
    </ul>
</details>

### High availability achieved with

<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>replica cluster sets</li>
    </ul>
</details>

### Horizontal scaling achieved with

<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>sharding cluster</li>
    </ul>
</details>

### Collection Scan

<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>If not using an index when querying collection, db will have to examine every document</li>
    </ul>
</details>

### What is a Collection Scan

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>If not using an index when querying collection, db will have to examine every document</li>
      </ul>
  </details>
  
  ### What is the structure of an index in MongoDB

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>key: value of field that has been indexed on</li>
        <li>value: reference to document containing the key</li>
      </ul>
  </details>
  
  ### Which field is automatically indexed and as unique

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>_id</li>
      </ul>
  </details>
  
  ### What structure are indexes stored in MongoDB

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>MongoDB indexes use a B-tree data structure</li>
      </ul>
  </details>
  
  ### Databases are:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>logical groups of collections</li>
      </ul>
  </details>
  
  ### Collections are:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>are operational units that group documents together</li>
      </ul>
  </details>

### Indexes are:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Indexes are special data structures that store a small portion of the collection's data set in an easy to traverse form.</li>
        <li>The index stores the value of a specific field or set of fields, ordered by the value of the field.</li>
        <li>Indexes support the efficient execution of queries in MongoDB.</li>
      </ul>
  </details>
  
  ### Documents are:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>MongoDB stores data records as BSON documents.</li>
        <li>Atomic units of information used by applications.</li>
      </ul>
  </details>
  
  ### Default databases created my MongoDB:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>admin</li>
        <li>local</li>
      </ul>
  </details>
  
  ### What is/how does Journaliing work?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Journal file acts as safeguard against data corruption caused by incopmlete file writes.</li>
        <li>Data stored in journal is used to recover to a consistent and correct state.</li>
        <li>Journal file structure includes individual write operations.</li>
        <li>To minimize performance impact of journalling, flushes performed with group commits in compressed format.</li>
        <li>Writes to journal are atomic to ensure consistency of journal files.</li>
        <li>With operations setting j: true will impact performance because mongo will wait until sync is done to disk before confirming the write has been acknowledged.</li>
      </ul>
  </details>
  
  ### Stages for a query plan found in the explain output contain:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>COLLSCAN</li>
        <li>IXSCAN</li>
        <li>FETCH</li>
        <li>SHARD_MERGE</li>
        <li>SHARDING_FILTER</li>
      </ul>
  </details>
  
  ### Which field in the explain output shows the number of keys examined:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>totalKeysExamined</li>
      </ul>
  </details>
  
  ### Which field shows the number of documents examed:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>totalDocsExamined</li>
      </ul>
  </details>
  
  ### Well created indexes can be verified in the output of explain by looking at what ratio?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The ratio between nReturned and totalkeysExamined must be as close as possible to 1:1</li>
        <li>nReturned is the number of documents returned from this stage</li>
      </ul>
  </details>
  
  ### Which stage do we want to avoid at all costs, meaning all documents were examined?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>COLLSCAN</li>
      </ul>
  </details>
  
  ### If an index exists for a field and a query returns reults how will the results be sorted (this is without an explicit sort stage)?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>If query is using index scan then the order of documents returned is guaranteed to be sorted by the index keys</li>
      </ul>
  </details>
  
  ### To effeciently use an index with a regex query what should be done?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Start the regex with the ^ operator meaning beginning of expression. /^B.*/ for example will be able to use the index to only look att indexes for strings starting with B.</li>
      </ul>
  </details>

### How do you delete all indexes?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.dropIndexes()</li>
      </ul>
  </details>
  
  ### When creating a compount index what order should the keys be in?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>equality, sort, range</li>
      </ul>
  </details>
  
  ### When to use compound index instead of single key index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>When your operation/query/sort involves multiple keys. This was it can find all documents that fit some expression using the first key and continue to narrow down the results using the second key in the compound key index.</li>
      </ul>
  </details>
  
  ### When to use single key index instead of compount key index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>If you didn't have a compound key index which started with the single key you were using in your query then the compound key index would not be of use.</li>
      </ul>
  </details>
  
  ### For a compount key index to be useful what has to be true about the query or operation?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The query or operation needs to use the keys from the compound key index in the order of the compound key index. The query can have the keys in whichever order but the keys that exist in the query must be all found in the compound key index without skipping a key from the compound key index.</li>
        <li>For example if a index is created with: {"item": 1, "location": 1, "stock": 1}</li>
        <li>Then the query will not use the compound key index if it queries only for item and stock. It will need to query for just item, item and location, or item location and stock</li>
      </ul>
  </details>
  
  ### What is a scalar value?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A scalar value refers to value that is neither an embedded document nor an array.</li>
      </ul>
  </details>
  
  ### What is a MultiKey index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>An index on an array field</li>
      </ul>
  </details>
  
  ### What is a partial index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>An index created with a query to decide which documents to index.</li>
        <li>For example:</li>
        <li>db.restaurants.createIndex( {"address.city": 1, cuisine: 1}, {partialFilterExpression: {"stars": {$gte: 3.5}}} )</li>
      </ul>
  </details>
  
  ### What is a sparse index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A sparse index will only index documents where a certain field exists</li>
      </ul>
  </details>
  
  ### What will collations provide in a text search?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Needed for correctness of text searching. Specifies the level of correctness</li>
        <li>Case insensitive indexes. Specifies if case senseitive or not</li>
      </ul>
  </details>
  
  ### Foreground indexes

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Used to block all incoming operations on the DB until the index was built. But as of WireTiger and the latest Mongo this is no longer the case. Operations are interleaved.</li>
      </ul>
  </details>

### Background indexes

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Before the latest Mongo/WireTiger release this was an option and would allow for indexes to build without blocking operations. But was much slower to build and impacted performance during the process.</li>
      </ul>
  </details>
  
  ### During a query how are query plans created?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Multiple query plans are created. And actually the Executor executes multiple plans for a period of time to see which performs best and chooses winner</li>
        <li>The winning query plan is then cached for future operations</li>
      </ul>
  </details>
  
  ### When is the query plan cache cleared?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>server restarted</li>
        <li>amount of work performed by first portion of query exceeds amount of work by winning by factor of 10</li>
        <li>index is rebuilt</li>
        <li>index added or dropped</li>
      </ul>
  </details>
  
  ### The best query plan will havve:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>totalDocsExamined nReturned totalKeysExamined all the same or close to the same number</li>
      </ul>
  </details>
  
  ### If an index is not being used by a query plan how can you force it to be used?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>By using hint</li>
        <li>db.collection.find.hint({field1: 1, field2: 1})</li>
        <li>or name can be used</li>
        <li>db.collection.find.hint("field1_1_field2_1")</li>
      </ul>
  </details>
  
  ### Which command will show the size of indexes?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.stats()</li>
      </ul>
  </details>
  
  ### Which command will show the size of indexes for a specific collection?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.stats()</li>
      </ul>
  </details>
  
  ### Indexes use what resources?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>disk - storing the index data</li>
        <li>memory - for operating on the index data structures</li>
      </ul>
  </details>
  
  ### What occurs if something like an index cannot fit into RAM?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Paging - rotating memory in and out of RAM and physical disk</li>
      </ul>
  </details>
  
  ### Which linux command will show memory statistics?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>free -h</li>
      </ul>
  </details>
  
  ### How do you specificy the size of the WireTiger cache?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>mongod --dbpath data --wiredTigerCacheSizeGB 1</li>
      </ul>
  </details>
  
  ### How to determine how much of an index is kept in RAM/cache?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.stats({indexDetails: true}).indexDetails.cache</li>
        <li>"bytes currently in the cache" - how much of index is in RAM</li>
        <li>"pages read into cache" - used to determine if paging is happeing too frequently</li>
      </ul>
  </details>
  
  ### What is the issue with a Right-end-side index, what causes it?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>When you index on something monotonically growing, like time, or actually even ObjectIds, it will populate only the "right side" of the index B-Tree.</li>
      </ul>
  </details>

### Low Level Benchmarking

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>File I/O performance</li>
        <li>Scheduler performance</li>
        <li>Memory allocation and transfer speed</li>
        <li>Thread performance</li>
        <li>Database server performance</li>
        <li>Transaction isolation</li>
      </ul>
  </details>
  
  ### Database Server Benchmarking

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Data set load</li>
        <li>Writes per second</li>
        <li>Reads per second</li>
        <li>Balanced workloads</li>
        <li>Read / Write ratio</li>
      </ul>
  </details>
  
  ### Distributed Systems Benchmarking

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Linearization</li>
        <li>Serialization</li>
        <li>Fault tolerance</li>
      </ul>
  </details>
  
  ### Good tool for benchmarking MongoDB?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>jepson.io</li>
      </ul>
  </details>
  
  ### In MongoDB, the WiredTiger storage engine provides concurrency at what level?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>WiredTiger uses document-level concurrency control for write operations.</li>
      </ul>
  </details>
  
  ### Cam journaling be disabled for replica sets?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>As of MongoDB 4.0, journaling cannot be disabled for replica set members.</li>
      </ul>
  </details>
  
  ### For determining disk latency issues which tool should be used?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>mongotop</li>
      </ul>
  </details>
  
  ### What does mongotop do?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>mongotop provides a method to track the amount of time a MongoDB instance mongod spends reading and writing data. mongotop provides statistics on a per-collection level. By default, mongotop returns values every second.</li>
      </ul>
  </details>
  
  ### What does mongostat do?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>mongostat utility provides a quick overview of the status of a currently running mongod or mongos instance. mongostat is functionally similar to the UNIX/Linux file system utility vmstat, but provides data regarding mongod and mongos instances.</li>
      </ul>
  </details>
  
  ### What is a Covered Query

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A covered query is a query that can be satisfied entirely using an index and does not have to examine any documents. An index covers a query when all of the following apply:</li>
        <li>* all the fields in the query are part of an index, and</li>
        <li>* all the fields returned in the results are in the same index.</li>
        <li>* no fields in the query are equal to null (i.e. {"field" : null} or {"field" : {$eq : null}} ).</li>
      </ul>
  </details>
  
  ### Use of indexes with sort:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>An index can support sort operations on a non-prefix subset of the index key pattern. To do so, the query must include equality conditions on all the prefix keys that precede the sort keys.</li>
        <li>For example with index: { a: 1, b: 1, c: 1, d: 1 }</li>
        <li>The following operations can use the index to get the sort order:</li>
        <li>db.data.find( { a: 5 } ).sort( { b: 1, c: 1 } )  -- { a: 1 , b: 1, c: 1 }</li>
        <li>db.data.find( { b: 3, a: 4 } ).sort( { c: 1 } ) -- { a: 1, b: 1, c: 1 }</li>
        <li>db.data.find( { a: 5, b: { $lt: 3} } ).sort( { b: 1 } ) -- { a: 1, b: 1 }</li>
      </ul>
  </details>
  
  ### Unique and hashed indexes

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>MongoDB does not support specifying a unique constraint on a hashed index. You can instead create an additional non-hashed index with the unique constraint on that field. MongoDB can use that non-hashed index for enforcing uniqueness on the field.</li>
      </ul>
  </details>
  
  ### Define idempotency

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>produce the same results whether applied once or multiple times</li>
      </ul>
  </details>
  
  ### What is the Replica Set Oplog

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The oplog (operations log) is a special capped collection that keeps a rolling record of all operations that modify the data stored in your databases.</li>
      </ul>
  </details>
  
  ### BSON and documents

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>MongoDB stores data records as BSON documents. BSON is a binary representation of JSON documents, though it contains more data types than JSON.</li>
        <li>BSON is actually used to describe the document itself not just the fields it contains</li>
      </ul>
  </details>
  
  ### Benchmarking Anti-Patterns

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Database swap replace</li>
        <li>Using mongo shell for write and read requests (not reflective of typical app usage)</li>
        <li>Using mongoimport to test write response</li>
        <li>Local laptop to run tests (use a server)</li>
        <li>Using default MongoDB parameters (use production settings - eg authentication, high availability)</li>
      </ul>
  </details>
  
  ### OpLog and Updates to Multiple Documents at Once

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The oplog must translate multi-updates into individual operations in order to maintain idempotency. This can use a great deal of oplog space without a corresponding increase in data size or disk use.</li>
      </ul>
  </details>
  
  ### Primary Shard

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Each database in a sharded cluster has a primary shard that holds all the un-sharded collections for that database. Each database has its own primary shard. The primary shard has no relation to the primary in a replica set.</li>
        <li>Again, all UNSHARDED COLLECTIONS exist on the Primary Shard</li>
        <li>The mongos selects the primary shard when creating a new database by picking the shard in the cluster that has the least amount of data</li>
        <li>MongoDB initializes the first sharding server as Primary</li>
      </ul>
  </details>
  
  ### Replica Sets

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A replica set is a group of mongod instances that maintain the same data set. A replica set contains several data bearing nodes and optionally one arbiter node. Of the data bearing nodes, one and only one member is deemed the primary node, while the other nodes are deemed secondary nodes.</li>
      </ul>
  </details>
  
  ### How do Updates to Multiple Documents at Once work? (Not with transactions)

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The oplog must translate multi-updates into individual operations in order to maintain idempotency. This can use a great deal of oplog space without a corresponding increase in data size or disk use.</li>
      </ul>
  </details>
  
  ### What is a Replica Set

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A replica set is a group of mongod instances that maintain the same data set. A replica set contains several data bearing nodes and optionally one arbiter node. Of the data bearing nodes, one and only one member is deemed the primary node, while the other nodes are deemed secondary nodes.</li>
      </ul>
  </details>
  
  ### When a chunk is in flight from one shard to another during a migration process, where are reads to that chunk directed

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The Donor shard - the shard where the chunk is coming from can still process reads and writes</li>
      </ul>
  </details>
  
  ### How do you choose a good shard key?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The ideal shard key allows MongoDB to distribute documents evenly throughout the cluster.</li>
      </ul>
  </details>
  
  ### What is an example of a bad shard key?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Anything that changes monotonically</li>
        <li>ObjectIds are actually monotonic</li>
        <li>Time is monotonic</li>
        <li>Anything that incrememts steadily is monotonic</li>
        <li>The asterisk here is that if a monotonic key is chosen it can be hashed</li>
      </ul>
  </details>
  
  ### The _id field across shards

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>If the _id field is not the shard key or the prefix of the shard key, _id index only enforces the uniqueness constraint per shard and not across shards.</li>
      </ul>
  </details>
  
  ### Why does MongoDB use BSON rather than JSON?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>BSON supports more data types than JSON</li>
        <li>BSON includes metadata to describe a document/object</li>
      </ul>
  </details>
  
  ### Which writes are atomic?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Update to a single document in shard</li>
        <li>Update to multiple document in replica set using a transaction</li>
        <li>Update to a single document in replica set</li>
      </ul>
  </details>
  
  ### Are Decimal128 Int32 and Int64 BSON datatypes?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Yes</li>
      </ul>
  </details>
  
  ### IF using addToSet to add an array to another array and there is any overlap, one item exists in both arrays what will happen?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Nothing will be added, the set/array will remain unchanged</li>
        <li>The $addToSet operator adds a value to an array unless the value is already present, in which case $addToSet does nothing to that array.</li>
      </ul>
  </details>
  
  ### When considering a good data model for your needs with MongoDB, which of the following should you prioritize?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Access Patterns</li>
        <li>Potential growth of Documents</li>
        <li>NOT DE DUPLICAITON</li>
      </ul>
  </details>
  
  ### Which of the following describe the primary reasons MongoDB supports replication?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>High availability</li>
        <li>Prevent Downtime in case of disaster</li>
        <li>NOT HORIZONTAL SCALING - THAT IS WHAT SHARDING IS FOR</li>
      </ul>
  </details>
  
  ### Where can unsharded collections be found in a sharded MongoDB?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The primary shard</li>
      </ul>
  </details>
  
  ### In which situations can we assume sharding will be an effective strategy?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Mongo cannot keep up with operations</li>
        <li>Too large data set</li>
        <li>Improve read performance</li>
        <li>Improve backup and restore time</li>
      </ul>
  </details>
  
  ### In a sharded cluster, which of the following indexes should contain only unique values?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>The _id field</li>
        <li>The shard key is just what defined which shard the data goes to it iss not a unique ID for the document.</li>
        <li>This goes agains the documentation but "In a sharded cluster, _id must also be unique across the sharded collection because documents may migrate to another shard, and identical values would prevent the document to be inserted in the receiver shard</li>
      </ul>
  </details>
  
  ### What will "low cardinality" or an insufficiently granularity lead to with a sharded cluster?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Jumbo chunks - chunks so large that they cannot be moved from shard to shard</li>
      </ul>
  </details>
  
  ### Is Mongo Schema Less

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Yes - Also referred to as a dynamic schema</li>
      </ul>
  </details>
  
  ### What file format does mongoimport/mongoexport work on?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>JSON/CSV/etc</li>
      </ul>
  </details>
  
  ### What format does mongodump/mongorestore?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>BSON</li>
      </ul>
  </details>

### Arbiters have what responsibilities in a replica set?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>They do not hold data but do participate in elections</li>
      </ul>
  </details>
  
  ### With a mongo query what does the $ operator act as?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Place holder for the first element that matches the query document</li>
      </ul>
  </details>
  
  ### what does the all positional operator $[] indicate in the update operation?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>should modify all elements in the specified array field.</li>
      </ul>
  </details>
  
  ### Multikey Indexes

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>To index a field that holds an array value</li>
      </ul>
  </details>
  
  ### Compound Indexes

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>single index structure holds references to multiple fields</li>
      </ul>
  </details>
  
  ### What is a Capped Collection?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Capped collections are fixed-size collections</li>
        <li>support high-throughput operations that insert and retrieve documents based on insertion order</li>
        <li>Capped collections work in a way similar to circular buffers: once a collection fills its allocated space, it makes room for new documents by overwriting the oldest documents in the collection.</li>
      </ul>
  </details>
  
  ### What is the byte size of ObjectID

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>12</li>
      </ul>
  </details>
  
  ### How can you get the last error that occurred in the shell?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>getLastErrror</li>
      </ul>
  </details>
  
  ### What are the types of JSON?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Array</li>
        <li>Object</li>
        <li>String</li>
        <li>Boolean</li>
        <li>Number</li>
        <li>Null</li>
        <li>Undefined</li>
      </ul>
  </details>
  
  ### What are the priorities of BSON?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Speed</li>
        <li>Space</li>
        <li>Flexibility</li>
      </ul>
  </details>
  
  ### In Mongo, in general what is the Atomicity of Write Operations?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Single Document Atomicity</li>
        <li>In MongoDB, a write operation is atomic on the level of a single document, even if the operation modifies multiple embedded documents within a single document.</li>
      </ul>
  </details>
  
  ### Without a transaction using db.collection.updateMany atomicity

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>When a single write operation (e.g. db.collection.updateMany()) modifies multiple documents, the modification of each document is atomic, but the operation as a whole is not atomic.</li>
      </ul>
  </details>
  
  ### Difference between findAndModify and update?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>findAndModify returns the document</li>
      </ul>
  </details>
  
  ### insert vs insertOne insertMany

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Insert is deprecated - use insertOne or insertMany</li>
      </ul>
  </details>
  
  ### db.collection.save

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.save is like a update with upsert : true</li>
      </ul>

  </details>

### db.collection.update using $set but no document found, what happens?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>it will insert a new document with $set fields</li>
      </ul>
  </details>
  
  ### Difference between $all and $in

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>$all must contain all values in array</li>
        <li>$in if contains any values in the array</li>
      </ul>
  </details>
  
  ### Using dot.notation to an array vs $elemMatch

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>$elemMatch can do conditions on each element in array, is one element in the array matches then it is true</li>
        <li>If using dot notation then it must match on all elements in array</li>
      </ul>
  </details>
  
  ### How to add documents to an array in a document?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>{ $push: { <field>: { $each: [ <value1>, <value2> ... ] } } }</li>
      </ul>
  </details>
  
  ### How to remove the first item from a documents array?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Remove the first item with $pop -1</li>
        <li>db.students.update( { _id: 1 }, { $pop: { scores: -1 } } )</li>
      </ul>
  </details>

### What does $pull do?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>$pull: removes all values from an array that match a condition:</li>
        <li>db.stores.update( { }, { $pull: { fruits: { $in: [ "apples", "oranges" ] }, vegetables: "carrots" } }, { multi: true } )</li>
        <li>After the operation, the fruits array no longer contains any "apples" or "oranges" values, and the vegetables array no longer contains any "carrots" values</li>
      </ul>
  </details>
  
  ### What does $pullAll do?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.survey.update( { _id: 1 }, { $pullAll: { scores: [ 0, 5 ] } } )</li>
        <li>will remove all scores 0, 5 from the scores array</li>
        <li>removes all values from the array</li>
      </ul>
  </details>
  
  ### What does $push with the $position operator do?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>With $push you can specify where in the array to push the value with the $position operator:</li>
        <li>db.students.update( { _id: 1 }, { $push: { scores: { $each: [ 50, 60, 70 ], $position: 0 } } } )</li>
        <li>Will push to the front of the array</li>
      </ul>
  </details>
  
  ### To remove items from an array use?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>$slice</li>
        <li>db.students.update( { _id: 3 }, { $push: { scores: { $each: [ ], $slice: -3 } } } )</li>
        <li>You have to use $push with $each as empty array and then $slice</li>

      </ul>

  </details>

### How to drop a collection?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collectionName.drop()</li>
      </ul>
  </details>
  
  ### Ways to delete documents from a collection?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.Collection.remove</li>
        <li>db.Collection.deleteOne</li>
        <li>db.Collection.deleteMany</li>
        <li>findOneAndDelete will return the deleted document and delete the document</li>
      </ul>
  </details>

### What is a TTL index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Will remove documents automatically after amount of time or at specific time</li>
        <li>db.eventlog.createIndex( { "lastModifiedDate": 1 }, { expireAfterSeconds: 3600 } )</li>
        <li>So it will remove the document 3600 seconds after the value of lastModifiedDate</li>
      </ul>
  </details>
  
  ### What is a partial index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Partial indexes only index if meeting a filter expression</li>
      </ul>
  </details>
  
  ### What is a sparse index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>A sparse will only index documents that contain a certain field</li>
      </ul>
  </details>
  
  ### Why would you hide an index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>You can hide and index which will prevent the planner from using it</li>
        <li>This is just a good way to test out if removing an index will negatively impact performance because then u can unhide it</li>
        <li>db.restaurants.hideIndex( "borough_1_ratings_1" );</li>
        <li>Then to unhide it</li>
        <li>just us db.collection.unHideIndex</li>
      </ul>
  </details>
  
  ### What is the schema of the GEOJSON objects?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>{ type: "Point", coordinates: [ 40, 5 ] }</li>
        <li>{ type: "LineString", coordinates: [ [ 40, 5 ], [ 41, 6 ] ] }</li>
        <li>{ type: "Polygon", coordinates: [ [ [ 0 , 0 ] , [ 3 , 6 ] , [ 6 , 1 ] , [ 0 , 0  ] ] ] }</li>
      </ul>
  </details>
  
  ### To find all documents within a sphere use?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>centerSphere</li>
        <li>db.places.find( { loc: { $geoWithin: { $centerSphere: [ [ -88, 30 ], 10/3963.2 ] } } } )</li>
      </ul>
  </details>
  
  ### To find a document near a point?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Use  field: $near { $geometry: { type: Point }}</li>
      </ul>
  </details>
  
  ### For a field to be used in a geo query it must be indexed as a certain type?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>2d</li>
        <li>2dsphere - the new one to use - this way you can get a distance from the point you query against</li>
      </ul>
  </details>
  
  ### For text indexes if you want certain fields to hold more weight in the search how do you do this?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>When creating the index, as the option object specify the weights object</li>
        <li>db.blog.createIndex({ content: "text", keywords: "text", about: "text" }, { weights: { content: 10, keywords: 5 }, name: "TextIndex" })</li>
      </ul>
  </details>
  
  ### How do you perform a text search on a field with a TextIndex?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>$text operator</li>
        <li>it's key is an object with the following properties</li>
        <li>search, language, caseSensitive, diacriticSensitive</li>
      </ul>
  </details>
  
  ### What is a Collation?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Collation allows users to specify language-specific rules for string comparison, such as rules for lettercase and accent marks</li>
        <li>strength property is to what level comparison happens. Is punctuation taken into account? etc</li>
        <li>Locale?</li>
      </ul>
  </details>
  
  ### How do you create a hashed index with the createIndex command

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.createIndex({key: 'hashed'})</li>
      </ul>
  </details>
  
  ### totalDocsExamined == 0 means it is a?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Covered query</li>
      </ul>
  </details>
  
  ### Good index performance can be seen by what ratio?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>nReturned and totalkeysExamined being equal, 1 to 1</li>
      </ul>
  </details>
  
  ### Again, what is the rule for creating compound indexes?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>equality, sort, range</li>
      </ul>
  </details>
  
  ### How can you create a hidden index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>db.collection.createIndex( { borough: 1 }, { hidden: true } );</li>
      </ul>
  </details>
  
  ### Steps in a Rolling Index Builds on Replica Sets

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Stop a secondary, start as standalone</li>
        <li>Create the index</li>
        <li>Restart as a replica</li>
        <li>Repeat for all secondaries</li>
        <li>For primary finally, run stepDown first to transfer primary to a secondary, then do the previous steps</li>
      </ul>
  </details>
  
  ### Steps in a Rolling Index Builds on Sharded Clusters

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>Connect to mongos and run sh.stopBalancer()</li>
        <li>Determine the Distribution of the Collection - db.records.getShardDistribution();</li>
        <li>This way you know which replicas/which hosts you need to create indexes on</li>
        <li>Now follow the steps fora rolling index build on a replica set again here</li>
      </ul>
  </details>
  
  ### What is the Working Set?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>indexes and documents kept in RAM</li>
      </ul>
  </details>
  
  ### What is GridFS?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>GridFS is for storing documents larger than the 16MB limit</li>
        <li>Divides the document into chunks , stores each as separate document</li>
        <li>255 KB file size default</li>
      </ul>
  </details>
  
  ### What BSON type do I use for monetary fields?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>NumberDecimal</li>
        <li>128 bit exact precision for monetary values</li>
      </ul>
  </details>
  
  ### What is the Nested Set Graph style

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>You have Left and right fields</li>
        <li>Left field is the index of how   many nodes were iterated to get to it</li>
        <li>Right field is on the way back</li>
      </ul>
  </details>
  
  ### For searching an array of strings ([‘"str1”, “str2”]) do  you need a special index?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>No</li>
      </ul>
  </details>
  
  ### After creating a view can I change the indexes used by the view?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>No, the view is a pipeline using other collections. The indexes are on those collections.</li>
      </ul>
  </details>
  
  ### NumberDecimal is better than NumberLong and Double because:

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>* Provides exact precision when working with base 10 floating-point numbers</li>
        <li>* Less vulnerable to systematic rounding errors than double</li>
      </ul>
  </details>
  
  ### What is the Outlier pattern?

  <details>
    <summary>Click here for the solution</summary>
      <ul>
        <li>If you have a few documents with fields that grow very very large you can create a new collection, move that information to documents in those collections and reference them</li>
      </ul>
  </details>

Oplog stores high-level transactions that modify the database (queries are not stored for example), like insert this document, update that, etc. Oplog is kept on the master and slaves will periodically poll the master to get newly performed operations (since the last poll). Operations sometimes get transformed before being stored in the oplog so that they are idempotent (and can be safely applied many times).

Journal on the other hand can be switched on/off on any node (master or slave), and is a low-level log of an operation for the purpose of crash recovery and durability of a single mongo instance. You can read low-level op like 'write these bytes to this file at this position'.

NOTE: Starting in MongoDB 4.0, you cannot turn journaling off for replica set members that use the WiredTiger storage engine

https://docs.mongodb.com/manual/reference/replica-configuration/

Replica Set Configuration

version and term

version
Type: int

An incrementing number used to distinguish revisions of the replica set configuration document from previous iterations of the configuration.

Changed in version 4.4: Replica set members use term and version to achieve consensus on the "newest" replica configuration. When members compare replica configuration documents, the configuration document with a larger term is considered the "newest". If term is the same or absent, the configuration document with the larger version is considered "newest".

term
Type: int

New in version 4.4.

Only available with featureCompatibilityVersion (fCV) "4.4" or later.

An incrementing number used to distinguish revisions of the replica set configuration document from previous iterations of the configuration. The term of a configuration document matches the term of the replica set primary which performed the reconfiguration. The primary increments its term each time it steps up after winning an election. The primary ignores the term field if set explicitly in the replSetReconfig operation.

Issuing a force reconfiguration removes the term field. When the primary next issues replSetReconfig without force, it sets the term to its own term.

Replica set members use term and version to achieve consensus on the "newest" replica configuration. When members compare replica configuration documents, the configuration document with a larger term is considered the "newest". If term is the same or absent, the configuration document with the larger version is considered "newest".

Change Stream Aggregation Pipeline

https://docs.mongodb.com/manual/changeStreams/

You can control change stream output by providing an array of one or more of the following pipeline stages when configuring the change stream:

$addFields
$match
$project
$replaceRoot
$replaceWith (Available starting in MongoDB 4.2)
$redact
$set (Available starting in MongoDB 4.2)
$unset (Available starting in MongoDB 4.2)
