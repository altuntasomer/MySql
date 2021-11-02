# MySql Create New Database

Open Terminal and type this to Log into MySql as root:

```
$ sudo mysql -u root
```

![login](https://user-images.githubusercontent.com/54469544/139883678-ce8b16af-eee5-444c-8774-702556a4a1f0.png)

Type it to Create new Database

```
mysql> CREATE DATABASE BIL_359;
```

![createdb](https://user-images.githubusercontent.com/54469544/139889309-1231d47a-1437-4ad1-be11-e132f5971e5b.png)

# MySql Create New Table

Firstly select a Database

```
mysql> USE BIL_359
```

![usedb](https://user-images.githubusercontent.com/54469544/139894532-ed600009-ab73-428b-b0d3-577a4189b6aa.png)

We want to create table with 3 columns as id, name, age.

id is Primary Key and int,
name is Varchar,
age is int.


```
mysql> CREATE TABLE bil_359_omer_altuntas(id INT NOT NULL, name VARCHAR(50) NOT NULL, age INT NOT NULL, PRIMARY KEY(id));

```
