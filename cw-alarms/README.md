# how to setup various alarms in cw

## for cpu utilization
- by default metric for cpu utilization sent every 5 mins
- so for a period of 5 mins, we can put avg aggregate with a threshold of say .5
- put how many data points should be breached say 10 out of 20 to go in Alart state
- give action for your alarm e.g. sending mail through sns