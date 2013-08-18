vagrant_logstash_kibana
=======================

vagrant system using logstash ( elastic search, rabbitmq, redis, kibana)


Setup
=======================

On host navigate to vagrant folder (where this git source is located)

'cd ./vagrant/vagrant_logstash_kibana'

'vagrant up'

This should open up two virtal machines with the following of ports forwarded:

rabbit : 192.168.11.10 [this is a mesageing server running RabbitMQ and REDIS]
rabbit ports fowarded: 22 => 2222, 55672 => 55672, 15672 => 15672, 5601 => 5601

logstash: 192.168.11.50 [this stores logs mesages and aggergates them]
logstash ports forwarded: 22 => 2200, 9200 => 9200, 80 => 8080


First thing we should do is ssh into logstash [192.168.11.50 private to host] and start the elastic search instance
'~/elasticsearch-0.90.3/bin/elasticsearch -f'

Next we require another ssh into logstash [192.168.11.50 private to host] and start the logstash.  This particual config just 

'cd ~'
'java -jar ~/logstash/'


oh snap... its broke... i'll continue this later.
