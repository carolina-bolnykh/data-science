connecting R to a database:
- working with data larger than memory
- install.packages("RSQLite")
- dbGetQuery(delay.con,"SELECT COUNT(*),Year FROM AirlineDelay WHERE Year=1987")
- dbGetQuery is an R function that sends an SQL query to the database and waits for the result
