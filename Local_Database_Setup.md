### Open terminal and type the following commands:
```
$psql
$CREATE DATABASE med_dash; 
$\c med_dash
```


### Create seperate table for each csv file
```
$CREATE TABLE file_name (
    timestamp TIMESTAMP WITH TIME ZONE,
    bpm INTEGER,
    quality TEXT,
    source TEXT,
    restorative BOOLEAN
);
```

### Import csv file into the database table
```
$\COPY file_name FROM '/path_to/file_name' WITH (FORMAT csv, HEADER true, DELIMITER ',');
```

### Check if table is successfully created
```
$SELECT COUNT(*) FROM file_name;
```
