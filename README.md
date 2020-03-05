
# Some tools/scripts/utilities for mantaining jormungandr node

## `cardano-utils-common`

Lbrary with common functions that are used in other scripts.

##  `publish-jormungandr-stats`

Bash script that regularly send jcli stats info to a *Telegram* channel.

### Usage

Run the script on host with `jormungandr` and `jcli`. Excample of publishing stats every ten minutes
on `@CardanoNodesHeartbeat` *Telegram* channel if your stake pool ticker is `FREE1` and your *Telegram* id `@fedot_netot`.

``` bash
publish-jormungandr-stats -p 'FREE1 (@fedot_netot)' -i 10 -a $ACCESS_TOKEN -c @CardanoNodesHeartbeat -r 'jcli rest v0 node stats'
```

## `jormungandr-overseer`

This scrip observes jormungandr health. And if jormungandr is not running and syncing then start/restart it.
Also some statistics regularly published via *Telegram* channel.

## `publish-pool-stake`

This scrip collect and report pool stack information of the jormungandr node to stdout and the *Telegram*
channel via the *Telegram* Bot.

## `publish-pool-slots`

This scrip collect and report information about the own slots of the pool to stdout and the *Telegram*
channel via the *Telegram* Bot.
