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
mysql> USE BIL_359;
```

![usedb](https://user-images.githubusercontent.com/54469544/139894532-ed600009-ab73-428b-b0d3-577a4189b6aa.png)

We want to create table with 3 columns as id, name, age.

id is Primary Key and int,
name is Varchar,
age is int.


```
mysql> CREATE TABLE bil_359_omeraltuntas(id INT NOT NULL AUTO_INCREMENT, name VARCHAR(50) NOT NULL, age INT NOT NULL, PRIMARY KEY(id));

```


![createtable](https://user-images.githubusercontent.com/54469544/139907188-ad946eac-0955-4a1a-9826-8b2f356c3b2e.png)


Verify that the table is created using the DESCRIBE command:
```
mysql> DESCRIBE bil_359_omeraltuntas;
```

![describe](https://user-images.githubusercontent.com/54469544/139907142-2d753cdd-1359-45d1-b0a9-482c0474e2e8.png)

# Insert Rows to Table

Insert row to table:

```
mysql> INSERT INTO bil_359_omeraltuntas(name, age) VALUES("omer altuntas", 20);
```

![insert](https://user-images.githubusercontent.com/54469544/139907227-7944862e-c8a9-4e2e-b23a-529c5ef1ce55.png)

Verify that the row is inserted using the SELECT command:

```
mysql> SELECT * FROM bil_359_omer_altuntas;
```

![select](https://user-images.githubusercontent.com/54469544/139911237-926bd59b-c7a8-4d69-921b-2220ba6523a9.png)


Now Insert many row:

```
mysql> INSERT INTO bil_359_omer_altuntas(name, age) VALUES ("muhammed basoglu", 20), ("ayse yilmaz", 29), ("sezen aksu", 50);
```

![insertMany](https://user-images.githubusercontent.com/54469544/139911191-df01591a-a9cb-4f54-bef3-0628142c2d8f.png)

Type it again:

```
mysql> SELECT * FROM bil_359_omer_altuntas;
```

![select2](https://user-images.githubusercontent.com/54469544/139911956-593c1022-68a0-4f65-ac86-3e92df215fe1.png)

# Backup Single Table

Logout from MySql

```
mysql> exit;
```

Type it to backup single table

```
$ sudo mysqldump BIL_359 bil_359_omer_altuntas > bil_359_omer_altuntas.sql
```

Now Create different Database:

```
$ sudo mysql -u root
```

```
mysql> CREATE DATABASE BIL_359_BACKUP;
```

And logout:

```
mysql> exit;
```

Type this to restore table:

```
$ sudo mysql -u root BIL_359_BACKUP < bil_359_omer_altuntas.sql

```

Check.

```
$ sudo mysql -u root
```

```
mysql> USE BIL_359_BACKUP;
```

```
mysql> SELECT * FROM bil_359_omer_altuntas;
```
