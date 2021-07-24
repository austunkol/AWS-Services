# `What is Database?`
- The existing information and stores this information in disks.
- The structured data is called a database.
- The database is an organized collection of data in which we can fetch the information based on the desired format and queries.

## `Type of Database`

![1a.png](./Images/1a.png)

- There are two leading types of Database storage
	- Relational Database - SQL
	- Non-Relational Database - NoSQL

- SQL stands for ` Structured Query Language`
- We usually prefer to call `Relational Database as SQL`
- `Non-Relational Database as NoSQL`

```
Note:
Databases make the information meaningful and useful
Database is an organized collection of data
```
## `What is SQL`
` Relational Databases`

![1b.png](./Images/1b.png)
- Oldest and currently most widely used database type.
- RD store data as `rows and columns` like Excel
- We called relational database because it concludes by using separate tables like `excel`
- These procesesses are called `Join`

## `Disadvantages`
- We need to update/add data into the database according to a determined scheme.
- It requires strict coordination with database developers.

## `What is NoSQL`

![1c.png](./Images/1c.png)

- NoSQL database is not based on SQL.
- The Non-relational database is a new database model is getting popular in recent years.

- It is designed to solve the problems
- The Non-Relational database keeps data as key data mappings in documents rather than tables.
- The documents are called `Collections` that store data in `JSON`

`Tip= Microsoft Excel is SQL -- Microsoft Word is NoSQL`

## `Advantages of NoSQL`
- NoSQL eliminates the need to coordinate with the Database developer when writing database programs.
- We don't need to know `SQL language`

** We can't use the `Join` process and lose the oppurtunity.

` Note= Difference between SQL and NoSQL is the JOIN process`

`Note= SQL is used to query complex data, NoSQL is desgined for simpler databases`


## `SQL vs. NoSQL`

![1d.png](./Images/1d.png)

## `Database Options in AWS`

![1e.png](./Images/1e.png)

- AWS supports both SQL and NoSQL database types.
- AWS provides solution with `AWS RDS` service.
- AWS offers different types of relational database engines:

```
Oracle
Microsoft SQL Server
MySQL
```

`Note= Amazon Aurora is open-source MySQL and PostgreSQL and AWS's database engine, under the Amazon RDS service.`

`Normally you can install these databases to EC2, but Amazon RDS service has taken the management from customers and made this service SaaS (Software as a Service).`

` AWS offers only its DynamoDB option in the NoSQL field.`

------

# `Amazon RDS`

- Amazon RDS is the SQL database service managed by AWS
- RDS enables to use of popular database engines like Oracle,Microsoft SQL Server, MySQL, PostgreSQL and MariaDB.
- RDS offers also own relational database product `Amazon Aurura`
----

## `Components of Amazon RDS`

![1f.png](./Images/1f.png)


 `Amazon RDS consists of 3 main components:`

- 1 `Database Engines` like MySQL, PostgreSQL, MariaDB, etc
- 2 `DB instance` which database software we choose will run.
- 3 `Storage Disk` which will be connected to the DB instance

`Note= As we can see , we can say Amazon RDS is similiar to EC2`

-----
## `Relational Database Engines on Amazon RDS`

![1g.png](./Images/1g.png)

- There are `6 Relational database engines with Amazon RDS`.

- `1 Amazon Aurora`
- Aurora is compatible with `MySQL and PostgreSQL`

- Aurora provides up to `five times` better performance than `MySQL` with the security, availability, and reliability.

- Commercial database at `one-tenth the cost`

- `2 Oracle`
- Oracle in minutes with cost-efficient and re-sizable hardware capacity.
- You can use existing `Oracle license or pay for license usage by hour`

- `3 Microsoft SQL Server`

- SQL Server makes it easy to set up, operate and scale SQL Server in the cloud.

- You can deploy multiple editions of SQL like `Express`, `Web`, `Standard`, and `Enterprise`

- `4 MySQL`
- is open source `rdbms`
- The code, applications, and tools you already use today with your existing databases can be used with Amazon RDS without any changes.

- `5 PostgreSQL`
- is a powerful open source `object-relational` database
- Runs and stored many programming languages like Java, Perl, Python, Ruby, Tcl, C/C++, and its own PL/pgSQL, which is similar to Oracle's PL/SQL.

- `6 MariaDB`
- You can deploy scalable MariaDB databases in minutes with cost-efficient and resizable hardware capacity
----
## `Relational Database Instance`

![1h.png](./Images/1h.png)

- DB instance as a database environment in the cloud with the compute and storage resources you specify.

- We select a DB Instance considering the CPU and RAM power in the RDS environment.

- RDS offers `On-Demand` and `Reserved Instance` options

- `Start` and `Stop` status are available just like EC2.
- We can `Stop` and run it again.
- `Amazon RDS` can only remain `Stop` status for 7 days. If the machine is not operation after 7th day, the machine is automatically started.

- RDS also allows the DB instance to be transferred to a more advanced and powerful machine without any interruption.

- You can run one or more DB instances, and each DB instance can support one or more databases or database schemas, depending on the engine type.
---
## `Amazon RDS DB Instance Storage`

![1j.png](./Images/1j.png)

- There are 3 types of Storage disks in Amazon RDS:

- `1 General Purpose (SSD) Storage`
- cost-effective storage
- RDS offers the General Purpose (SSD) Storage option, which has a storage capacity of `20 GB to 64 TB` as part of the disk infrastructure and gives a value of `3 IOPS per GB,` provided that it has an upper limit of up to 3000 IOPS in total.

- `2 Provisioned IOPs (SSD) Storage`
- For production application `fast and consistent I/O performance`
- Amazon RDS offers the `Provisioned IOPs (SSD) Storage` option, with `1000 to 80000 IOPs` and a storage capacity of `20GB to 64 TB`

- `3 Magnetic Storage`
- For backward compatibility
-  `Magnetic storage doesn't allow you to scale storage when using the SQL Server database engine`
- It is limited to a maximum size of `3 TB and 1,000 IOPS.`
- It doesn't support elastic volumes.
 