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
$ drill_log_collector -e [ -d <directory to save to>]
```

Only works on MapR clusters for now.

