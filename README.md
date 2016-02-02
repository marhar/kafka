Here's some quick kafka tools.  I'm using Confluent Kafka which
differs from Apache Kafka in some command names, etc.

kaft -- kafka tool
==================

- kaft list args...
- kaft consume <topic> args...
- kaft produce <topic> args...
- kaft help

Any extra arguments are passed along to the low level kafka commands.

configuration
-------------

- set KAFT_INSTANCE to specify your configuration.
- put the configuration in $HOME/.kaft/instance-name

example:

```
~ $ cat $HOME/.kaft/localhost
ZOOKEEPER=localhost:2181
KAFKA_SERVER=localhost:9091

~ $ export KAFT_INSTANCE=localhost

~ $ kaft list
__consumer_offsets
foo
bar
...
```

superkaf -- local instance laptop convenience 
=============================================

This starts and stops a local kafka.  It's nice if you're on
a mac coz it starts the zookeeper and kafka server in tabs.

This came before kaft, I'll roll this into kaft later.

```
superkaf start
superkaf stop
```

starts and stops the zookeeper and kafa servers.  If you're in Terminal
on a Mac it does it in new tabs, nice and tidy.

```
superkaf status
superkaf help
```

gives the status (as best as I can tell), and gives some handy kafka
commands to get started.

Edit the file and set KAFDIR if you've got it installed in a different
place than me.

