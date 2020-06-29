---
layout: post
title: "Sparkify Cassandra ETL"
date: 2020-06-29
---

### Summary

Create a ipynb ETL pipeline of NoSQL database using Cassandra

### NoSQL Advantages

- Can handle large volumes of structured/semi-structured/unstructured data
- OOP based that is easy to use and flexible
- Efficient in scaling horizontally
- Examples: MongoDB, Cassandra

### Sparkify Data

- NoSQL system requires the user to design the table according to the queries that we want to run.
- We create 3 tables, each with different analytic purpose.
  - Session Song Info: Keeps track of song information associated with the given session id and the item of the session. This allows us to comphrehend what type of music is popular in give session which might be associated with different regions
  - Song Playlist Session: Keeps track of the users playlist for each session. This allows us to build the relationship between user and the session.
  - Song Listener Info: Keeps track of users listening histroy. This is useful for generating recommendation system according to the users' past history.

### Tools

- Cassandra (CQL)
- Python

<span class="improved">Link</span> [Github Repo](https://github.com/maerory/udacity_data_engineering/blob/master/sparkify_cassandra/sparkify_cassandra.ipynb)
