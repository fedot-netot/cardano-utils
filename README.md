
# Some tools/scripts/utilities for mantaining jormungandr node

##  `publish-jormungandr-stats`
   
Bash script that regularly send stats info to a Telegram channel. It may be helpfull
for realizing if somebody's node is on a wrong fork. When several pool operators send their pool
stats to the channel then all of them can check if his/her pool is out of sync with others.

### Usage

Run the script on host with `jormungandr` and `jcli`. Excample of publishing stats every ten minutes
on `@CardanoNodesHeartbeat` telegram channel if your stake pool ticker is `FREE1` and your telegram id `@fedot_netot`.

``` bash
publish-jormungandr-stats -p 'FREE1 (@fedot_netot)' -i 10 -a $ACCESS_TOKEN -c @CardanoNodesHeartbeat -r 'jcli rest v0 node stats'
```
