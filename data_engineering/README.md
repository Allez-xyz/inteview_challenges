# Data engineer position challenges

Fork this folder and put all the relevant files in the relevant folder, e.g. if you're doing task 1 all the relevant files should be in data_engineering/task_1. 

## Task 1: Index event data and ETL pipeline into Clickhouse

The goal of this task is to index event data for Morpho contracts using [Josh Stevens'](https://github.com/joshstevens19) [rindexer](https://rindexer.xyz) into a hosted postgres database and ETL the data into a hosted clickhouse database.

### A breakdown of the task:

1- Setup a hosted postgres database using [neon](https://neon.tech) and a hosted column-oriented database, preferrably [clickhouse](https://clickhouse.com).

2- Fill and debug rindexer.yaml and get it running on your favorite cloud provider: we want you to index Morpho Blue, Public Allocator, two MetaMorpho vaults of your choice (choose wisely) and Metamorpho Factory. See [Morpho docs](https://docs.morpho.org) to understand all this lingo.

3- Port all data from neon to clickhouse.


### Delierables
- share with us your configuration file for rindexer
- share with us credentials to connect to your newly setup clickhouse database (you better assume that we will sniff around and/or delete/alter/truncate everything if you grant us the permissions)
- share with us key metrics around the whole indexing process (the metrics you decide to include or leave out of what you share will say a lot)
- explain to us the issues you've faced while setting up this project
- explain to us the set of trade-offs you've decided to make when choosing your solution for ETL-ing data from neon to clickhouse and how you're transforming data


### The questions we will ask when judging your setup

Priority 0: Did you involuntarily leak credentials, keys, setup the wrong permissions ?

Priority 1.0: Correctness. Is the data correct ? Is the typing for the columns right and efficient ? Are there events missing ? What was your process for checking that you had everything right ?
Priority 1.1: What are the key resources you're consuming and how much of them are you consuming ?

Priority 2.0: Is the solution elegant ? Is it easy to maintain and upgrade ? How long did it take you to do ?



