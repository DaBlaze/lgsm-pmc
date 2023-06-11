# lgsm-pmc

A simple script to help make managing a PaperMC LinuxGSM server a little easier.

This small script makes it easy to use regular minecraft console commands through bash script execution.

## Installation

**This guide assumes PaperMC is installed using the [official LinuxGSM documentation](https://linuxgsm.com/servers/pmcserver/)**

You should be logged into the server under your LinuxGSM user account.

In the home directory (/home/pmcserver), perform the following:

```bash
wget https://raw.githubusercontent.com/DaBlaze/lgsm-pmc/main/lgsm-pmc
chmod +x lgsm-pmc
```

## Usage

```
./lgsm-pmc [option]

backup                  b       | Stop and backup the server with an alert and delay.
ban-ip                  bi      | Ban an ip from the server.
ban-user                bu      | Ban a user from the server.
broadcast               bc      | Send a broadcast message to the server (Remember quotes!).
restart                 r       | Restart the server with an alert and delay.
start                   st      | Start the server.
stop                    sp      | Stop the server with delay.
unban-ip                ui      | Unban an ip from the server.
unban-user              uu      | Unban a user from the server.
update-lgsm             ul      | Update lgsm with an alert and delay.
whitelist-add           wa      | Add user to server whitelist.
whitelist-remove        wr      | Remove user from server whitelist.
```

### Cron Usage

#### As User:

```bash
* * * * * [/path/to/script] [command] > /dev/null 2>&1
```

#### As Root:

```bash
* * * * * su - username -c '[/path/to/script] [command]' > /dev/null 2>&1
```
