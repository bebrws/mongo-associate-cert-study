# Problem

Operations requiring availability of CPU cycles:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Page Compression</li>
    <li>Data Calculation</li>
    <li>Aggrgation Framework Operations</li>
    <li>Map Reduce</li>
	</ul>
</details>

Main resources MongoDB relies on to operate:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>CPU for processing and calculations</li>
    <li>Memory for execution -> IMPORTANT!</li>
    <li>Disk and IO for persistency and communications between servers or within host processes</li>
	</ul>
</details>

RAM having come down in price makes prevalence of dbs that are designed around usage of memory. It's also 25x faster than SSD's.

Operations depending heavily on memory include:

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

MongoDB uses CPU for:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Storage Engine</li>
    <li>Concurrency Model</li>
	</ul>
</details>

MongoDB uses CPU for:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>Storage Engine</li>
    <li>Concurrency Model</li>
	</ul>
</details>

By default, MongoDB will try to use all available cores to respond to incoming requests.

MongoDB RAID Consideratons - Preferred RAID - Non-preferred RAID:

<details>
  <summary>Click here for the solution</summary>
    <ul>
    <li>DO NOT USE RAID 5, RAID 6.</li>
    <li>Also avoid RAID 0 - has good write performance but limited availability, can lead to reduced performance on read operations.</li>
    <li>RAID 10 provides benefits needed by MongoDB</li>
	</ul>
</details>

Networking performance considerations:

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
