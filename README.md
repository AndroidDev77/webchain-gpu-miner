# webchain-miner

webchain-miner is a high performance Webchain (WEB) GPU miner, support for Windows.
Originally based on XMRig with changes that allows mining WEB on AMD GPUs.

#### Table of contents
* [Features](#features)
* [Download](#download)
* [Usage](#usage)
* [Algorithm variations](#algorithm-variations)
* [Common Issues](#common-issues)
* [Other information](#other-information)
* [Donations](#donations)
* [Contacts](#contacts)

## Features
* High performance.
* Official Windows support.
* Small Windows executable, without dependencies.
* Support for backup (failover) mining server.
* keepalived support.
* Command line options compatible with XMRig.
* It's open source software.

## Download
* Binary releases: https://github.com/webchain-network/webchain-miner/releases
* Git tree: https://github.com/webchain-network/webchain-miner.git
  * Clone with `git clone https://github.com/webchain-network/webchain-miner.git` :hammer: [Build instructions](https://github.com/xmrig/xmrig/wiki/Build).

## Usage

### Options
```
  -o, --url=URL            URL of mining server
  -O, --userpass=U:P       username:password pair for mining server
  -u, --user=USERNAME      username for mining server
  -p, --pass=PASSWORD      password for mining server
  -t, --threads=N          number of miner threads
  -k, --keepalive          send keepalived for prevent timeout (need pool support)
  -r, --retries=N          number of times to retry before switch to backup server (default: 5)
  -R, --retry-pause=N      time to pause between retries (default: 5)
      --cpu-affinity       set process affinity to CPU core(s), mask 0x3 for cores 0 and 1
      --cpu-priority       set process priority (0 idle, 2 normal to 5 highest)
      --no-huge-pages      disable huge pages support
      --no-color           disable colored output
      --variant            algorithm PoW variant
      --donate-level=N     donate level, default 5% (5 minutes in 100 minutes)
      --user-agent         set custom user-agent string for pool
  -B, --background         run the miner in the background
  -c, --config=FILE        load a JSON-format configuration file
  -l, --log-file=FILE      log all output to a file
  -S, --syslog             use system log for output messages
      --max-cpu-usage=N    maximum CPU usage for automatic threads mode (default 75)
      --safe               safe adjust threads and av settings for current CPU
      --print-time=N       print hashrate report every N seconds
      --api-port=N         port for the miner API
      --api-access-token=T access token for API
      --api-worker-id=ID   custom worker-id for API
  -h, --help               display this help and exit
  -V, --version            output version information and exit
```

Also you can use configuration via config file, default **config.json**. You can load multiple config files and combine it with command line options.

## Common Issues
### HUGE PAGES unavailable
* Run webchain-miner as Administrator.

## Other information
* No HTTP support, only stratum protocol support.
* No TLS support.
* Default donation 5% (5 minutes in 100 minutes) can be reduced to 0% via command line option `--donate-level`.


### Maximum performance checklist
* Idle operating system.
* Do not exceed optimal thread count.

## Contacts
* curquhart90@gmail.com
