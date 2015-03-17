### Drill Log Collector
Collect drill logs from all Drill hosts in a cluster. Only collects a `diff` of the logs between the start and end flags. 

#### Usage
Set the checkpoint:
```
$ drill_log_collector -s
```

Now run your Drill queries, and any logs that are generated from now until the `-e` flag is passed will be collected.

End and collect the logs from the cluster nodes:
```
$ drill_log_collector -e [-x] [ -d <directory to save to>]
```
Using the `-x` flag with the `-e` flag will collect the logs but not clear the snapshots, this is useful if you'd like to collect the logs while a query is running.

Only works on MapR clusters for now.

