## Date functions

#### unix_timestamp()
Return type: Bigint(unittimestamp)
We get the current unix timestamp in seconds.

#### unix_timestamp(string date)
Return type: Bigint(unixtimestamp)
This function converts the date in format ‘yyyy-MM-dd HH:mm:ss’ into Unix timestamp. This will return the number of seconds between the specified date and the Unix epoch. If it fails, then it returns 0.

    select unix_timestamp('2000-01-01 10:20:30'); returns 1565331424

#### from_unixtime(Bigint number_of_seconds)
Return type: string
The FROM_UNIXTIME function converts the specified number of seconds from Unix epoch and returns the date in the format ‘yyyy-MM-dd HH:mm:ss’.

    select from_unixtime(unix_timestamp()); reutrns 2019-08-09 06:23:55

#### to_date(string timestamp)
Return type: string
It will fetch and give the date part of a timestamp string

    > select to_date('2000-01-01 10:20:30'); 
    reutrns 2000-01-01
    > select to_date(current_date);
    returns 2019-08-09
    > select to_date(unix_timestamp());
    returns: ERROR because to_date takes only strings, timestamp, dtaewritable types where as we gave LONG/INT.
    
> NOTE: select to_date(from_unixtime(unix_timestamp())); ---- returns 2019-08-09
    
