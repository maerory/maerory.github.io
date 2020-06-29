---
layout: post
title: "Sparkify Postgre ETL"
date: 2020-06-28
---

### Summary

Create a python pipeline that ingest json log files and load it onto the sparkify database in appropriate tables

### SQL Advantages

- Adheres to the ACID principle:

  - Atomicity: Each transaction is either complete or rolled back
  - Consistencty: Data written to a database must be valid accodring to all rules
  - Isolation: Concurrent transaction do not contend with one another and acts sequentially
  - Durability: Transaction commit is permanent

- SQL database can scale vertically
- Can use joins to aggregate multiple tables in a single query
- Examples: MySQL, Microsoft SQL, PostgreSQL, Oracle

### Sparkify Data

- We apply the star schema in storing the sparkify data. Star schema splits the data into fact tables and dimension tables. Fact tables record measurements for a specific event that connects out to many dimension tables that records the specifics of each field of that events.
- Star Schema is one of the simplest and widely used DB design. We can use single join to create the relationship between the fact table and any dimension table. However, the data is denormalized and might have high level of redundancy.
- For sparkify, user playing a single song marks an event. This will form a fact table that records the information of user_id, timestamp of event, artists_id, and song_id.
- The dimension table will be users, artists, time, songs and save the details of each category.

### Result

The STAR schema is as below:

<figure>
  <center><img src="/assets/sparkify_schema.png" alt="Midnight" style="width:100%"></center>
  <figcaption>Schema for database sparkifydb</figcaption>
</figure>

### Tools

- Postgre SQL
- Python (Psycopg2, Pandas, Numpy)

<span class="improved">Link</span> [Github Repo](https://github.com/maerory/udacity_data_engineering/tree/master/sparkify_postgre)
