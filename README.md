# docker-sample
docker sample

### run & create & down
run docker

<pre>
docker-compose up --build -d
</pre>

initialize 
<pre>
sh ./init-mysql.sh
</pre>

stop docker

<pre>
docker-compose down
</pre>

### node.js run
run node.js container

<pre>
docker-compose run --rm --service-ports nodejs
</pre>