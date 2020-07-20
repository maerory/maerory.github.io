---
layout: post
title: "Sparkify Redshift ETL (Infra. as Code)"
date: 2020-07-15
---

### Summary

Create ETL pipeline using AWS redshift following 'Infrastructure as Code' format.

### Code As Infrastructure

- Prcoess of managing and provisioning computer data centers through machine-readable definition files
- Ease of repeatability by other users
- Might be hard to edit if co-working project

### Details

1. Most part of the necessary constants must be saved in the cfg for reference
2. Python boto3 library is used to establish connection between different services in AWS
3. Create a IAM role that takes control of database
4. Create redshift cluster through the new user
5. Attain the endpoint of the cluster, and run the necessary python file for loading using the connection

- Most SQL data loading is similar to the past queries

### Tools

- Python
- SQL

<span class="improved">Link</span> [Github Repo](https://github.com/maerory/udacity_data_engineering/tree/master/sparkify_redshift)
