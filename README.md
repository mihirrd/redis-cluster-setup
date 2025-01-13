## Redis cluster setup

Follow the below steps to get the cluster up and running. 

1. Make sure docker is installed and running.
2. cd into the repo and run `docker-compose up -d`. This will spin up 4 redis nodes. 
3. create the cluster using the command - `docker exec -it redis-node1 redis-cli --cluster create redis-node1:6379 redis-node2:6379 redis-node3:6379 redis-node4:6379 --cluster-replicas 0`
4. To stop the containers, use `docker-compose down`.
