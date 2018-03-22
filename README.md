# ansidockhapr
ansible starting a dockerized haproxy serving a static response

## how to start

1. adjust inventory to your needs (or use a different one alltogether)
1. run playbook: `ansible-playbook -i inventory start.yml`
1. the target host should now have configuration files present at /tmp/haproxy, which will be bind-mounted into the docker container.
1. the target host should begin serving http requests at port 8081 shortly after
1. open browser, connect to `http://<docker host>:8081/hello`
