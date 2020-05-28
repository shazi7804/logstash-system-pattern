# Logstash grok pattern for system

Defined logstash grok pattern for system log

## How To

- Deploy pattern file to `/etc/logstash/patterns/system`

## Pattern

-  system log format pattern

  - CRONLOG_RUN_PARTS
  - CRONLOG_TIME_ISO8601
  - COMMANDLOG_SUDO
  - COMMANDLOG_SU

# Command log 

setting format of this

```
# /etc/profile.d/prompt_command.sh
export PROMPT_COMMAND='{ echo "date=$(date +"%Y-%m-%d %H:%M:%S"),from=${SSH_CLIENT},login=${SUDO_USER},user=${USER},pwd=$(pwd),exec=$(history 1|cut -c 8-)"; } >> /tmp/command.log'
```
