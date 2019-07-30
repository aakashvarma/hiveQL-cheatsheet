### Create Database:
    CREATE DATABASE IF NOT EXISTS [database_name];
    
### Show Database:
    SHOW DATABASES;

### Create Tables in Hive:
    CREATE TABLE IF NOT EXISTS [table_name](
        variable1 datatype1,
        variable2 datatype2,
        ..... )
        ROW FORMAT DELIMITED
        FIELDS TERMINATED BY ‘,’
        STORED AS TEXTFILE
        
#### ROW FORMAT DELIMITED:
This line is telling Hive to expect the file to contain one row per line. So basically, we are telling Hive that when it finds a new line character that means is a new records.

#### FIELDS TERMINATED BY ‘,’: 
This is really similar to the one above, but instead of meaning rows this one means columns, this way Hive knows what delimiter you are using in your files to separate each column. If none is set the default will be used which is ctrl-A

#### STORED AS TEXTFILE: 
This is to tell Hive what type of file to expect. The other type of file that can be consumed is Sequence Files (Hadoop’s binary file format).

