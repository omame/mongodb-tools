# mongodb-tools
Scripts that I find useful for managing MongoDB

#### mongodb-ebs-snapshot

Takes consistent snapshots of MongoDB data directories stored on EBS volumes.
Then expires old snapshots assuming each snapshot is taken at hh:00.<br />
The expiration policy is to keep 2 days of hourly snapshots, 2 weeks of daily
snapshots at 00:00 and one year of monthly snapshots taken at 00:00 on the
first day of the month.
The expirer is still pretty basic but it does the job if you're happy with its policy.

#### mongodb-oplog-window-size

Reports the MongoDB oplog window size in hours to a local statsd server.
