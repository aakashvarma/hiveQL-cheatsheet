### 1. Create Database:
    CREATE DATABASE IF NOT EXISTS [database_name];
    
### 2. Show Database:
    SHOW DATABASES;

### 3. Create Tables in Hive:
    CREATE TABLE IF NOT EXISTS [table_name](
        variable1 datatype1,
        variable2 datatype2,
        ..... )
        ROW FORMAT DELIMITED
        FIELDS TERMINATED BY ‘,’
        STORED AS TEXTFILE
        
#### ROW FORMAT DELIMITED:
This line is telling Hive to expect the file to contain one row per line. So basically, we are telling Hive that when it finds a new line character that means, it is a new record.

#### FIELDS TERMINATED BY ‘,’: 
This is similar to the one above, but instead of rows this is for columns, this way Hive knows what delimiter you are using in your files to separate each column. If nothing is set the default will be used (which is ctrl-A)

#### STORED AS TEXTFILE: 
This is to tell Hive what type of file to expect. The other type of file that can be consumed is Sequence Files (Hadoop’s binary file format).

### 4. Alter tables in Hive:
Add columns:
    
    ALTER TABLE [table_name]  ADD COLUMNS(id int, name string);
Replace an existing column with a new column:
    
    ALTER TABLE CHANGE [existing column] [new_column] [datatype];
Ex:
    
    ALTER TABLE CHANGE id name_id int;
    
