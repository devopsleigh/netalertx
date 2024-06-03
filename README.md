# NetAlertX

NetAlertX discovers and alerts when new network devices are found.

> The below config can be configured using the `app.conf` file, however I couldn't find a way to use an external secret file without deploying via CI/CD.

## Manual setup

Go to Settings and configure the following items.

### Set a password

Find `SETPWD`, check `Enable login` and set the password.

### Add UniFi Import connector

1. Create a unique UniFi admin account with network read access
1. Find `ARPSCAN_RUN` and set to `disabled`
1. Find `UNFIMP` and enter the following values:
   Name | Value
   --- | ---
   When to run | `schedule`
   Username | `NetAlertX`
   Password | 
   API version | `UDMP-unifiOS`
   Schedule | `*/5 * * * *`

### TODO

Configure publishers
