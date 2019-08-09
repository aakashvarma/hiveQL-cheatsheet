## Date functions

#### unix_timestamp()
Return type: Bigint(unittimestamp)
We get the current unix timestamp in seconds.

#### unix_timestamp(string date)
Return type: Bigint(unixtimestamp)
This function converts the date in format ‘yyyy-MM-dd HH:mm:ss’ into Unix timestamp. This will return the number of seconds between the specified date and the Unix epoch. If it fails, then it returns 0.

  select unix_timestamp('2000-01-01 10:20:30'); returns 1565331424

#### to_date(timestamp date)
Return type: 
