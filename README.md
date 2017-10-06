# check_rocketchat_user_status

check_rocketchat_user_status is a Nagios/Icinga2 plugin to check the online status of a [Rocket.Chat](https://rocket.chat) user, e.g. if a [Hubot](https://hubot.github.com/) user is online via [Hubot adapter](https://github.com/RocketChat/hubot-rocketchat) for Rocket.Chat.

# Installation

* `cp check_rocketchat_user_status /usr/local/lib/nagios/plugins/`

# Configuration

For database configuration see `DEFAULTS`.

# Usage

see `check_rocketchat_user_status -h` for help

```
Usage: check_rocketchat_user_status [-h]

    -h             display this help and exit
    -u username
    -w warning  [online|away|offline]
    -c critical [online|away|offline]

Note: -w and -c are optional arguments.

For full debug trace use DEBUG=1 ./check_rocketchat_user_status

Please send feedback and bugreport to Marcus Schopen <marcus.schopen@uni-bielefeld.de>
```

* Example:

```
  :~$ check_rocketchat_user_status -u hubot -c offline
  :~$ STATUS OK: user 'hubot' is online | UserStatus=2
```
